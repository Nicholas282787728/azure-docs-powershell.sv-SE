---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: 2ad9574cbd50c4100dbda7b35a64e557b195898a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090089"
---
# Get-AzDtlAutoShutdownPolicy

## Sammanfattning
Hämtar policyn för automatisk avslutning av ett labb i DevTest Labs.

## FRÅGESYNTAXEN

```
Get-AzDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzDtlAutoShutdownPolicy** hämtar den automatiska avslutnings principen för ett labb, vilket gör att du automatiskt kan stänga av alla virtuella datorer i ett labb under en viss tid.
Cmdleten returnerar om principens status är aktive rad och den tid som du har angett för att stänga av virtuella laboratorie datorer automatiskt.

## BESKRIVS

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

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
Anger namnet på den Lab för vilken denna cmdlet får principen för automatisk avstängning.

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
Anger namnet på den resurs grupp som laboratoriet hör till.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. commands. DevTestLabs. Models. PSSchedule

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Set-AzDtlAutoShutdownPolicy](./Set-AzDtlAutoShutdownPolicy.md)


