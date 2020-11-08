---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271364"
---
# <span data-ttu-id="e795d-101">New-AzBatchResourceFile</span><span class="sxs-lookup"><span data-stu-id="e795d-101">New-AzBatchResourceFile</span></span>

## <span data-ttu-id="e795d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e795d-102">SYNOPSIS</span></span>
<span data-ttu-id="e795d-103">Skapar en resurs fil för användning med `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="e795d-103">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="e795d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e795d-104">SYNTAX</span></span>

### <span data-ttu-id="e795d-105">HttpUrl (standard)</span><span class="sxs-lookup"><span data-stu-id="e795d-105">HttpUrl (Default)</span></span>
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e795d-106">StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="e795d-106">StorageContainerUrl</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e795d-107">AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="e795d-107">AutoStorageContainerName</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e795d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e795d-108">DESCRIPTION</span></span>
<span data-ttu-id="e795d-109">Skapar en resurs fil för användning med `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="e795d-109">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="e795d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e795d-110">EXAMPLES</span></span>

### <span data-ttu-id="e795d-111">Exempel 1: skapa en resurs fil från en HTTP-URL som pekar på en enda fil</span><span class="sxs-lookup"><span data-stu-id="e795d-111">Example 1: Create a resource file from an HTTP URL pointing at a single file</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="e795d-112">Skapar en `PSResourceFile` referens till en HTTP-URL.</span><span class="sxs-lookup"><span data-stu-id="e795d-112">Creates a `PSResourceFile` referencing an HTTP url.</span></span>

### <span data-ttu-id="e795d-113">Exempel 2: skapa en resurs fil från en URL för en Azure-lagringsenhet</span><span class="sxs-lookup"><span data-stu-id="e795d-113">Example 2: Create a resource file from an Azure Storage container URL</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="e795d-114">Skapar en `PSResourceFile` referens till en Azure Storage container-URL.</span><span class="sxs-lookup"><span data-stu-id="e795d-114">Creates a `PSResourceFile` referencing an Azure Storage container URL.</span></span> <span data-ttu-id="e795d-115">Alla filer i behållaren hämtas till den angivna mappen.</span><span class="sxs-lookup"><span data-stu-id="e795d-115">All files in the container will be downloaded to the specified folder.</span></span>

### <span data-ttu-id="e795d-116">Exempel 3: skapa en resurs fil från ett namn på en behållare för automatisk lagring</span><span class="sxs-lookup"><span data-stu-id="e795d-116">Example 3: Create a resource file from an Auto Storage container name</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="e795d-117">Skapar ett `PSResourceFile` referens namn för en automatisk lagrings behållare.</span><span class="sxs-lookup"><span data-stu-id="e795d-117">Creates a `PSResourceFile` referencing an Auto Storage container name.</span></span> <span data-ttu-id="e795d-118">Alla filer i behållaren hämtas till den angivna mappen.</span><span class="sxs-lookup"><span data-stu-id="e795d-118">All files in the container will be downloaded to the specified folder.</span></span>

## <span data-ttu-id="e795d-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e795d-119">PARAMETERS</span></span>

### <span data-ttu-id="e795d-120">-AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="e795d-120">-AutoStorageContainerName</span></span>
<span data-ttu-id="e795d-121">Namnet på lagrings behållaren i det automatiska lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="e795d-121">The storage container name in the auto storage account.</span></span>

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

### <span data-ttu-id="e795d-122">-BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="e795d-122">-BlobPrefix</span></span>
<span data-ttu-id="e795d-123">Hämtar BLOB-prefixet som ska användas vid nedladdning av BLOB från en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="e795d-123">Gets the blob prefix to use when downloading blobs from an Azure Storage container.</span></span>
<span data-ttu-id="e795d-124">Endast blobbar vars namn börjar med det angivna prefixet hämtas.</span><span class="sxs-lookup"><span data-stu-id="e795d-124">Only the blobs whose names begin with the specified prefix will be downloaded.</span></span>
<span data-ttu-id="e795d-125">Detta prefix kan vara ett delvis fil namn eller en under katalog.</span><span class="sxs-lookup"><span data-stu-id="e795d-125">This prefix can be a partial filename or a subdirectory.</span></span>
<span data-ttu-id="e795d-126">Om ett prefix inte anges hämtas alla filer i behållaren.</span><span class="sxs-lookup"><span data-stu-id="e795d-126">If a prefix is not specified, all the files in the container will be downloaded.</span></span>

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

### <span data-ttu-id="e795d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e795d-127">-DefaultProfile</span></span>
<span data-ttu-id="e795d-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e795d-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e795d-129">-FileMode</span><span class="sxs-lookup"><span data-stu-id="e795d-129">-FileMode</span></span>
<span data-ttu-id="e795d-130">Hämtar attributet för fil behörighets läge i det oktala formatet.</span><span class="sxs-lookup"><span data-stu-id="e795d-130">Gets the file permission mode attribute in octal format.</span></span>
<span data-ttu-id="e795d-131">Den här egenskapen är endast tillämplig om resurs filen laddas ned till en Linux-nod.</span><span class="sxs-lookup"><span data-stu-id="e795d-131">This property is applicable only if the resource file is downloaded to a Linux node.</span></span>
<span data-ttu-id="e795d-132">Om den här egenskapen inte anges för en Linux-nod är standardvärdet 0770.</span><span class="sxs-lookup"><span data-stu-id="e795d-132">If this property is not specified for a Linux node, then the default value is 0770.</span></span>

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

