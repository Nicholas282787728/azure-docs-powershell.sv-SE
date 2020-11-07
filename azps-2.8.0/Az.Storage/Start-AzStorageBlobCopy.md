---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: a990b168fcaf32deffd495b5eeb0f9a813f2f093
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920246"
---
# <span data-ttu-id="367a7-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="367a7-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="367a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="367a7-102">SYNOPSIS</span></span>
<span data-ttu-id="367a7-103">Startar för att kopiera en blob.</span><span class="sxs-lookup"><span data-stu-id="367a7-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="367a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="367a7-104">SYNTAX</span></span>

### <span data-ttu-id="367a7-105">ContainerName (standard)</span><span class="sxs-lookup"><span data-stu-id="367a7-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="367a7-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="367a7-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="367a7-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="367a7-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="367a7-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="367a7-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="367a7-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="367a7-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="367a7-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="367a7-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="367a7-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="367a7-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="367a7-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="367a7-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="367a7-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="367a7-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="367a7-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="367a7-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="367a7-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="367a7-115">DESCRIPTION</span></span>
<span data-ttu-id="367a7-116">Cmdleten **Start-AzStorageBlobCopy** börjar kopiera en blob.</span><span class="sxs-lookup"><span data-stu-id="367a7-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="367a7-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="367a7-117">EXAMPLES</span></span>

### <span data-ttu-id="367a7-118">Exempel 1: kopiera en namngiven BLOB</span><span class="sxs-lookup"><span data-stu-id="367a7-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="367a7-119">Det här kommandot startar kopieringen av blobben med namnet ContosoPlanning2015 från behållaren ContosoUploads till behållaren ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="367a7-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="367a7-120">Exempel 2: Hämta en behållare för att ange blobs att kopiera</span><span class="sxs-lookup"><span data-stu-id="367a7-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="367a7-121">Det här kommandot hämtar behållaren med namnet ContosoUploads med cmdleten **Get-AzStorageContainer** och överför sedan behållaren till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="367a7-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="367a7-122">Denna cmdlet startar kopieringen av blobben med namnet ContosoPlanning2015.</span><span class="sxs-lookup"><span data-stu-id="367a7-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="367a7-123">Föregående cmdlet tillhandahåller käll behållaren.</span><span class="sxs-lookup"><span data-stu-id="367a7-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="367a7-124">Parametern *DestContainer* anger ContosoArchives som mål behållare.</span><span class="sxs-lookup"><span data-stu-id="367a7-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="367a7-125">Exempel 3: Hämta alla blobbar i en behållare och kopiera dem</span><span class="sxs-lookup"><span data-stu-id="367a7-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="367a7-126">Det här kommandot hämtar blobben i behållaren med namnet ContosoUploads med cmdleten **Get-AzStorageBlob** och skickar sedan resultaten till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="367a7-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="367a7-127">Denna cmdlet startar kopieringen av blobben till behållaren med namnet ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="367a7-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="367a7-128">Exempel 4: kopiera en blob som angetts som ett objekt</span><span class="sxs-lookup"><span data-stu-id="367a7-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="367a7-129">Det första kommandot får blobben med namnet ContosoPlanning2015 i behållaren med namnet ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="367a7-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="367a7-130">Kommandot lagrar objektet i $SrcBlob variabel.</span><span class="sxs-lookup"><span data-stu-id="367a7-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="367a7-131">Det andra kommandot hämtar blobben med namnet ContosoPlanning2015Archived i behållaren med namnet ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="367a7-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="367a7-132">Kommandot lagrar objektet i $DestBlob variabel.</span><span class="sxs-lookup"><span data-stu-id="367a7-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="367a7-133">Med kommandot senaste startas kopieringen från käll behållaren till mål behållaren.</span><span class="sxs-lookup"><span data-stu-id="367a7-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="367a7-134">Kommandot använder standard punkt notation för att ange **ICloudBlob** -objekten för $SrcBlob-och $DestBlob-blob.</span><span class="sxs-lookup"><span data-stu-id="367a7-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="367a7-135">Exempel 5: kopiera en BLOB från en URI</span><span class="sxs-lookup"><span data-stu-id="367a7-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="367a7-136">Det här kommandot skapar en kontext för kontot med namnet ContosoGeneral som använder den angivna tangenten och lagrar sedan den tangenten i $Context variabel.</span><span class="sxs-lookup"><span data-stu-id="367a7-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="367a7-137">Det andra kommandot kopierar filen från angiven URI till blobben med namnet ContosoPlanning i behållaren med namnet ContosoArchive.</span><span class="sxs-lookup"><span data-stu-id="367a7-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="367a7-138">Kommandot startar kopieringen i kontexten som lagras i $Context.</span><span class="sxs-lookup"><span data-stu-id="367a7-138">The command starts the copy operation in the context stored in $Context.</span></span>

