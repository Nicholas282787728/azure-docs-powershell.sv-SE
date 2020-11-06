---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 1b00930332d9f3f5a78e4cfe8ab7478a5dc5fa19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582900"
---
# New-AzureRmStorageAccount

## Sammanfattning
Skapar ett lagrings konto.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [[-Kind] <String>] [[-AccessTier] <String>] [[-CustomDomainName] <String>]
 [[-UseSubDomain] <Boolean>] [[-EnableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmStorageAccount** skapar ett Azure Storage-konto.

## BESKRIVS

### Exempel 1: skapa ett lagrings konto
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS"
```

Det här kommandot skapar ett lagrings konto för resurs grupps namnet MyResourceGroup.

### Exempel 2: skapa ett Blob Storage-konto som använder Storage Service Encryption
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS" -EnableEncryptionService Blob -Kind "BlobStorage" -AccessTier Hot
```

Det här kommandot skapar ett Blob Storage-konto som använder typen varm åtkomst.
Kontot har aktiverat Storage Service-kryptering för Blob-tjänsten.

### Exempel 3: skapa ett lagrings konto som möjliggör kryptering av lagrings tjänst för blob och fil tjänster och skapa och tilldela en identitet för Azure-valv.
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS" -EnableEncryptionService "Blob,File" -AssignIdentity
```

Det här kommandot skapar ett lagrings konto med aktiverat Storage Service-kryptering för blob och fil tjänster.  Den skapar också och tilldelar en identitet som kan användas för att hantera konto nycklar via Azure-nyckel valv.

## MALLPARAMETRAR

### -AccessTier
Anger åtkomst nivån för det lagrings konto som skapas av denna cmdlet.
De acceptabla värdena för denna parameter är: varmt och coolt.

Om du anger ett värde för BlobStorage för parametern *sort* måste du ange ett värde för parametern *AccessTier* .

Om du anger ett värde för lagring för denna *sort* parameter ska du inte ange parametern *AccessTier* .

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignIdentity
Skapa och tilldela en ny lagrings konto identitet för det här lagrings kontot för användning med hanterings tjänster som Azure-valv.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomDomainName
Anger namnet på lagrings kontots anpassade domän.
Standardvärdet är lagring.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableEncryptionService
Anger om denna cmdlet aktiverar Storage Service-kryptering för lagrings tjänsten.
Stöd för Azure-blob och Azure File Services.

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHttpsTrafficOnly
Anger om lagrings kontot endast aktiverar HTTPS-trafik.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InformationAction
Anger hur den här cmdleten svarar på en informations händelse.

De acceptabla värdena för den här parametern är:

- Vidare
- Över
- Inquire
- SilentlyContinue
- Stanna
- Avbryt

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Anger en informations variabel.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sort
Anger den typ av lagrings konto som denna cmdlet skapar.
De acceptabla värdena för den här parametern är:

- Lagringsrelaterade.
Allmänt syfte lagrings konto som stöder lagring av blobbar, tabeller, köer, filer och diskar.

- BlobStorage.
Blob Storage-konto som endast stöder lagring av BLOB.


Standardvärdet är lagring.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plats
Anger platsen för det lagrings konto som ska skapas.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på det lagrings konto som ska skapas.

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

### -ResourceGroupName
Anger namnet på den resurs grupp där lagrings kontot ska läggas till.

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

### -SkuName
Anger SKU-namnet på det lagrings konto som skapas av denna cmdlet.
De acceptabla värdena för den här parametern är:

- Standard_LRS.
Lokalt-redundant lagring.
- Standard_ZRS.
Zone – redundant lagring.
- Standard_GRS.
Geo-redundant lagring.
- Standard_RAGRS.
Läs åtkomst Geo-redundant lagring.
- Premium_LRS.
Premium lokalt-redundant lagring.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tagg
Om du anger ett värde för BlobStorage för parametern *sort* måste du ange ett värde för parametern *AccessTier* .

Om du anger ett värde för lagring för denna *sort* parameter ska du inte ange parametern *AccessTier* .

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseSubDomain
Anger om indirekt CName-verifiering ska aktive ras.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
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

[Get-AzureRmStorageAccount](./Get-AzureRmStorageAccount.md)

[Remove-AzureRmStorageAccount](./Remove-AzureRmStorageAccount.md)

[Set-AzureRmStorageAccount](./Set-AzureRmStorageAccount.md)