### <span data-ttu-id="e795d-133">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="e795d-133">-FilePath</span></span>
<span data-ttu-id="e795d-134">Den plats på noden Compute dit du vill ladda ned filen/filerna i förhållande till aktivitetens arbets katalog.</span><span class="sxs-lookup"><span data-stu-id="e795d-134">The location on the compute node to which to download the file(s), relative to the task's working directory.</span></span> <span data-ttu-id="e795d-135">Om parametern HttpUrl är angiven är fil Sök vägen obligatorisk och beskriver sökvägen som filen hämtas till, inklusive fil namnet.</span><span class="sxs-lookup"><span data-stu-id="e795d-135">If the HttpUrl parameter is specified, the FilePath is required and describes the path which the file will be downloaded to, including the filename.</span></span> <span data-ttu-id="e795d-136">I annat fall är filsökväg valfri och är den katalog som du vill ladda ned filerna till om du har angett parametrarna AutoStorageContainerName eller StorageContainerUrl.</span><span class="sxs-lookup"><span data-stu-id="e795d-136">Otherwise, if the AutoStorageContainerName or StorageContainerUrl parameters are specified, FilePath is optional and is the directory to download the files to.</span></span> <span data-ttu-id="e795d-137">I de fall då sökvägen används som katalog sparas alla katalog strukturer som redan är kopplade till indata och läggs till i den angivna katalogen för katalog tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e795d-137">In the case where FilePath is used as a directory, any directory structure already associated with the input data will be retained in full and appended to the specified FilePath directory.</span></span> <span data-ttu-id="e795d-138">Den angivna relativa sökvägen kan inte ta slut i aktivitetens arbets katalog (till exempel genom att använda "..").</span><span class="sxs-lookup"><span data-stu-id="e795d-138">The specified relative path cannot break out of the task's working directory (for example by using '..').</span></span>

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

### <span data-ttu-id="e795d-139">-HttpUrl</span><span class="sxs-lookup"><span data-stu-id="e795d-139">-HttpUrl</span></span>
<span data-ttu-id="e795d-140">URL-adressen till filen som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="e795d-140">The URL of the file to download.</span></span>
<span data-ttu-id="e795d-141">Om URL-adressen är Azure-Blob-lagring måste den vara läsbar med anonym åtkomst. Det innebär att kommando tjänsten inte visar några autentiseringsuppgifter när blobben laddas ner.</span><span class="sxs-lookup"><span data-stu-id="e795d-141">If the URL is Azure Blob Storage, it must be readable using anonymous access; that is, the Batch service does not present any credentials when downloading the blob.</span></span>
<span data-ttu-id="e795d-142">Det finns två sätt att skaffa en sådan URL för en BLOB i Azure-lagring: inkludera en delad Access-signatur (SAS) bevilja Läs behörigheter för blobben, eller ange ACL för blobben eller dess behållare för att tillåta offentlig åtkomst.</span><span class="sxs-lookup"><span data-stu-id="e795d-142">There are two ways to get such a URL for a blob in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the blob, or set the ACL for the blob or its container to allow public access.</span></span>

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

### <span data-ttu-id="e795d-143">-StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="e795d-143">-StorageContainerUrl</span></span>
<span data-ttu-id="e795d-144">URL-adressen för BLOB-behållaren i Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="e795d-144">The URL of the blob container within Azure Blob Storage.</span></span>
<span data-ttu-id="e795d-145">Denna URL måste vara läsbar och kan listas med anonym åtkomst. Det innebär att kommando tjänsten inte visar några autentiseringsuppgifter när du laddar ned blobbar från behållaren.</span><span class="sxs-lookup"><span data-stu-id="e795d-145">This URL must be readable and listable using anonymous access; that is, the Batch service does not present any credentials when downloading blobs from the container.</span></span>
<span data-ttu-id="e795d-146">Det finns två sätt att hämta en URL-adress för en behållare i Azure-lagring: inkludera en delad Access-signatur (SAS) bevilja Läs behörigheter för behållaren, eller ange ACL för behållaren för att tillåta offentlig åtkomst.</span><span class="sxs-lookup"><span data-stu-id="e795d-146">There are two ways to get such a URL for a container in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the container, or set the ACL for the container to allow public access.</span></span>

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

### <span data-ttu-id="e795d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e795d-147">CommonParameters</span></span>
<span data-ttu-id="e795d-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e795d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e795d-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e795d-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e795d-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e795d-150">INPUTS</span></span>

### <span data-ttu-id="e795d-151">Ingen</span><span class="sxs-lookup"><span data-stu-id="e795d-151">None</span></span>

## <span data-ttu-id="e795d-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e795d-152">OUTPUTS</span></span>

### <span data-ttu-id="e795d-153">Microsoft.Azure.Commands.BatCH. Modeller. PSResourceFile</span><span class="sxs-lookup"><span data-stu-id="e795d-153">Microsoft.Azure.Commands.Batch.Models.PSResourceFile</span></span>

## <span data-ttu-id="e795d-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e795d-154">NOTES</span></span>

## <span data-ttu-id="e795d-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e795d-155">RELATED LINKS</span></span>

[<span data-ttu-id="e795d-156">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="e795d-156">New-AzBatchTask</span></span>](./New-AzBatchTask.md)