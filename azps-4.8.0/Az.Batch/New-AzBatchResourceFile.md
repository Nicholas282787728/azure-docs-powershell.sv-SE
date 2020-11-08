---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260326"
---
# <span data-ttu-id="6fc86-101">New-AzBatchResourceFile</span><span class="sxs-lookup"><span data-stu-id="6fc86-101">New-AzBatchResourceFile</span></span>

## <span data-ttu-id="6fc86-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6fc86-102">SYNOPSIS</span></span>
<span data-ttu-id="6fc86-103">Skapar en resurs fil för användning med `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="6fc86-103">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="6fc86-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6fc86-104">SYNTAX</span></span>

### <span data-ttu-id="6fc86-105">HttpUrl (standard)</span><span class="sxs-lookup"><span data-stu-id="6fc86-105">HttpUrl (Default)</span></span>
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fc86-106">StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="6fc86-106">StorageContainerUrl</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fc86-107">AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="6fc86-107">AutoStorageContainerName</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fc86-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6fc86-108">DESCRIPTION</span></span>
<span data-ttu-id="6fc86-109">Skapar en resurs fil för användning med `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="6fc86-109">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="6fc86-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6fc86-110">EXAMPLES</span></span>

### <span data-ttu-id="6fc86-111">Exempel 1: skapa en resurs fil från en HTTP-URL som pekar på en enda fil</span><span class="sxs-lookup"><span data-stu-id="6fc86-111">Example 1: Create a resource file from an HTTP URL pointing at a single file</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="6fc86-112">Skapar en `PSResourceFile` referens till en HTTP-URL.</span><span class="sxs-lookup"><span data-stu-id="6fc86-112">Creates a `PSResourceFile` referencing an HTTP url.</span></span>

### <span data-ttu-id="6fc86-113">Exempel 2: skapa en resurs fil från en URL för en Azure-lagringsenhet</span><span class="sxs-lookup"><span data-stu-id="6fc86-113">Example 2: Create a resource file from an Azure Storage container URL</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="6fc86-114">Skapar en `PSResourceFile` referens till en Azure Storage container-URL.</span><span class="sxs-lookup"><span data-stu-id="6fc86-114">Creates a `PSResourceFile` referencing an Azure Storage container URL.</span></span> <span data-ttu-id="6fc86-115">Alla filer i behållaren hämtas till den angivna mappen.</span><span class="sxs-lookup"><span data-stu-id="6fc86-115">All files in the container will be downloaded to the specified folder.</span></span>

### <span data-ttu-id="6fc86-116">Exempel 3: skapa en resurs fil från ett namn på en behållare för automatisk lagring</span><span class="sxs-lookup"><span data-stu-id="6fc86-116">Example 3: Create a resource file from an Auto Storage container name</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="6fc86-117">Skapar ett `PSResourceFile` referens namn för en automatisk lagrings behållare.</span><span class="sxs-lookup"><span data-stu-id="6fc86-117">Creates a `PSResourceFile` referencing an Auto Storage container name.</span></span> <span data-ttu-id="6fc86-118">Alla filer i behållaren hämtas till den angivna mappen.</span><span class="sxs-lookup"><span data-stu-id="6fc86-118">All files in the container will be downloaded to the specified folder.</span></span>

## <span data-ttu-id="6fc86-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6fc86-119">PARAMETERS</span></span>

### <span data-ttu-id="6fc86-120">-AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="6fc86-120">-AutoStorageContainerName</span></span>
<span data-ttu-id="6fc86-121">Namnet på lagrings behållaren i det automatiska lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="6fc86-121">The storage container name in the auto storage account.</span></span>

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

### <span data-ttu-id="6fc86-122">-BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="6fc86-122">-BlobPrefix</span></span>
<span data-ttu-id="6fc86-123">Hämtar BLOB-prefixet som ska användas vid nedladdning av BLOB från en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="6fc86-123">Gets the blob prefix to use when downloading blobs from an Azure Storage container.</span></span>
<span data-ttu-id="6fc86-124">Endast blobbar vars namn börjar med det angivna prefixet hämtas.</span><span class="sxs-lookup"><span data-stu-id="6fc86-124">Only the blobs whose names begin with the specified prefix will be downloaded.</span></span>
<span data-ttu-id="6fc86-125">Detta prefix kan vara ett delvis fil namn eller en under katalog.</span><span class="sxs-lookup"><span data-stu-id="6fc86-125">This prefix can be a partial filename or a subdirectory.</span></span>
<span data-ttu-id="6fc86-126">Om ett prefix inte anges hämtas alla filer i behållaren.</span><span class="sxs-lookup"><span data-stu-id="6fc86-126">If a prefix is not specified, all the files in the container will be downloaded.</span></span>

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

### <span data-ttu-id="6fc86-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fc86-127">-DefaultProfile</span></span>
<span data-ttu-id="6fc86-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6fc86-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fc86-129">-FileMode</span><span class="sxs-lookup"><span data-stu-id="6fc86-129">-FileMode</span></span>
<span data-ttu-id="6fc86-130">Hämtar attributet för fil behörighets läge i det oktala formatet.</span><span class="sxs-lookup"><span data-stu-id="6fc86-130">Gets the file permission mode attribute in octal format.</span></span>
<span data-ttu-id="6fc86-131">Den här egenskapen är endast tillämplig om resurs filen laddas ned till en Linux-nod.</span><span class="sxs-lookup"><span data-stu-id="6fc86-131">This property is applicable only if the resource file is downloaded to a Linux node.</span></span>
<span data-ttu-id="6fc86-132">Om den här egenskapen inte anges för en Linux-nod är standardvärdet 0770.</span><span class="sxs-lookup"><span data-stu-id="6fc86-132">If this property is not specified for a Linux node, then the default value is 0770.</span></span>

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

