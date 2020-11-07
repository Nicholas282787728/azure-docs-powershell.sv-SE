---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
ms.openlocfilehash: 104a5b1ff5cde0f3ea55a29e87e38e6adaaf0488
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923686"
---
# Get-AzStorageBlob

## Sammanfattning
Visar blobbar i en behållare.

## FRÅGESYNTAXEN

### BlobName (standard)
```
Get-AzStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### BlobPrefix
```
Get-AzStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzStorageBlob** visar blobbar i den angivna behållaren i ett Azure Storage-konto.

## BESKRIVS

### Exempel 1: skaffa en BLOB per BLOB-namn
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob blob*
```

Det här kommandot använder ett BLOB-namn och ett jokertecken för att hämta en blob.

### Exempel 2: skaffa blobs i en container med hjälp av pipeline
```
PS C:\>Get-AzStorageContainer -Name container* | Get-AzStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

Det här kommandot använder pipeline för att hämta alla blobbar (inklusive BLOB i borttaget) i en behållare.

### Exempel 3: Hämta blobs efter namn
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Prefix "blob"
```

Det här kommandot använder ett namn prefix för att hämta blob.

### Exempel 4: list-BLOB i flera batchar
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

I det här exemplet används parametrarna *MaxCount* och *ContinuationToken* för att lista Azure Storage BLOB i flera batchar.
De första fyra kommandona tilldelar värden till variabler som ska användas i exemplet.
Det femte kommandot anger en **do-while-** sats som använder cmdleten **Get-AzStorageBlob** för att hämta blobs.
Uttrycket innehåller det tilläggs token som lagras i $Token variabeln.
$Token ändrar värde när slingan körs.
Om du vill ha mer information skriver du `Get-Help About_Do` .
Det sista kommandot använder kommandot **ECHO** för att visa summan.

## MALLPARAMETRAR

### -BLOB
Anger ett namn eller namn mönster som kan användas för sökning med jokertecken.
Om inget BLOB-namn anges visar cmdleten alla blobbar i den angivna behållaren.
Om du anger ett värde för den här parametern visar cmdleten alla blobbar med namn som matchar den här parametern.

```yaml
Type: System.String
Parameter Sets: BlobName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientTimeoutPerRequest
Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.
Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.
Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.

```yaml
Type: System.Nullable`1[System.Int32]
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
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Container
Anger namnet på behållaren.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kontext
Anger det Azure Storage-konto som du vill få en lista över blobs från.
Du kan använda New-AzStorageContext cmdlet för att skapa en lagrings kontext.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ContinuationToken
Anger ett fortsättnings-token för BLOB-listan.
Använd den här parametern och parametern *MaxCount* om du vill visa blobs i flera batchar.

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
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

### -IncludeDeleted
Ta bort blob som standard tar inte bort blob.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxCount
Anger det maximala antalet objekt som denna cmdlet returnerar.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Prefix
Anger ett prefix för de BLOB-namn som du vill hämta.
Den här parametern stöder inte användning av vanliga uttryck eller jokertecken för att söka.
Det innebär att om behållaren bara innehåller blobbar med namnet "My", "MyBlob1" och "MyBlob2" och du anger "-prefix My *", returnerar cmdleten inga blob.
Men om du anger "prefixet My" returnerar cmdleten "My", "MyBlob1" och "MyBlob2".

```yaml
Type: System.String
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Anger timeout-intervall för tjänsten i sekunder för en begäran.
Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

### Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext

## VÄRDEN

### Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageBlob

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzStorageBlobContent](./Get-AzStorageBlobContent.md)

[Remove-AzStorageBlob](./Remove-AzStorageBlob.md)

[Set-AzStorageBlobContent](./Set-AzStorageBlobContent.md)


