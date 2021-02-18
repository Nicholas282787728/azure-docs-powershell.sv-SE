---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 14cd2a45e87fa5042fbf77d4c37d46211f5793a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216206"
---
# Set-AzAutomationModule

## SYNOPSIS
Uppdaterar en modul i Automation.

## SYNTAX

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Set-AzAutomationModule** uppdaterar en modul i Azure Automation.
Det här kommandot accepterar en komprimerad fil som har filnamnstillägget .zip.
Filen innehåller en mapp som innehåller en fil som är av följande typer: 
- wps_2, som har filnamnstillägget .psm1 eller .dll 
- wps_2 modulmanifest, som har filnamnstillägget .psd1. Namnet på ZIP-filen, namnet på mappen och namnet på filen i mappen måste vara samma.
Ange ZIP-filen som en URL som automationstjänsten kan komma åt.
Om du importerar wps_2 modul till Automation med hjälp av den här cmdleten New-AzAutomationModule cmdleten är åtgärden asynkron.
Kommandot avslutas oavsett om importen lyckas eller misslyckas.
Kör följande kommando för att kontrollera om det lyckades: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName kontrollera **egenskapen ProvisioningState** för värdet Succeeded.

## EXEMPEL

### Exempel 1: Uppdatera en modul
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

Med det här kommandot importeras en uppdaterad version av en befintlig modul med namnet ContosoModule till automatiseringskontot Contoso17.  Modulen lagras i en Azure-blob i ett lagringskonto med namnet contosostorage och en behållare som heter moduler.

## PARAMETERS

### -AutomationAccountName
Anger namnet på det automatiseringskonto för vilket den här cmdleten uppdaterar en modul.

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
Anger URL:en för ZIP-filen som innehåller den nya versionen av en modul som cmdleten importerar.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContentLinkVersion
Anger versionen av modulen som cmdleten uppdaterar automation till.

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
Anger namnet på en resursgrupp för vilken denna cmdlet uppdaterar en modul.

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

[New-AzAutomationModule](./New-AzAutomationModule.md)

[Remove-AzAutomationModule](./Remove-AzAutomationModule.md)


