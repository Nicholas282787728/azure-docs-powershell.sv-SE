---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229526"
---
# Disable-AzDataCollection

## SYNOPSIS
Avanmäler sig från insamling av data för att förbättra Azure PowerShell-cmdletarna. Data samlas in som standard om du inte uttryckligen väljer bort.

## SYNTAX

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING

`Disable-AzDataCollection`Cmdleten används för att välja bort datainsamling. Azure PowerShell samlar automatiskt in telemetridata som standard. Om du vill inaktivera datainsamling måste du uttryckligen välja bort funktionen. Microsoft sammanställer insamlade data för att identifiera mönster för användning, identifiera vanliga problem och för att förbättra Upplevelsen av Azure PowerShell. Microsoft Azure PowerShell samlar inte in några privata data eller personliga data. Om du tidigare har valt bort kör du cmdleten för att återaktivera datainsamling för `Enable-AzDataCollection` den aktuella användaren på den aktuella datorn.

## EXEMPEL

### Exempel 1: Inaktivera datainsamling för den aktuella användaren

I följande exempel visas hur du inaktiverar datainsamling för den aktuella användaren.

```powershell
Disable-AzDataCollection
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

[Enable-AzDataCollection](./Enable-AzDataCollection.md)
