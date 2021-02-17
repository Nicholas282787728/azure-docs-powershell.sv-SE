---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: bffe2874effb99b3fbcca77888a3108bc3798311
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220543"
---
# Get-AzProviderOperation

## SYNOPSIS
Hämtar åtgärderna för en Azure-resursleverantör som kan skyddas med Azure RBAC.

## SYNTAX

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
I Get-AzProviderOperation av åtgärder som exponeras av Azure-resursleverantörer.
Åtgärder kan skapas för att skapa anpassade roller i Azure RBAC.
Kommandot tar som indata en söksträng (med möjliga jokertecken( ) som bestämmer vilka *åtgärdsinformation som ska visas. Använd Get-AzProviderOperation * för att få alla åtgärder för alla Azure-resursleverantörer. Använd Get-AzProviderOperation Microsoft.Compute/ för* att få alla åtgärder från Microsoft.Compute-resursleverantören.

## EXEMPEL

### Exempel 1: Hämta alla åtgärder för alla leverantörer
```powershell
PS C:\> Get-AzProviderOperation *
```

### Exempel 2: Hämta åtgärder för en viss resursleverantör
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### Exempel 3: Hämta alla åtgärder som kan utföras på virtuella datorer
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

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

### -OperationSearchString
Söksträngen för åtgärden (med möjliga jokertecken (*) tecken)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

## UTDATA

### Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation

## ANTECKNINGAR
Nyckelord: azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, mall, distribution

## RELATERADE LÄNKAR
