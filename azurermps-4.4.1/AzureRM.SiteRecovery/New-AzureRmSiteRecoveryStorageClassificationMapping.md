---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4B4CB198-ABD3-4926-808D-2087151EA06B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 2520dd90eed1362f4d499eb88ce88dec33f1338c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574509"
---
# New-AzureRmSiteRecoveryStorageClassificationMapping

## Sammanfattning
Skapar en mappning för lagrings klassificering i webbplats återställning.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
New-AzureRmSiteRecoveryStorageClassificationMapping [-Name <String>]
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmSiteRecoveryStorageClassificationMapping** skapar en mappning för lagrings klassificering i Azure Site Recovery.

## BESKRIVS

## MALLPARAMETRAR

### -Namn
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimaryStorageClassification
Anger primär mappning för lagrings klassificering.

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecoveryStorageClassification
Anger en klassificerings mappning för en lagrings plats.

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
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

### ASRStorageClassification
Parametern ' PrimaryStorageClassification ' godkänner värdet av typen ' ASRStorageClassification ' från pipeline

## VÄRDEN

### Microsoft. Azure. commands. SiteRecovery. ASRJob

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmSiteRecoveryStorageClassificationMapping](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[Remove-AzureRmSiteRecoveryStorageClassificationMapping](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
