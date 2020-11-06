---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
ms.openlocfilehash: 48de3ae521f77c531433ffca67dadc9e2c46a980
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582804"
---
# New-AzureRmBatchAccountKey

## Sammanfattning
Återskapar en Key för ett batch-konto.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
New-AzureRmBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
**New-AzureRmBatchAccountKey** cmdlet återskapar den primära eller sekundära nyckeln för ett Azure Batch-konto.
Cmdleten returnerar ett **BatchAccountContext** -objekt som har dess aktuella **PrimaryAccountKey** -och **SecondaryAccountKey** -egenskaper.

## BESKRIVS

### Exempel 1: återskapa primär konto nyckeln på ett batch-konto
```
PS C:\>New-AzureRmBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller

Location                     : westus

ResourceGroupName            : CmdletExampleRG

CoreQuota                    : 20

PoolQuota                    : 20

ActiveJobAndJobScheduleQuota : 20

Tags                         : 
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

Det här kommandot återskapar den primära konto nyckeln för batch-kontot som heter pfuller.

## MALLPARAMETRAR

### -AccountName
Anger namnet på det kommando konto som denna cmdlet återskapar en nyckeln för.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Värdetyp
Anger den typ av nycklar som denna cmdlet återskapar.
Giltiga värden är: 
- Första
- Sekundär

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger resurs gruppen för det konto som denna cmdlet återskapar en nyckeln för.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Cmdlets för Azure Batch](./AzureRM.Batch.md)