### <span data-ttu-id="6fc86-133">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="6fc86-133">-FilePath</span></span>
<span data-ttu-id="6fc86-134">Den plats på noden Compute dit du vill ladda ned filen/filerna i förhållande till aktivitetens arbets katalog.</span><span class="sxs-lookup"><span data-stu-id="6fc86-134">The location on the compute node to which to download the file(s), relative to the task's working directory.</span></span> <span data-ttu-id="6fc86-135">Om parametern HttpUrl är angiven är fil Sök vägen obligatorisk och beskriver sökvägen som filen hämtas till, inklusive fil namnet.</span><span class="sxs-lookup"><span data-stu-id="6fc86-135">If the HttpUrl parameter is specified, the FilePath is required and describes the path which the file will be downloaded to, including the filename.</span></span> <span data-ttu-id="6fc86-136">I annat fall är filsökväg valfri och är den katalog som du vill ladda ned filerna till om du har angett parametrarna AutoStorageContainerName eller StorageContainerUrl.</span><span class="sxs-lookup"><span data-stu-id="6fc86-136">Otherwise, if the AutoStorageContainerName or StorageContainerUrl parameters are specified, FilePath is optional and is the directory to download the files to.</span></span> <span data-ttu-id="6fc86-137">I de fall då sökvägen används som katalog sparas alla katalog strukturer som redan är kopplade till indata och läggs till i den angivna katalogen för katalog tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6fc86-137">In the case where FilePath is used as a directory, any directory structure already associated with the input data will be retained in full and appended to the specified FilePath directory.</span></span> <span data-ttu-id="6fc86-138">Den angivna relativa sökvägen kan inte ta slut i aktivitetens arbets katalog (till exempel genom att använda "..").</span><span class="sxs-lookup"><span data-stu-id="6fc86-138">The specified relative path cannot break out of the task's working directory (for example by using '..').</span></span>

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

### <span data-ttu-id="6fc86-139">-HttpUrl</span><span class="sxs-lookup"><span data-stu-id="6fc86-139">-HttpUrl</span></span>
<span data-ttu-id="6fc86-140">URL-adressen till filen som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="6fc86-140">The URL of the file to download.</span></span>
<span data-ttu-id="6fc86-141">Om URL-adressen är Azure-Blob-lagring måste den vara läsbar med anonym åtkomst. Det innebär att kommando tjänsten inte visar några autentiseringsuppgifter när blobben laddas ner.</span><span class="sxs-lookup"><span data-stu-id="6fc86-141">If the URL is Azure Blob Storage, it must be readable using anonymous access; that is, the Batch service does not present any credentials when downloading the blob.</span></span>
<span data-ttu-id="6fc86-142">Det finns två sätt att skaffa en sådan URL för en BLOB i Azure-lagring: inkludera en delad Access-signatur (SAS) bevilja Läs behörigheter för blobben, eller ange ACL för blobben eller dess behållare för att tillåta offentlig åtkomst.</span><span class="sxs-lookup"><span data-stu-id="6fc86-142">There are two ways to get such a URL for a blob in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the blob, or set the ACL for the blob or its container to allow public access.</span></span>

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

### <span data-ttu-id="6fc86-143">-StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="6fc86-143">-StorageContainerUrl</span></span>
<span data-ttu-id="6fc86-144">URL-adressen för BLOB-behållaren i Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="6fc86-144">The URL of the blob container within Azure Blob Storage.</span></span>
<span data-ttu-id="6fc86-145">Denna URL måste vara läsbar och kan listas med anonym åtkomst. Det innebär att kommando tjänsten inte visar några autentiseringsuppgifter när du laddar ned blobbar från behållaren.</span><span class="sxs-lookup"><span data-stu-id="6fc86-145">This URL must be readable and listable using anonymous access; that is, the Batch service does not present any credentials when downloading blobs from the container.</span></span>
<span data-ttu-id="6fc86-146">Det finns två sätt att hämta en URL-adress för en behållare i Azure-lagring: inkludera en delad Access-signatur (SAS) bevilja Läs behörigheter för behållaren, eller ange ACL för behållaren för att tillåta offentlig åtkomst.</span><span class="sxs-lookup"><span data-stu-id="6fc86-146">There are two ways to get such a URL for a container in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the container, or set the ACL for the container to allow public access.</span></span>

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

### <span data-ttu-id="6fc86-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fc86-147">CommonParameters</span></span>
<span data-ttu-id="6fc86-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fc86-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fc86-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6fc86-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fc86-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6fc86-150">INPUTS</span></span>

### <span data-ttu-id="6fc86-151">Ingen</span><span class="sxs-lookup"><span data-stu-id="6fc86-151">None</span></span>

## <span data-ttu-id="6fc86-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6fc86-152">OUTPUTS</span></span>

### <span data-ttu-id="6fc86-153">Microsoft.Azure.Commands.BatCH. Modeller. PSResourceFile</span><span class="sxs-lookup"><span data-stu-id="6fc86-153">Microsoft.Azure.Commands.Batch.Models.PSResourceFile</span></span>

## <span data-ttu-id="6fc86-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6fc86-154">NOTES</span></span>

## <span data-ttu-id="6fc86-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6fc86-155">RELATED LINKS</span></span>

[<span data-ttu-id="6fc86-156">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6fc86-156">New-AzBatchTask</span></span>](./New-AzBatchTask.md)