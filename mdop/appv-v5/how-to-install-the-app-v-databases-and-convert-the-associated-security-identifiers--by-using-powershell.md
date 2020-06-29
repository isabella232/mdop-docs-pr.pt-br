---
title: Como instalar os bancos de dados do App-V e converter os identificadores de segurança associados usando o PowerShell
description: Como instalar os bancos de dados do App-V e converter os identificadores de segurança associados usando o PowerShell
author: dansimp
ms.assetid: 9399342b-1ea7-41df-b988-33e302f9debe
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bb4ff48a532d4c9ec7035421c6e8e7dcd41f5214
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796401"
---
# Como instalar os bancos de dados do App-V e converter os identificadores de segurança associados usando o PowerShell


Use o procedimento a seguir do PowerShell para converter qualquer número de contas de usuário ou computador dos serviços de domínio Active Directory (AD DS) em identificadores de segurança formatados (SIDs) no formato padrão e no formato hexadecimal usado pelo Microsoft SQL Server ao executar scripts SQL.

Antes de tentar este procedimento, você deve ler e entender as informações e os exemplos exibidos na lista a seguir:

-   **. ENTRADAS** – a conta ou contas usadas para converter em formato Sid. Pode ser um único nome de conta ou uma matriz de nomes de conta.

-   **. SAÍDAS** -uma lista de nomes de conta com o Sid correspondente nos formatos padrão e hexadecimal.

-   **Exemplos** -

    **.\\ConvertToSID.ps1 DOMAIN\\user\ _account1 DOMAIN\\machine\ _account1 $ DOMAIN\\user\ _account2 | Format-List**.

    **$accountsArray = @ ("DOMAIN\\user\ _account1", "DOMAIN\\machine\ _account1 $", "domínio \ _user \ _account2")**

    **.\\ConvertToSID.ps1 $accountsArray | Write-Output-FilePath .\\SIDs.txt-Width 200**

    \#&gt;

**Para converter qualquer número de contas de usuário ou máquina de serviços de domínio Active Directory (AD DS) em SIDs (identificadores de segurança formatados)**

1. Copie o script a seguir em um editor de texto e salve-o como um arquivo de script do PowerShell, por exemplo **ConvertToSIDs.ps1**.

2. Para abrir um console do PowerShell, clique em **Iniciar** e digite **PowerShell**. Clique com o botão direito do mouse em **Windows PowerShell** e selecione **Executar como Administrador**.

   ```powershell
   <#
   .SYNOPSIS
   This PowerShell script will take an array of account names and try to convert each of them to the corresponding SID in standard and hexadecimal formats.

   .DESCRIPTION
   This is a PowerShell script that converts any number of Active Directory (AD) user or machine accounts into formatted Security Identifiers (SIDs) both in the standard format and in the hexadecimal format used by SQL server when running SQL scripts.

   .INPUTS
   The account(s) to convert to SID format. This can be a single account name or an array of account names. Please see examples below.

   .OUTPUTS
   A list of account names with the corresponding SID in standard and hexadecimal formats

   .EXAMPLE
   .\ConvertToSID.ps1 DOMAIN\user_account1 DOMAIN\machine_account1$ DOMAIN\user_account2 | Format-List

   .EXAMPLE
   $accountsArray = @("DOMAIN\user_account1", "DOMAIN\machine_account1$", "DOMAIN_user_account2")

   .\ConvertToSID.ps1 $accountsArray | Write-Output -FilePath .\SIDs.txt -Width 200
   #>

   function ConvertSIDToHexFormat
   {
      param([System.Security.Principal.SecurityIdentifier]$sidToConvert)

      $sb = New-Object System.Text.StringBuilder

      [int] $binLength = $sidToConvert.BinaryLength

      [Byte[]] $byteArray = New-Object Byte[] $binLength

      $sidToConvert.GetBinaryForm($byteArray, 0)

      foreach($byte in $byteArray)
      {
          $sb.Append($byte.ToString("X2")) |Out-Null
      }
      return $sb.ToString()
   }

   [string[]]$myArgs = $args



   if(($myArgs.Length -lt 1) -or ($myArgs[0].CompareTo("/?") -eq 0))
   {
       [string]::Format("{0}====== Description ======{0}{0}" +
                  "  Converts any number of user or machine account names to string and hexadecimal SIDs.{0}" +
                  "  Pass the account(s) as space separated command line parameters. (For example 'ConvertToSID.exe DOMAIN\\Account1 DOMAIN\\Account2 ...'){0}" +
                  "  The output is written to the console in the format 'Account name    SID as string   SID as hexadecimal'{0}" +
                  "  And can be written out to a file using standard PowerShell redirection{0}" +
                  "  Please specify user accounts in the format 'DOMAIN\username'{0}" +
                  "  Please specify machine accounts in the format 'DOMAIN\machinename$'{0}" +
                  "  For more help content, please run 'Get-Help ConvertToSID.ps1'{0}" +
                  "{0}====== Arguments ======{0}" +



                  "{0}  /?    Show this help message", [Environment]::NewLine)
   }
   else
   {
       #If an array was passed in, try to split it
       if($myArgs.Length -eq 1)
       {
           $myArgs = $myArgs.Split(' ')
       }

       #Parse the arguments for account names
       foreach($accountName in $myArgs)
       {
           [string[]] $splitString = $accountName.Split('\')  # We're looking for the format "DOMAIN\Account" so anything that does not match, we reject

           if($splitString.Length -ne 2)
           {
               $message = [string]::Format("{0} is not a valid account name. Expected format 'Domain\username' for user accounts or 'DOMAIN\machinename$' for machine accounts.", $accountName)

               Write-Error -Message $message
               continue
           }

           #Convert any account names to SIDs
           try
           {
               [System.Security.Principal.NTAccount] $account = New-Object System.Security.Principal.NTAccount($splitString[0], $splitString[1])

               [System.Security.Principal.SecurityIdentifier] $SID = [System.Security.Principal.SecurityIdentifier]($account.Translate([System.Security.Principal.SecurityIdentifier]))
           }
           catch [System.Security.Principal.IdentityNotMappedException]
           {
               $message = [string]::Format("Failed to translate account object '{0}' to a SID. Please verify that this is a valid user or machine account.", $account.ToString())

               Write-Error -Message $message

               continue
           }

           #Convert regular SID to binary format used by SQL

           $hexSIDString = ConvertSIDToHexFormat $SID

           $SIDs = New-Object PSObject

           $SIDs | Add-Member NoteProperty Account $accountName

           $SIDs | Add-Member NoteProperty SID $SID.ToString()

           $SIDs | Add-Member NoteProperty Hexadecimal $hexSIDString

           Write-Output $SIDs
       }
   }
   ```

3. Execute o script que você salvou na etapa um deste procedimento passando as contas para converter como argumentos.

   Por exemplo,

   **.\\ConvertToSID.ps1 DOMAIN\\user\ _account1 DOMAIN\\machine\ _account1 $ DOMAIN\\user\ _account2 | Format-List "ou" $accountsArray = @ ("DOMAIN\\user\ _account1", "DOMAIN\\machine\ _account1 $", "domínio \ _user \ _account2")**

   **.\\ConvertToSID.ps1 $accountsArray | Write-Output-FilePath .\\SIDs.txt-Width 200 "**

   **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Administração do App-V usando o PowerShell](administering-app-v-by-using-powershell.md)
