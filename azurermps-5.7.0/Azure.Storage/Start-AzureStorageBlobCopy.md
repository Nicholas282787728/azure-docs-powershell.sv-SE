---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/start-azurestorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageBlobCopy.md
ms.openlocfilehash: 054aa003752c27849c44eb00654313c395c255ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756828"
---
# <span data-ttu-id="11f67-101">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="11f67-101">Start-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="11f67-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11f67-102">SYNOPSIS</span></span>
<span data-ttu-id="11f67-103">Startar för att kopiera en blob.</span><span class="sxs-lookup"><span data-stu-id="11f67-103">Starts to copy a blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11f67-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11f67-104">SYNTAX</span></span>

### <span data-ttu-id="11f67-105">ContainerName (standard)</span><span class="sxs-lookup"><span data-stu-id="11f67-105">ContainerName (Default)</span></span>
```
Start-AzureStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11f67-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="11f67-106">BlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11f67-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="11f67-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11f67-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="11f67-108">ContainerInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11f67-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="11f67-109">ShareName</span></span>
```
Start-AzureStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11f67-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="11f67-110">ShareInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11f67-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="11f67-111">DirInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11f67-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="11f67-112">FileInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11f67-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="11f67-113">FileInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11f67-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="11f67-114">UriPipeline</span></span>
```
Start-AzureStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11f67-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11f67-115">DESCRIPTION</span></span>
<span data-ttu-id="11f67-116">Cmdleten **Start-AzureStorageBlobCopy** börjar kopiera en blob.</span><span class="sxs-lookup"><span data-stu-id="11f67-116">The **Start-AzureStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="11f67-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11f67-117">EXAMPLES</span></span>

### <span data-ttu-id="11f67-118">Exempel 1: kopiera en namngiven BLOB</span><span class="sxs-lookup"><span data-stu-id="11f67-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="11f67-119">Det här kommandot startar kopieringen av blobben med namnet ContosoPlanning2015 från behållaren ContosoUploads till behållaren ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="11f67-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="11f67-120">Exempel 2: Hämta en behållare för att ange blobs att kopiera</span><span class="sxs-lookup"><span data-stu-id="11f67-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="11f67-121">Det här kommandot hämtar behållaren med namnet ContosoUploads med cmdleten **Get-AzureStorageContainer** och överför sedan behållaren till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="11f67-121">This command gets the container named ContosoUploads, by using the **Get-AzureStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="11f67-122">Denna cmdlet startar kopieringen av blobben med namnet ContosoPlanning2015.</span><span class="sxs-lookup"><span data-stu-id="11f67-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="11f67-123">Föregående cmdlet tillhandahåller käll behållaren.</span><span class="sxs-lookup"><span data-stu-id="11f67-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="11f67-124">Parametern *DestContainer* anger ContosoArchives som mål behållare.</span><span class="sxs-lookup"><span data-stu-id="11f67-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="11f67-125">Exempel 3: Hämta alla blobbar i en behållare och kopiera dem</span><span class="sxs-lookup"><span data-stu-id="11f67-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzureStorageBlob -Container "ContosoUploads" | Start-AzureStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="11f67-126">Det här kommandot hämtar blobben i behållaren med namnet ContosoUploads med cmdleten **Get-AzureStorageBlob** och skickar sedan resultaten till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="11f67-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzureStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="11f67-127">Denna cmdlet startar kopieringen av blobben till behållaren med namnet ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="11f67-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="11f67-128">Exempel 4: kopiera en blob som angetts som ett objekt</span><span class="sxs-lookup"><span data-stu-id="11f67-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzureStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzureStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzureStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="11f67-129">Det första kommandot får blobben med namnet ContosoPlanning2015 i behållaren med namnet ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="11f67-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="11f67-130">Kommandot lagrar objektet i $SrcBlob variabel.</span><span class="sxs-lookup"><span data-stu-id="11f67-130">The command stores that object in the $SrcBlob variable.</span></span>

<span data-ttu-id="11f67-131">Det andra kommandot hämtar blobben med namnet ContosoPlanning2015Archived i behållaren med namnet ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="11f67-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="11f67-132">Kommandot lagrar objektet i $DestBlob variabel.</span><span class="sxs-lookup"><span data-stu-id="11f67-132">The command stores that object in the $DestBlob variable.</span></span>

<span data-ttu-id="11f67-133">Med kommandot senaste startas kopieringen från käll behållaren till mål behållaren.</span><span class="sxs-lookup"><span data-stu-id="11f67-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="11f67-134">Kommandot använder standard punkt notation för att ange **ICloudBlob** -objekten för $SrcBlob-och $DestBlob-blob.</span><span class="sxs-lookup"><span data-stu-id="11f67-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="11f67-135">Exempel 5: kopiera en BLOB från en URI</span><span class="sxs-lookup"><span data-stu-id="11f67-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzureStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="11f67-136">Det här kommandot skapar en kontext för kontot med namnet ContosoGeneral som använder den angivna tangenten och lagrar sedan den tangenten i $Context variabel.</span><span class="sxs-lookup"><span data-stu-id="11f67-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>

<span data-ttu-id="11f67-137">Det andra kommandot kopierar filen från angiven URI till blobben med namnet ContosoPlanning i behållaren med namnet ContosoArchive.</span><span class="sxs-lookup"><span data-stu-id="11f67-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="11f67-138">Kommandot startar kopieringen i kontexten som lagras i $Context.</span><span class="sxs-lookup"><span data-stu-id="11f67-138">The command starts the copy operation in the context stored in $Context.</span></span>

## <span data-ttu-id="11f67-139">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11f67-139">PARAMETERS</span></span>

### <span data-ttu-id="11f67-140">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="11f67-140">-AbsoluteUri</span></span>
<span data-ttu-id="11f67-141">Anger den absoluta URI: n för en fil som ska kopieras till en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="11f67-141">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f67-142">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="11f67-142">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="11f67-143">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="11f67-143">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="11f67-144">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="11f67-144">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="11f67-145">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="11f67-145">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="11f67-146">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="11f67-146">-CloudBlob</span></span>
<span data-ttu-id="11f67-147">Anger ett **CloudBlob** -objekt från ett Azure Storage-bibliotek.</span><span class="sxs-lookup"><span data-stu-id="11f67-147">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="11f67-148">För att hämta ett **CloudBlob** -objekt, Använd cmdleten Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="11f67-148">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11f67-149">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="11f67-149">-CloudBlobContainer</span></span>
<span data-ttu-id="11f67-150">Anger ett **CloudBlobContainer** -objekt från klient bibliotek för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="11f67-150">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="11f67-151">Denna cmdlet kopierar en BLOB från den behållare som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="11f67-151">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="11f67-152">För att hämta ett **CloudBlobContainer** -objekt, Använd cmdleten Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="11f67-152">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f67-153">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="11f67-153">-ConcurrentTaskCount</span></span>
<span data-ttu-id="11f67-154">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="11f67-154">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="11f67-155">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="11f67-155">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="11f67-156">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="11f67-156">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="11f67-157">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="11f67-157">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="11f67-158">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="11f67-158">The default value is 10.</span></span>

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

### <span data-ttu-id="11f67-159">-Kontext</span><span class="sxs-lookup"><span data-stu-id="11f67-159">-Context</span></span>
<span data-ttu-id="11f67-160">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="11f67-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="11f67-161">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="11f67-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, FileInstanceToBlobInstance
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11f67-162">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="11f67-162">-DestBlob</span></span>
<span data-ttu-id="11f67-163">Anger namnet på mål-bloben.</span><span class="sxs-lookup"><span data-stu-id="11f67-163">Specifies the name of the destination blob.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f67-164">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="11f67-164">-DestCloudBlob</span></span>
<span data-ttu-id="11f67-165">Anger ett mål **CloudBlob** -objekt</span><span class="sxs-lookup"><span data-stu-id="11f67-165">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f67-166">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="11f67-166">-DestContainer</span></span>
<span data-ttu-id="11f67-167">Anger namnet på mål behållaren.</span><span class="sxs-lookup"><span data-stu-id="11f67-167">Specifies the name of the destination container.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f67-168">-DestContext</span><span class="sxs-lookup"><span data-stu-id="11f67-168">-DestContext</span></span>
<span data-ttu-id="11f67-169">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="11f67-169">Specifies an Azure storage context.</span></span>
<span data-ttu-id="11f67-170">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="11f67-170">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f67-171">-Force</span><span class="sxs-lookup"><span data-stu-id="11f67-171">-Force</span></span>
<span data-ttu-id="11f67-172">Anger att denna cmdlet skriver över mål-BLOB utan att be dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="11f67-172">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="11f67-173">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="11f67-173">-PremiumPageBlobTier</span></span>
<span data-ttu-id="11f67-174">Premie sidans BLOB-nivå</span><span class="sxs-lookup"><span data-stu-id="11f67-174">Premium Page Blob Tier</span></span>

```yaml
Type: PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f67-175">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="11f67-175">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="11f67-176">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="11f67-176">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="11f67-177">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="11f67-177">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="11f67-178">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="11f67-178">-SrcBlob</span></span>
<span data-ttu-id="11f67-179">Anger namnet på käll-blob.</span><span class="sxs-lookup"><span data-stu-id="11f67-179">Specifies the name of the source blob.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, ContainerInstance
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f67-180">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="11f67-180">-SrcContainer</span></span>
<span data-ttu-id="11f67-181">Anger namnet på käll behållaren.</span><span class="sxs-lookup"><span data-stu-id="11f67-181">Specifies the name of the source container.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f67-182">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="11f67-182">-SrcDir</span></span>
<span data-ttu-id="11f67-183">Anger ett **CloudFileDirectory** -objekt från ett Azure Storage-bibliotek.</span><span class="sxs-lookup"><span data-stu-id="11f67-183">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f67-184">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="11f67-184">-SrcFile</span></span>
<span data-ttu-id="11f67-185">Specifes ett **CloudFile** -objekt från ett Azure Storage-bibliotek.</span><span class="sxs-lookup"><span data-stu-id="11f67-185">Specifes a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="11f67-186">Du kan skapa det eller använda Get-AzureStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11f67-186">You can create it or use Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11f67-187">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="11f67-187">-SrcFilePath</span></span>
<span data-ttu-id="11f67-188">Anger den relativa sökvägen till käll katalogen eller käll resursen.</span><span class="sxs-lookup"><span data-stu-id="11f67-188">Specifies the source file relative path of source directory or source share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, ShareInstance, DirInstance
Aliases: SourceFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f67-189">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="11f67-189">-SrcShare</span></span>
<span data-ttu-id="11f67-190">Anger ett **CloudFileShare** -objekt från ett Azure Storage-bibliotek.</span><span class="sxs-lookup"><span data-stu-id="11f67-190">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="11f67-191">Du kan skapa det eller använda Get-AzureStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11f67-191">You can create it or use Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f67-192">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="11f67-192">-SrcShareName</span></span>
<span data-ttu-id="11f67-193">Anger namnet på käll resursen.</span><span class="sxs-lookup"><span data-stu-id="11f67-193">Specifies the source share name.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: SourceShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f67-194">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="11f67-194">-Confirm</span></span>
<span data-ttu-id="11f67-195">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="11f67-195">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f67-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11f67-196">-WhatIf</span></span>
<span data-ttu-id="11f67-197">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="11f67-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11f67-198">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="11f67-198">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f67-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11f67-199">CommonParameters</span></span>
<span data-ttu-id="11f67-200">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11f67-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11f67-201">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11f67-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11f67-202">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11f67-202">INPUTS</span></span>

