---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: c176c9b8726c4f0edfebcebdc77197f1d555807d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235134"
---
# New-AzAutomationModule

## SYNOPSIS
Importerar en modul till Automation.

## SYNTAX

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzAutomationModule** importerar en modul till Azure Automation.
Det här kommandot accepterar en komprimerad fil med filnamnstillägget ZIP.
Filen innehåller en mapp som innehåller en fil som är av följande typer: 
- Windows PowerShell-modul som har filnamnstillägget .psm1 eller .dll 
- Windows PowerShell-modulmanifest, som har filnamnstillägget .psd1. Namnet på ZIP-filen, namnet på mappen och namnet på filen i mappen måste vara samma.
Ange ZIP-filen som en URL som automationstjänsten kan komma åt.
Om du importerar en Windows PowerShell-modul till Automation med hjälp av den här cmdleten eller Set-AzAutomationModule-cmdleten är åtgärden asynkron.
Kommandot avslutas oavsett om importen lyckas eller misslyckas.
Kör följande kommando för att kontrollera om det lyckades: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName kontrollera **egenskapen ProvisioningState** för värdet Succeeded.

## EXEMPEL

### Exempel 1: Importera en modul
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

Med det här kommandot importeras modulen ContosoModule till automationskontot Contoso17.
Modulen lagras i en Azure-blob i ett lagringskonto med namnet contosostorage och en behållare som heter moduler.

## PARAMETERS

### -AutomationAccountName
Anger namnet på det automatiseringskonto för vilket denna cmdlet importerar en modul.

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

### -ContentLinkUri
URL-adressen till ett modul zip-paket

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
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

### -Name
Anger namnet på modulen som cmdleten importerar.

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
Anger namnet på en resursgrupp för vilken denna cmdlet importerar en modul.

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

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

### System.Uri

## UTDATA

### Microsoft.Azure.Commands.Automation.Model.Module

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzAutomationModule](./Get-AzAutomationModule.md)

[Remove-AzAutomationModule](./Remove-AzAutomationModule.md)

[Set-AzAutomationModule](./Set-AzAutomationModule.md)


