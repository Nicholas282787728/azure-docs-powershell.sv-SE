---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: ba8131ba496d51ba5597995e24f873fe2e186435
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263472"
---
# <span data-ttu-id="282af-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="282af-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="282af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="282af-102">SYNOPSIS</span></span>
<span data-ttu-id="282af-103">Startar för att kopiera en blob.</span><span class="sxs-lookup"><span data-stu-id="282af-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="282af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="282af-104">SYNTAX</span></span>

### <span data-ttu-id="282af-105">ContainerName (standard)</span><span class="sxs-lookup"><span data-stu-id="282af-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="282af-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="282af-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="282af-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="282af-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="282af-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="282af-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="282af-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="282af-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="282af-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="282af-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="282af-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="282af-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="282af-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="282af-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="282af-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="282af-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="282af-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="282af-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="282af-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="282af-115">DESCRIPTION</span></span>
<span data-ttu-id="282af-116">Cmdleten **Start-AzStorageBlobCopy** börjar kopiera en blob.</span><span class="sxs-lookup"><span data-stu-id="282af-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="282af-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="282af-117">EXAMPLES</span></span>

### <span data-ttu-id="282af-118">Exempel 1: kopiera en namngiven BLOB</span><span class="sxs-lookup"><span data-stu-id="282af-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="282af-119">Det här kommandot startar kopieringen av blobben med namnet ContosoPlanning2015 från behållaren ContosoUploads till behållaren ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="282af-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="282af-120">Exempel 2: Hämta en behållare för att ange blobs att kopiera</span><span class="sxs-lookup"><span data-stu-id="282af-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="282af-121">Det här kommandot hämtar behållaren med namnet ContosoUploads med cmdleten **Get-AzStorageContainer** och överför sedan behållaren till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="282af-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="282af-122">Denna cmdlet startar kopieringen av blobben med namnet ContosoPlanning2015.</span><span class="sxs-lookup"><span data-stu-id="282af-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="282af-123">Föregående cmdlet tillhandahåller käll behållaren.</span><span class="sxs-lookup"><span data-stu-id="282af-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="282af-124">Parametern *DestContainer* anger ContosoArchives som mål behållare.</span><span class="sxs-lookup"><span data-stu-id="282af-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="282af-125">Exempel 3: Hämta alla blobbar i en behållare och kopiera dem</span><span class="sxs-lookup"><span data-stu-id="282af-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="282af-126">Det här kommandot hämtar blobben i behållaren med namnet ContosoUploads med cmdleten **Get-AzStorageBlob** och skickar sedan resultaten till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="282af-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="282af-127">Denna cmdlet startar kopieringen av blobben till behållaren med namnet ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="282af-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="282af-128">Exempel 4: kopiera en blob som angetts som ett objekt</span><span class="sxs-lookup"><span data-stu-id="282af-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="282af-129">Det första kommandot får blobben med namnet ContosoPlanning2015 i behållaren med namnet ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="282af-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="282af-130">Kommandot lagrar objektet i $SrcBlob variabel.</span><span class="sxs-lookup"><span data-stu-id="282af-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="282af-131">Det andra kommandot hämtar blobben med namnet ContosoPlanning2015Archived i behållaren med namnet ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="282af-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="282af-132">Kommandot lagrar objektet i $DestBlob variabel.</span><span class="sxs-lookup"><span data-stu-id="282af-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="282af-133">Med kommandot senaste startas kopieringen från käll behållaren till mål behållaren.</span><span class="sxs-lookup"><span data-stu-id="282af-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="282af-134">Kommandot använder standard punkt notation för att ange **ICloudBlob** -objekten för $SrcBlob-och $DestBlob-blob.</span><span class="sxs-lookup"><span data-stu-id="282af-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="282af-135">Exempel 5: kopiera en BLOB från en URI</span><span class="sxs-lookup"><span data-stu-id="282af-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="282af-136">Det här kommandot skapar en kontext för kontot med namnet ContosoGeneral som använder den angivna tangenten och lagrar sedan den tangenten i $Context variabel.</span><span class="sxs-lookup"><span data-stu-id="282af-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="282af-137">Det andra kommandot kopierar filen från angiven URI till blobben med namnet ContosoPlanning i behållaren med namnet ContosoArchive.</span><span class="sxs-lookup"><span data-stu-id="282af-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="282af-138">Kommandot startar kopieringen till mål kontexten som lagras i $Context.</span><span class="sxs-lookup"><span data-stu-id="282af-138">The command starts the copy operation to the destination context stored in $Context.</span></span>
<span data-ttu-id="282af-139">Det finns ingen käll lagrings kontext så käll-URI: n måste ha åtkomst till källobjektet.</span><span class="sxs-lookup"><span data-stu-id="282af-139">There are no source storage context, so the source Uri must have access to the source object.</span></span> <span data-ttu-id="282af-140">Till exempel: om källan är en NONE-offentlig Azure-Blob bör URI: n innehålla SAS-token som har Läs åtkomst till blobben.</span><span class="sxs-lookup"><span data-stu-id="282af-140">E.g: if the source is a none public Azure blob, the Uri should contain SAS token which has read access to the blob.</span></span>

