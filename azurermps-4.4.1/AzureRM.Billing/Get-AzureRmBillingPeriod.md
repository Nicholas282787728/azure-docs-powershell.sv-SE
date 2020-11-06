---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: f6b75a1c161515ee45571ba3db6d2f84b95af967
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575012"
---
# Get-AzureRmBillingPeriod

## Sammanfattning
Få fakturerings perioder för abonnemanget.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### Lista (standard)
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Enda
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmBillingPeriod** erhåller abonnemangets fakturerings period.

## BESKRIVS

### Exempel 1
```
PS C:\> Get-AzureRmBillingPeriod
```

Få alla tillgängliga fakturerings perioder för abonnemanget.

### Exempel 2
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

Skaffa fakturerings perioden för abonnemanget med det angivna namnet.

### Exempel 3
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

Få maximalt 2 fakturerings perioder för abonnemanget.

## MALLPARAMETRAR

### -MaxCount
Ange det maximala antalet poster som ska returneras.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Namnet på en viss fakturerings period att få.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Billing. Models. PSBillingPeriod, Microsoft. Azure. commands. fakturering, version = 0.12.0.0, Culture = neutralt, PublicKeyToken = null]]
Microsoft. Azure. commands. Billing. Models. PSBillingPeriod

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

