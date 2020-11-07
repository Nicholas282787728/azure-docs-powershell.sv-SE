---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 15e11e9deedbc8a2e442d9b3f006511a98fd6394
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922725"
---
# Get-AzKeyVaultManagedStorageSasDefinition

## Sammanfattning
Hämtar SAS-definitioner för hanterade nycklar för viktiga valv.

## FRÅGESYNTAXEN

### ByAccountName (standard)
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDefinitionName
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Hämtar en säkerhets beskrivning för Managed Storage för viktiga nycklar om namnet på definitionen anges. Om du inte anger något definitions namn visas alla SAS-definitioner som är kopplade till det angivna lagrings kontot för Key valv som hanteras i valvet.

## BESKRIVS

### Exempel 1: lista alla sa-definitioner för hanterade nycklar
```
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'
```

Visar en lista över alla SAS-definitioner som är associerade med Key valv Managed Storage Account ' mystorageaccount ' som hanteras av valv ' online Vault '

### Exempel 2: Hämta ett hanterat lagrings konto för viktiga valv
```
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasDef'
```

Hämtar information om SAS-definitionen ' mysasDef ' som är associerad med Key valv Managed Storage-konto ' mystorageaccount ' som hanteras av valv ' The valv '.

## MALLPARAMETRAR

### -AccountName
Valv namn.
Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Namn på lagrings-sa.
Cmdlet konstruerar FQDN-namnet på en lagrings-säkerhets Association från ett valv namn, för närvarande valda miljö-, lagrings konto namn och SAS-namn.

```yaml
Type: String
Parameter Sets: ByDefinitionName
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Valv namn.
Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. 2.5.0.0. Models. ManagedStorageSasDefinitionListItem, Microsoft. Azure. commands., version =, Culture = neutralt, PublicKeyToken = null]]
Microsoft. Azure. commands. valv. Models. ManagedStorageSasDefinition

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

