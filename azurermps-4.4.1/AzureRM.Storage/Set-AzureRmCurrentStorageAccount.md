---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmCurrentStorageAccount.md
ms.openlocfilehash: 73680e82a9d898075e905d88bcc8602609a5612d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755903"
---
# Set-AzureRmCurrentStorageAccount

## Sammanfattning
Ändrar det aktuella lagrings kontot för den angivna prenumerationen.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### UsingResourceGroupAndNameParameterSet (standard)
```
Set-AzureRmCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### UsingStorageContext
```
Set-AzureRmCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureRmCurrentStorageAccount** ändrar det aktuella Azure Storage-kontot för det angivna Azure-abonnemanget i Azure PowerShell.
Det aktuella lagrings kontot används som standard när du öppnar lagring utan att ange ett lagrings konto namn.

## BESKRIVS

### Exempel 1: Ange det aktuella lagrings kontot
```
PS C:\>Set-AzureRmCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

Det här kommandot anger standard lagrings kontot för den angivna prenumerationen.

## MALLPARAMETRAR

### -Kontext
Anger ett **AzureStorageContext** -objekt för det aktuella lagrings kontot.
Använd New-AzureStorageContext cmdlet för att få ett lagrings kontext objekt.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UsingStorageContext
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Namn
Anger namnet på det lagrings konto som denna cmdlet ändrar.

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger den resurs grupp som innehåller det lagrings konto som ska ändras.

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: 

Required: True
Position: Named
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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Set-AzureRmStorageAccount](./Set-AzureRmStorageAccount.md)


