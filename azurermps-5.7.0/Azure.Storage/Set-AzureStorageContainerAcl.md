---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerAcl.md
ms.openlocfilehash: 5cfd42ebbdae85d59bf6715f41ffbe99911ec35c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580468"
---
# Set-AzureStorageContainerAcl

## Sammanfattning
Ställer in offentlig åtkomst till en lagrings behållare.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Set-AzureStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureStorageContainerAcl** anger offentlig åtkomst behörighet för den angivna lagrings behållaren i Azure.

## BESKRIVS

### Exempel 1: ange ACL för Azure Storage-behållare med namn
```
PS C:\>Set-AzureStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

Det här kommandot skapar en behållare som inte har offentlig åtkomst.

### Exempel 2: ange ACL för Azure Storage-behållare genom att använda pipeline
```
PS C:\>Get-AzureStorageContainer container* | Set-AzureStorageContainerAcl -Permission Blob -PassThru
```

Det här kommandot får alla lagrings behållare vars namn börjar med en container och skickar sedan resultatet i pipeline för att ställa in behörigheten för alla till BLOB-åtkomst.

## MALLPARAMETRAR

### -ClientTimeoutPerRequest
Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.
Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.
Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Anger maximalt antal samtidiga nätverks samtal.
Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.
Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.
Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.
Standardvärdet är 10.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kontext
Anger Azure Storage-kontexten.
Du kan skapa det med hjälp av New-AzureStorageContext cmdlet.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Namn
Anger ett namn på en behållare.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -PassThru
Returnerar ett objekt som representerar det objekt som du arbetar med.
Denna cmdlet genererar som standard inga utdata.

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

### -Tillstånd
Anger nivån för offentlig åtkomst till den här behållaren.
Som standard kan bara en container och alla BLOB-objekt nås av lagrings kontots ägare.
Om du vill ge anonyma användare Läs behörigheter till en behållare och dess BLOB-objekt kan du ange behållar behörigheter för att aktivera offentlig åtkomst.
Anonyma användare kan läsa BLOB i en offentligt tillgänglig container utan att autentisera begäran.
De acceptabla värdena för den här parametern är:

--Container.
Ger fullständig Läs åtkomst till en behållare och dess blob.
Klienter kan räkna upp blobs i behållaren via anonym begäran men kan inte räkna upp behållare i lagrings kontot. --Blob.
Ger Läs åtkomst till BLOB-data i en behållare via anonym begäran, men ger inte åtkomst till behållar data.
Klienter kan inte räkna upp blobbar i behållaren med anonym begäran. -Av.
Begränsar åtkomst till lagrings kontots ägare.

```yaml
Type: BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Anger timeout-intervall för tjänsten i sekunder för en begäran.
Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.
Timeout för servern för varje begäran.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### IStorageContext

Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline

### Strängvärdet

Parametern "name" accepterar värdet för typen String från pipeline

## VÄRDEN

### Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageContainer

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureStorageContainer](./Get-AzureStorageContainer.md)

[New-AzureStorageContainer](./New-AzureStorageContainer.md)

[Remove-AzureStorageContainer](./Remove-AzureStorageContainer.md)