### <span data-ttu-id="11f67-203">CloudBlob</span><span class="sxs-lookup"><span data-stu-id="11f67-203">CloudBlob</span></span>

<span data-ttu-id="11f67-204">Parametern ' CloudBlob ' godkänner värdet av typen ' CloudBlob ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="11f67-204">Parameter 'CloudBlob' accepts value of type 'CloudBlob' from the pipeline</span></span>

### <span data-ttu-id="11f67-205">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="11f67-205">IStorageContext</span></span>

<span data-ttu-id="11f67-206">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="11f67-206">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="11f67-207">CloudFile</span><span class="sxs-lookup"><span data-stu-id="11f67-207">CloudFile</span></span>

<span data-ttu-id="11f67-208">Parametern ' SrcFile ' godkänner värdet av typen ' CloudFile ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="11f67-208">Parameter 'SrcFile' accepts value of type 'CloudFile' from the pipeline</span></span>

## <span data-ttu-id="11f67-209">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11f67-209">OUTPUTS</span></span>

### <span data-ttu-id="11f67-210">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="11f67-210">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="11f67-211">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11f67-211">NOTES</span></span>

## <span data-ttu-id="11f67-212">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11f67-212">RELATED LINKS</span></span>

[<span data-ttu-id="11f67-213">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="11f67-213">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)

[<span data-ttu-id="11f67-214">Stopp-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="11f67-214">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)