### <span data-ttu-id="282af-141">Exempel 6: kopiera en Block-Blob till en mål container med ett nytt BLOB-namn och ange StandardBlobTier som varmt, RehydratePriority som hög</span><span class="sxs-lookup"><span data-stu-id="282af-141">Example 6: Copy a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Hot -RehydratePriority High
```

<span data-ttu-id="282af-142">Det här kommandot startar kopieringen av en Block-Blob till mål container med ett nytt BLOB-namn och anger mål-BLOB-StandardBlobTier som het, RehydratePriority som hög</span><span class="sxs-lookup"><span data-stu-id="282af-142">This command starts the copy operation of a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>

## <span data-ttu-id="282af-143">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="282af-143">PARAMETERS</span></span>

### <span data-ttu-id="282af-144">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="282af-144">-AbsoluteUri</span></span>
<span data-ttu-id="282af-145">Anger den absoluta URI: n för en fil som ska kopieras till en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="282af-145">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="282af-146">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="282af-146">-BlobBaseClient</span></span>
<span data-ttu-id="282af-147">BlobBaseClient-objekt</span><span class="sxs-lookup"><span data-stu-id="282af-147">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="282af-148">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="282af-148">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="282af-149">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="282af-149">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="282af-150">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="282af-150">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="282af-151">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="282af-151">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="282af-152">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="282af-152">-CloudBlob</span></span>
<span data-ttu-id="282af-153">Anger ett **CloudBlob** -objekt från ett Azure Storage-bibliotek.</span><span class="sxs-lookup"><span data-stu-id="282af-153">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="282af-154">För att hämta ett **CloudBlob** -objekt, Använd cmdleten Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="282af-154">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="282af-155">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="282af-155">-CloudBlobContainer</span></span>
<span data-ttu-id="282af-156">Anger ett **CloudBlobContainer** -objekt från klient bibliotek för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="282af-156">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="282af-157">Denna cmdlet kopierar en BLOB från den behållare som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="282af-157">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="282af-158">För att hämta ett **CloudBlobContainer** -objekt, Använd cmdleten Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="282af-158">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="282af-159">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="282af-159">-ConcurrentTaskCount</span></span>
<span data-ttu-id="282af-160">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="282af-160">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="282af-161">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="282af-161">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="282af-162">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="282af-162">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="282af-163">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="282af-163">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="282af-164">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="282af-164">The default value is 10.</span></span>

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

### <span data-ttu-id="282af-165">-Kontext</span><span class="sxs-lookup"><span data-stu-id="282af-165">-Context</span></span>
<span data-ttu-id="282af-166">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="282af-166">Specifies an Azure storage context.</span></span>
<span data-ttu-id="282af-167">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="282af-167">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, FileInstanceToBlobInstance
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="282af-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="282af-168">-DefaultProfile</span></span>
<span data-ttu-id="282af-169">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="282af-169">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="282af-170">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="282af-170">-DestBlob</span></span>
<span data-ttu-id="282af-171">Anger namnet på mål-bloben.</span><span class="sxs-lookup"><span data-stu-id="282af-171">Specifies the name of the destination blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="282af-172">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="282af-172">-DestCloudBlob</span></span>
<span data-ttu-id="282af-173">Anger ett mål **CloudBlob** -objekt</span><span class="sxs-lookup"><span data-stu-id="282af-173">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="282af-174">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="282af-174">-DestContainer</span></span>
<span data-ttu-id="282af-175">Anger namnet på mål behållaren.</span><span class="sxs-lookup"><span data-stu-id="282af-175">Specifies the name of the destination container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="282af-176">-DestContext</span><span class="sxs-lookup"><span data-stu-id="282af-176">-DestContext</span></span>
<span data-ttu-id="282af-177">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="282af-177">Specifies an Azure storage context.</span></span>
<span data-ttu-id="282af-178">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="282af-178">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="282af-179">-Force</span><span class="sxs-lookup"><span data-stu-id="282af-179">-Force</span></span>
<span data-ttu-id="282af-180">Anger att denna cmdlet skriver över mål-BLOB utan att be dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="282af-180">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="282af-181">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="282af-181">-PremiumPageBlobTier</span></span>
<span data-ttu-id="282af-182">Premie sidans BLOB-nivå</span><span class="sxs-lookup"><span data-stu-id="282af-182">Premium Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60, P70, P80

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="282af-183">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="282af-183">-RehydratePriority</span></span>
<span data-ttu-id="282af-184">Blockera BLOB-RehydratePriority.</span><span class="sxs-lookup"><span data-stu-id="282af-184">Block Blob RehydratePriority.</span></span> <span data-ttu-id="282af-185">Anger den prioritet som en arkiverad BLOB ska rehydratiseras med.</span><span class="sxs-lookup"><span data-stu-id="282af-185">Indicates the priority with which to rehydrate an archived blob.</span></span> <span data-ttu-id="282af-186">Giltiga värden är High/standard.</span><span class="sxs-lookup"><span data-stu-id="282af-186">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:
Accepted values: Standard, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="282af-187">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="282af-187">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="282af-188">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="282af-188">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="282af-189">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="282af-189">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="282af-190">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="282af-190">-SrcBlob</span></span>
<span data-ttu-id="282af-191">Anger namnet på käll-blob.</span><span class="sxs-lookup"><span data-stu-id="282af-191">Specifies the name of the source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="282af-192">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="282af-192">-SrcContainer</span></span>
<span data-ttu-id="282af-193">Anger namnet på käll behållaren.</span><span class="sxs-lookup"><span data-stu-id="282af-193">Specifies the name of the source container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="282af-194">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="282af-194">-SrcDir</span></span>
<span data-ttu-id="282af-195">Anger ett **CloudFileDirectory** -objekt från ett Azure Storage-bibliotek.</span><span class="sxs-lookup"><span data-stu-id="282af-195">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="282af-196">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="282af-196">-SrcFile</span></span>
<span data-ttu-id="282af-197">Anger ett **CloudFile** -objekt från ett Azure Storage-bibliotek.</span><span class="sxs-lookup"><span data-stu-id="282af-197">Specifies a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="282af-198">Du kan skapa det eller använda Get-AzStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="282af-198">You can create it or use Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="282af-199">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="282af-199">-SrcFilePath</span></span>
<span data-ttu-id="282af-200">Anger den relativa sökvägen till käll katalogen eller käll resursen.</span><span class="sxs-lookup"><span data-stu-id="282af-200">Specifies the source file relative path of source directory or source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance, DirInstance
Aliases: SourceFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="282af-201">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="282af-201">-SrcShare</span></span>
<span data-ttu-id="282af-202">Anger ett **CloudFileShare** -objekt från ett Azure Storage-bibliotek.</span><span class="sxs-lookup"><span data-stu-id="282af-202">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="282af-203">Du kan skapa det eller använda Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="282af-203">You can create it or use Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="282af-204">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="282af-204">-SrcShareName</span></span>
<span data-ttu-id="282af-205">Anger namnet på käll resursen.</span><span class="sxs-lookup"><span data-stu-id="282af-205">Specifies the source share name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: SourceShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="282af-206">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="282af-206">-StandardBlobTier</span></span>
<span data-ttu-id="282af-207">Block Blob Tier, giltiga värden är varm/coolt/arkiverat.</span><span class="sxs-lookup"><span data-stu-id="282af-207">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="282af-208">Se detalj i https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="282af-208">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool, Archive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="282af-209">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="282af-209">-Confirm</span></span>
<span data-ttu-id="282af-210">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="282af-210">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="282af-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="282af-211">-WhatIf</span></span>
<span data-ttu-id="282af-212">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="282af-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="282af-213">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="282af-213">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="282af-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="282af-214">CommonParameters</span></span>
<span data-ttu-id="282af-215">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="282af-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="282af-216">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="282af-216">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="282af-217">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="282af-217">INPUTS</span></span>

### <span data-ttu-id="282af-218">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="282af-218">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="282af-219">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="282af-219">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="282af-220">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="282af-220">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="282af-221">System. String</span><span class="sxs-lookup"><span data-stu-id="282af-221">System.String</span></span>

### <span data-ttu-id="282af-222">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="282af-222">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="282af-223">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="282af-223">OUTPUTS</span></span>

### <span data-ttu-id="282af-224">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="282af-224">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="282af-225">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="282af-225">NOTES</span></span>

## <span data-ttu-id="282af-226">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="282af-226">RELATED LINKS</span></span>

[<span data-ttu-id="282af-227">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="282af-227">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="282af-228">Stopp-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="282af-228">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)
