---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacesharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
ms.openlocfilehash: 75c69c96b82cf71aa71d4ac89bb10c064af1f4f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223494"
---
# Get-AzOperationalInsightsWorkspaceSharedKey

## SYNOPSIS
Hämtar de delade nycklarna för en arbetsyta.

## SYNTAX

```
Get-AzOperationalInsightsWorkspaceSharedKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten Get-AzOperationalInsightsWorkspaceSharedKey** visar de delade nycklarna för en arbetsyta.
Nycklarna används för att ansluta Operational Insights-representanter till arbetsytan.

## EXEMPEL

### Exempel 1: Hämta delade nycklar efter arbetsytans namn
```
PS C:\>Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

Med det här kommandot får du de delade nycklarna för arbetsytan MyWorkspace i resursgruppen ContosoResourceGroup.

### Exempel 2: Hämta delade nycklar med hjälp av pipelinen
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceSharedKey
```

Det här kommandot hämtar arbetsytan MyWorkspace med cmdleten Get-AzOperationalInsightsWorkspace och skickar sedan arbetsytan till **cmdleten Get-AzOperationalInsightsWorkspaceSharedKey.**
Kommandot hämtar de delade nycklarna för arbetsytan.

## PARAMETERS

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
Anger namnet på arbetsytan.

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

### -ResourceGroupName
Anger namnet på en Azure-resursgrupp.

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

## UTDATA

### Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Azure Operational Insights-cmdlets](./Az.OperationalInsights.md)

[Get-AzOperationalInsightsWorkspace](./Get-AzOperationalInsightsWorkspace.md)


