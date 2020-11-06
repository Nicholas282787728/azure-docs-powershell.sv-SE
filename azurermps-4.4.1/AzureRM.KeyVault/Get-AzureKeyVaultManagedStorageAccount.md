---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 7bf6539aaf849177d6e9da1fd74bcbedc28c8763
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582396"
---
# Get-AzureKeyVaultManagedStorageAccount

## Sammanfattning
Hämtar Key valv-hanterade Azure Storage-konton.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ByVaultName (standard)
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByAccountName
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Hämtar ett nyckel valv hanterat Azure Storage-konto om namnet på kontot anges och konto nycklarna hanteras av det angivna valvet. Om konto namnet inte anges visas alla konton vars nycklar hanteras av angivet valv.

## BESKRIVS

### Exempel 1: lista alla hanterade lagrings konton för viktiga valv nycklar
```
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault'
```

Visar alla konton vars nycklar hanteras av valv ' Mina valv '

### Exempel 2: Hämta ett hanterat lagrings konto för viktiga valv
```
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'
```

Hämtar information om Key valv Managed Storage-kontot för ' mystorageaccount ' om dess nycklar hanteras av valvet ' för valv '

## MALLPARAMETRAR

### -AccountName
Namn på hanterat lagrings konto för viktiga valv. Cmdlet konstruerar FQDN för ett hanterat lagrings konto namn från valv namn, valt miljö-och manged.

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Valv namn.
Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.

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

### System. String

## VÄRDEN

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. 2.5.0.0. Models. ManagedStorageAccount, Microsoft. Azure. commands., version =, Culture = neutralt, PublicKeyToken = null]]
Microsoft. Azure. commands. valv. Models. ManagedStorageAccount

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

