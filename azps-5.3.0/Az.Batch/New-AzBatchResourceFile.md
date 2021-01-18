---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524749"
---
# New-AzBatchResourceFile

## Sammanfattning
Skapar en resurs fil för användning med `New-AzBatchTask` .

## FRÅGESYNTAXEN

### HttpUrl (standard)
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### StorageContainerUrl
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AutoStorageContainerName
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Skapar en resurs fil för användning med `New-AzBatchTask` .

## BESKRIVS

### Exempel 1: skapa en resurs fil från en HTTP-URL som pekar på en enda fil
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Skapar en `PSResourceFile` referens till en HTTP-URL.

### Exempel 2: skapa en resurs fil från en URL för en Azure-lagringsenhet
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Skapar en `PSResourceFile` referens till en Azure Storage container-URL. Alla filer i behållaren hämtas till den angivna mappen.

### Exempel 3: skapa en resurs fil från ett namn på en behållare för automatisk lagring
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Skapar ett `PSResourceFile` referens namn för en automatisk lagrings behållare. Alla filer i behållaren hämtas till den angivna mappen.

## MALLPARAMETRAR

### -AutoStorageContainerName
Namnet på lagrings behållaren i det automatiska lagrings kontot.

```yaml
Type: System.String
Parameter Sets: AutoStorageContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlobPrefix
Hämtar BLOB-prefixet som ska användas vid nedladdning av BLOB från en Azure Storage-behållare.
Endast blobbar vars namn börjar med det angivna prefixet hämtas.
Detta prefix kan vara ett delvis fil namn eller en under katalog.
Om ett prefix inte anges hämtas alla filer i behållaren.

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileMode
Hämtar attributet för fil behörighets läge i det oktala formatet.
Den här egenskapen är endast tillämplig om resurs filen laddas ned till en Linux-nod.
Om den här egenskapen inte anges för en Linux-nod är standardvärdet 0770.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sökväg
Den plats på noden Compute dit du vill ladda ned filen/filerna i förhållande till aktivitetens arbets katalog. Om parametern HttpUrl är angiven är fil Sök vägen obligatorisk och beskriver sökvägen som filen hämtas till, inklusive fil namnet. I annat fall är filsökväg valfri och är den katalog som du vill ladda ned filerna till om du har angett parametrarna AutoStorageContainerName eller StorageContainerUrl. I de fall då sökvägen används som katalog sparas alla katalog strukturer som redan är kopplade till indata och läggs till i den angivna katalogen för katalog tjänsten. Den angivna relativa sökvägen kan inte ta slut i aktivitetens arbets katalog (till exempel genom att använda "..").

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpUrl
URL-adressen till filen som ska hämtas.
Om URL-adressen är Azure-Blob-lagring måste den vara läsbar med anonym åtkomst. Det innebär att kommando tjänsten inte visar några autentiseringsuppgifter när blobben laddas ner.
Det finns två sätt att skaffa en sådan URL för en BLOB i Azure-lagring: inkludera en delad Access-signatur (SAS) bevilja Läs behörigheter för blobben, eller ange ACL för blobben eller dess behållare för att tillåta offentlig åtkomst.

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContainerUrl
URL-adressen för BLOB-behållaren i Azure Blob Storage.
Denna URL måste vara läsbar och kan listas med anonym åtkomst. Det innebär att kommando tjänsten inte visar några autentiseringsuppgifter när du laddar ned blobbar från behållaren.
Det finns två sätt att hämta en URL-adress för en behållare i Azure-lagring: inkludera en delad Access-signatur (SAS) bevilja Läs behörigheter för behållaren, eller ange ACL för behållaren för att tillåta offentlig åtkomst.

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft.Azure.Commands.BatCH. Modeller. PSResourceFile

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzBatchTask](./New-AzBatchTask.md)