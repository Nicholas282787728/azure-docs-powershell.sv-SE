---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239251"
---
# New-AzBatchResourceFile

## SYNOPSIS
Skapar en resursfil för användning `New-AzBatchTask` efter.

## SYNTAX

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

## BESKRIVNING
Skapar en resursfil för användning `New-AzBatchTask` efter.

## EXEMPEL

### Exempel 1: Skapa en resursfil från en HTTP-URL som pekar på en enda fil
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Skapar en `PSResourceFile` referens till en HTTP-URL.

### Exempel 2: Skapa en resursfil från en URL till en Azure Storage-behållare
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Skapar en `PSResourceFile` referens till URL-adressen till en Azure Storage-behållare. Alla filer i behållaren laddas ned till den angivna mappen.

### Exempel 3: Skapa en resursfil från ett namn på en behållare för automatisk lagring
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Skapar en `PSResourceFile` referens till behållarnamnet Automatisk lagring. Alla filer i behållaren laddas ned till den angivna mappen.

## PARAMETERS

### -AutoStorageContainerName
Namnet på lagringsbehållaren i kontot för automatisk lagring.

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
Hämtar blob-prefixet som ska användas när du hämtar blobbar från en Azure Storage-behållare.
Endast blobbar vars namn börjar med det angivna prefixet laddas ned.
Prefixet kan vara en del av filnamnet eller en underkatalog.
Om inget prefix anges laddas alla filer i behållaren ned.

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
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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
Hämtar attributet filbehörighetsläge i oktalt format.
Den här egenskapen gäller endast om resursfilen laddas ned till en Linux-nod.
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

### -FilePath
Platsen på beräkningsnoden som du vill ladda ned filer till i förhållande till aktivitetens arbetskatalog. Om httpUrl-parametern anges är FilePath obligatoriskt och beskriver sökvägen som filen ska laddas ned till, inklusive filnamnet. Om parametrarna AutoStorageContainerName eller StorageContainerUrl har angetts är FilePath valfritt och är då katalogen som filerna hämtas till. I de fall där FilePath används som katalog kommer alla katalogstrukturer som redan är associerade med indata att behållas i sin helhet och läggas till i den angivna FilePath-katalogen. Den angivna relativa sökvägen kan inte bryta ut från aktivitetens arbetskatalog (till exempel genom att använda ".").

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
URL-adressen till filen som ska laddas ned.
Om URL:en är Azure Blob Storage måste den vara läsbar med anonym åtkomst. Det innebär att batchtjänsten inte presenterar några autentiseringsuppgifter när du hämtar blob-filen.
Det finns två sätt att få en sådan URL för en blob i Azure-lagring: inkludera EN SAS (Shared Access Signature) som beviljar läsbehörigheter för bloben, eller ange ACL för bloben eller dess behållare för att tillåta offentlig åtkomst.

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
URL-adressen för blob-behållaren i Azure Blob Storage.
Den här URL-adressen måste vara läsbar och listbar med anonym åtkomst. Batchtjänsten presenterar inga autentiseringsuppgifter när du hämtar blobbar från behållaren.
Det finns två sätt att få en sådan URL för en behållare i Azure-lagring: inkludera EN SAS (Shared Access Signature) som beviljar läsbehörighet för behållaren, eller ange åtkomstbehörighet för behållaren som ger offentlig åtkomst.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Ingen

## UTDATA

### Microsoft.Azure.Commands.Batkap. Models.PSResourceFile

## ANTECKNINGAR

## RELATERADE LÄNKAR

[New-AzBatchTask](./New-AzBatchTask.md)