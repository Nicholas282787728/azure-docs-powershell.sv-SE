---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
ms.openlocfilehash: d4e58e1fc2da68d9293afa27072a4cf32023f661
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756564"
---
# Get-AzureRmProviderOperation

## Sammanfattning
Hämtar de åtgärder för en Azure-adressresurs som är skyddade med Azure RBAC.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmProviderOperation [-OperationSearchString] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Get-AzureRmProviderOperation får de operationer som tillhandahålls av Azure Resource providers.
Operationer kan skapas för att skapa anpassade roller i Azure RBAC.
Kommandot tar sig en gång i Sök strängen (med möjligt jokertecken (*) tecken som avgör vilka verksamhets uppgifter som ska visas.

Använd Get-AzureRmProviderOperation * för att få alla funktioner för alla Azure Resource-leverantörer.

Använd Get-AzureRmProviderOperation Microsoft. Compute/* för att få alla funktioner i Microsoft. Compute Resource Provider.

## BESKRIVS

### --------------------------Få alla åtgärder--------------------------
```
PS C:\> Get-AzureRmProviderOperation *
```

### --------------------------Få instruktioner för en viss resurs leverantör--------------------------
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### --------------------------Få alla åtgärder som kan utföras på virtuella datorer--------------------------
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## MALLPARAMETRAR

### -OperationSearchString
Sök strängen för åtgärden (med möjliga jokertecken (*))

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

### Strängvärdet
Parametern ' OperationSearchString ' godkänner värdet för typen String från pipeline

## VÄRDEN

### Microsoft. Azure. commands. Resources. Models. PSResourceProviderOperation

## ANMÄRKNINGAR
Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution

## RELATERADE LÄNKAR

