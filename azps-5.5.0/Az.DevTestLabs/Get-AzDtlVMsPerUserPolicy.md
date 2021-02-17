---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: f2d8604de126dcdfa830bdd6650cf66a6db391b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234503"
---
# Get-AzDtlVMsPerUserPolicy

## SYNOPSIS
Hämtar virtuella datorer per användarprincip för ett labb i DevTest Labs.

## SYNTAX

```
Get-AzDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzDtlVMsPerUserPolicy** hämtar virtuella maskiner per användarprincip för ett labb, vilket gör att du kan ange det maximala antalet virtuella maskiner per användare.
Cmdleten returnerar den aktiverade eller inaktiverade statusen för principen och det maximala antalet virtuella datorer som tillåts per användare som du har angett i principen.

## EXEMPEL

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

### -LabName
Anger namnet på det labb som cmdleten hämtar den virtuella datorn för per användarprincip.

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

### -ResourceGroupName
Anger namnet på den resursgrupp som labbet tillhör.

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

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

## UTDATA

### Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Set-AzDtlVMsPerUserPolicy](./Set-AzDtlVMsPerUserPolicy.md)


