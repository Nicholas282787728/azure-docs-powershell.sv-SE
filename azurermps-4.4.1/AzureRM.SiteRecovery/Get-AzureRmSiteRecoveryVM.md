---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: A5697F1E-623A-4E26-96C8-6197852BFFAA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 9f594b61b1ad34a39ea0a84381f6181cadc418c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755915"
---
# Get-AzureRmSiteRecoveryVM

## Sammanfattning
Hämtar information om virtuella datorer som hanteras av webbplats återställning.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ByObject (standard)
```
Get-AzureRmSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObjectWithName
```
Get-AzureRmSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObjectWithFriendlyName
```
Get-AzureRmSiteRecoveryVM -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmSiteRecoveryVM** hämtar information om virtuella datorer som hanteras i Azure Site Recovery.

## BESKRIVS

## MALLPARAMETRAR

### -FriendlyName
Anger det egna namnet på den virtuella datorn.

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på den virtuella datorn.

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionContainer
Anger objekt för objektet för webbplats återställnings skydd.

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### ASRProtectionContainer
Parametern ' ProtectionContainer ' godkänner värdet av typen ' ASRProtectionContainer ' från pipeline

### ASRProtectionContainer
Parametern ' ProtectionContainer ' godkänner värdet av typen ' ASRProtectionContainer ' från pipeline

## VÄRDEN

### System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRVirtualMachine]

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Set-AzureRmSiteRecoveryVM](./Set-AzureRmSiteRecoveryVM.md)