### <span data-ttu-id="367a7-139">Exempel 6: kopiera en Block-Blob till en mål container med ett nytt BLOB-namn och ange StandardBlobTier som Arkiv, RehydratePriority som hög</span><span class="sxs-lookup"><span data-stu-id="367a7-139">Example 6: Copy a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Archive, RehydratePriority as High</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Archive
```

<span data-ttu-id="367a7-140">Det här kommandot startar kopieringen av en Block-Blob till mål container med ett nytt BLOB-namn och anger mål-BLOB-StandardBlobTier som Arkiv, RehydratePriority som hög</span><span class="sxs-lookup"><span data-stu-id="367a7-140">This command starts the copy operation of a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Archive, RehydratePriority as High</span></span>

## <span data-ttu-id="367a7-141">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="367a7-141">PARAMETERS</span></span>

### <span data-ttu-id="367a7-142">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="367a7-142">-AbsoluteUri</span></span>
<span data-ttu-id="367a7-143">Anger den absoluta URI: n för en fil som ska kopieras till en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="367a7-143">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="367a7-144">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="367a7-144">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="367a7-145">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="367a7-145">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="367a7-146">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="367a7-146">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="367a7-147">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="367a7-147">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="367a7-148">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="367a7-148">-CloudBlob</span></span>
<span data-ttu-id="367a7-149">Anger ett **CloudBlob** -objekt från ett Azure Storage-bibliotek.</span><span class="sxs-lookup"><span data-stu-id="367a7-149">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="367a7-150">För att hämta ett **CloudBlob** -objekt, Använd cmdleten Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="367a7-150">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="367a7-151">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="367a7-151">-CloudBlobContainer</span></span>
<span data-ttu-id="367a7-152">Anger ett **CloudBlobContainer** -objekt från klient bibliotek för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="367a7-152">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="367a7-153">Denna cmdlet kopierar en BLOB från den behållare som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="367a7-153">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="367a7-154">För att hämta ett **CloudBlobContainer** -objekt, Använd cmdleten Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="367a7-154">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="367a7-155">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="367a7-155">-ConcurrentTaskCount</span></span>
<span data-ttu-id="367a7-156">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="367a7-156">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="367a7-157">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="367a7-157">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="367a7-158">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="367a7-158">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="367a7-159">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="367a7-159">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="367a7-160">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="367a7-160">The default value is 10.</span></span>

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

### <span data-ttu-id="367a7-161">-Kontext</span><span class="sxs-lookup"><span data-stu-id="367a7-161">-Context</span></span>
<span data-ttu-id="367a7-162">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="367a7-162">Specifies an Azure storage context.</span></span>
<span data-ttu-id="367a7-163">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="367a7-163">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="367a7-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="367a7-164">-DefaultProfile</span></span>
<span data-ttu-id="367a7-165">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="367a7-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="367a7-166">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="367a7-166">-DestBlob</span></span>
<span data-ttu-id="367a7-167">Anger namnet på mål-bloben.</span><span class="sxs-lookup"><span data-stu-id="367a7-167">Specifies the name of the destination blob.</span></span>

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

### <span data-ttu-id="367a7-168">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="367a7-168">-DestCloudBlob</span></span>
<span data-ttu-id="367a7-169">Anger ett mål **CloudBlob** -objekt</span><span class="sxs-lookup"><span data-stu-id="367a7-169">Specifies a destination **CloudBlob** object</span></span>

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

### <span data-ttu-id="367a7-170">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="367a7-170">-DestContainer</span></span>
<span data-ttu-id="367a7-171">Anger namnet på mål behållaren.</span><span class="sxs-lookup"><span data-stu-id="367a7-171">Specifies the name of the destination container.</span></span>

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

### <span data-ttu-id="367a7-172">-DestContext</span><span class="sxs-lookup"><span data-stu-id="367a7-172">-DestContext</span></span>
<span data-ttu-id="367a7-173">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="367a7-173">Specifies an Azure storage context.</span></span>
<span data-ttu-id="367a7-174">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="367a7-174">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="367a7-175">-Force</span><span class="sxs-lookup"><span data-stu-id="367a7-175">-Force</span></span>
<span data-ttu-id="367a7-176">Anger att denna cmdlet skriver över mål-BLOB utan att be dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="367a7-176">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="367a7-177">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="367a7-177">-PremiumPageBlobTier</span></span>
<span data-ttu-id="367a7-178">Premie sidans BLOB-nivå</span><span class="sxs-lookup"><span data-stu-id="367a7-178">Premium Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="367a7-179">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="367a7-179">-RehydratePriority</span></span>
<span data-ttu-id="367a7-180">Blockera BLOB-RehydratePriority.</span><span class="sxs-lookup"><span data-stu-id="367a7-180">Block Blob RehydratePriority.</span></span> <span data-ttu-id="367a7-181">Anger den prioritet som en arkiverad BLOB ska rehydratiseras med.</span><span class="sxs-lookup"><span data-stu-id="367a7-181">Indicates the priority with which to rehydrate an archived blob.</span></span> <span data-ttu-id="367a7-182">Giltiga värden är High/standard.</span><span class="sxs-lookup"><span data-stu-id="367a7-182">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="367a7-183">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="367a7-183">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="367a7-184">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="367a7-184">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="367a7-185">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="367a7-185">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="367a7-186">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="367a7-186">-SrcBlob</span></span>
<span data-ttu-id="367a7-187">Anger namnet på käll-blob.</span><span class="sxs-lookup"><span data-stu-id="367a7-187">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="367a7-188">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="367a7-188">-SrcContainer</span></span>
<span data-ttu-id="367a7-189">Anger namnet på käll behållaren.</span><span class="sxs-lookup"><span data-stu-id="367a7-189">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="367a7-190">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="367a7-190">-SrcDir</span></span>
<span data-ttu-id="367a7-191">Anger ett **CloudFileDirectory** -objekt från ett Azure Storage-bibliotek.</span><span class="sxs-lookup"><span data-stu-id="367a7-191">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

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

### <span data-ttu-id="367a7-192">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="367a7-192">-SrcFile</span></span>
<span data-ttu-id="367a7-193">Anger ett **CloudFile** -objekt från ett Azure Storage-bibliotek.</span><span class="sxs-lookup"><span data-stu-id="367a7-193">Specifies a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="367a7-194">Du kan skapa det eller använda Get-AzStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="367a7-194">You can create it or use Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="367a7-195">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="367a7-195">-SrcFilePath</span></span>
<span data-ttu-id="367a7-196">Anger den relativa sökvägen till käll katalogen eller käll resursen.</span><span class="sxs-lookup"><span data-stu-id="367a7-196">Specifies the source file relative path of source directory or source share.</span></span>

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

### <span data-ttu-id="367a7-197">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="367a7-197">-SrcShare</span></span>
<span data-ttu-id="367a7-198">Anger ett **CloudFileShare** -objekt från ett Azure Storage-bibliotek.</span><span class="sxs-lookup"><span data-stu-id="367a7-198">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="367a7-199">Du kan skapa det eller använda Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="367a7-199">You can create it or use Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="367a7-200">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="367a7-200">-SrcShareName</span></span>
<span data-ttu-id="367a7-201">Anger namnet på käll resursen.</span><span class="sxs-lookup"><span data-stu-id="367a7-201">Specifies the source share name.</span></span>

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

### <span data-ttu-id="367a7-202">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="367a7-202">-StandardBlobTier</span></span>
<span data-ttu-id="367a7-203">Block Blob Tier, giltiga värden är varm/coolt/arkiverat.</span><span class="sxs-lookup"><span data-stu-id="367a7-203">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="367a7-204">Se detalj i https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="367a7-204">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="367a7-205">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="367a7-205">-Confirm</span></span>
<span data-ttu-id="367a7-206">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="367a7-206">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="367a7-207">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="367a7-207">-WhatIf</span></span>
<span data-ttu-id="367a7-208">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="367a7-208">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="367a7-209">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="367a7-209">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="367a7-210">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="367a7-210">CommonParameters</span></span>
<span data-ttu-id="367a7-211">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="367a7-211">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="367a7-212">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="367a7-212">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="367a7-213">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="367a7-213">INPUTS</span></span>

### <span data-ttu-id="367a7-214">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="367a7-214">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="367a7-215">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="367a7-215">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="367a7-216">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="367a7-216">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="367a7-217">System. String</span><span class="sxs-lookup"><span data-stu-id="367a7-217">System.String</span></span>

### <span data-ttu-id="367a7-218">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="367a7-218">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="367a7-219">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="367a7-219">OUTPUTS</span></span>

### <span data-ttu-id="367a7-220">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="367a7-220">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="367a7-221">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="367a7-221">NOTES</span></span>

## <span data-ttu-id="367a7-222">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="367a7-222">RELATED LINKS</span></span>

[<span data-ttu-id="367a7-223">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="367a7-223">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="367a7-224">Stopp-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="367a7-224">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)
