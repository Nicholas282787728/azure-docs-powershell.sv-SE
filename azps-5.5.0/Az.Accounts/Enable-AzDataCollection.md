---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229503"
---
# Enable-AzDataCollection

## SYNOPSIS
Gör att Azure PowerShell kan samla in data för att förbättra användarupplevelsen med Azure PowerShell-cmdlets. När du kör den här cmdleten registrera sig för datainsamling för den aktuella användaren på den aktuella datorn. Data samlas in som standard om du inte uttryckligen väljer bort.

## SYNTAX

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING

`Enable-AzDataCollection`Cmdleten används för att registrera sig för datainsamling. Azure PowerShell samlar automatiskt in telemetridata som standard. Microsoft sammanställer insamlade data för att identifiera mönster för användning, identifiera vanliga problem och för att förbättra Upplevelsen av Azure PowerShell.
Microsoft Azure PowerShell samlar inte in några privata data eller personliga data. Om du vill inaktivera datainsamling måste du uttryckligen välja bort det genom att `Disable-AzDataCollection` köra.

## EXEMPEL

### Exempel 1: Aktivera datainsamling för den aktuella användaren

I följande exempel visas hur du aktiverar datainsamling för den aktuella användaren.

```powershell
Enable-AzDataCollection
```

## PARAMETERS

### -DefaultProfile

Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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

### -Bekräfta

Frågar dig om bekräftelse innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Visar vad som skulle hända om cmdleten körs. Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)

## INDATA

### Ingen

## UTDATA

### System.Void

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Disable-AzDataCollection](./Disable-AzDataCollection.md)
