---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
ms.openlocfilehash: e44b9a5c497aba5533d53acdc9aab31cb5ece703
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233678"
---
# Set-AzAutomationCredential

## SYNOPSIS
Ändrar en automatiserings credential.

## SYNTAX

```
Set-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Set-AzAutomationCredential** ändrar ett autentiseringsobjekt som ett **PSCredential-objekt** i Azure Automation.

## EXEMPEL

### Exempel 1: Uppdatera en autentisering
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

Det första kommandot tilldelar ett användarnamn till den $User variabeln.
Med det andra kommandot konverteras ett oformaterat textlösenord till en säker sträng med hjälp ConvertTo-SecureString cmdleten.
Kommandot lagrar objektet i den $Password variabeln.
Det tredje kommandot skapar en autentiserings baserat på $User och $Password, och lagrar sedan den i $Credential variabeln.
Det slutliga kommandot ändrar automatiserings credential med namnet ContosoCredential till att använda autentiserings uppgifter i $Credential.

## PARAMETERS

### -AutomationAccountName
Anger namnet på det automatiseringskonto för vilket den här cmdleten ändrar en autentiseringsuppgifter.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Beskrivning
Anger en beskrivning för de autentiseringsuppgifter som denna cmdlet ändrar.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Anger namnet på de autentiseringsuppgifter som denna cmdlet ändrar.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resursgrupp för vilken denna cmdlet ändrar en autentiseringsuppgifter.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Värde
Anger autentiseringsuppgifterna som ett **PSCredential-objekt.**

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

### System.Management.Automation.PSCredential

## UTDATA

### Microsoft.Azure.Commands.Automation.Model.CredentialInfo

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzAutomationCredential](./Get-AzAutomationCredential.md)

[New-AzAutomationCredential](./New-AzAutomationCredential.md)

[Remove-AzAutomationCredential](./Remove-AzAutomationCredential.md)


