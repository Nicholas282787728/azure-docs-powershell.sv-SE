---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
ms.openlocfilehash: 8590c9566cf84648dc8668d3fb49ac19b8d4787d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755367"
---
# Get-AzureRmStorageAccountNameAvailability

## Sammanfattning
Kontrollerar tillgänglighet för ett lagrings konto namn.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmStorageAccountNameAvailability** kontrollerar om namnet på ett Azure Storage-konto är giltigt och tillgängligt för användning.

## BESKRIVS

### Exempel 1: kontrol lera tillgänglighet för ett lagrings konto namn
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'ContosoStorage03'
```

Det här kommandot kontrollerar tillgängligheten för namnet ContosoStorage03.

## MALLPARAMETRAR

### -Namn
Anger namnet på det lagrings konto som denna cmdlet kontrollerar.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Azure Storage Manager-cmdletar](./AzureRM.Storage.md)
