---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/start-azurestorageblobcopy
schema: 2.0.0
ms.openlocfilehash: 379e86e6f6e97e1e8d70b55d972076d540654cb8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931062"
---
# <span data-ttu-id="ff3fe-101">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ff3fe-101">Start-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="ff3fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff3fe-102">SYNOPSIS</span></span>
<span data-ttu-id="ff3fe-103">Startar för att kopiera en blob.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-103">Starts to copy a blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff3fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff3fe-104">SYNTAX</span></span>

### <span data-ttu-id="ff3fe-105">ContainerName (standard)</span><span class="sxs-lookup"><span data-stu-id="ff3fe-105">ContainerName (Default)</span></span>
```
Start-AzureStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff3fe-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="ff3fe-106">BlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff3fe-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="ff3fe-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff3fe-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ff3fe-108">ContainerInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff3fe-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="ff3fe-109">ShareName</span></span>
```
Start-AzureStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff3fe-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="ff3fe-110">ShareInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff3fe-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="ff3fe-111">DirInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff3fe-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="ff3fe-112">FileInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff3fe-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="ff3fe-113">FileInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff3fe-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="ff3fe-114">UriPipeline</span></span>
```
Start-AzureStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff3fe-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff3fe-115">DESCRIPTION</span></span>
<span data-ttu-id="ff3fe-116">Cmdleten **Start-AzureStorageBlobCopy** börjar kopiera en blob.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-116">The **Start-AzureStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="ff3fe-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff3fe-117">EXAMPLES</span></span>

### <span data-ttu-id="ff3fe-118">Exempel 1: kopiera en namngiven BLOB</span><span class="sxs-lookup"><span data-stu-id="ff3fe-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="ff3fe-119">Det här kommandot startar kopieringen av blobben med namnet ContosoPlanning2015 från behållaren ContosoUploads till behållaren ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="ff3fe-120">Exempel 2: Hämta en behållare för att ange blobs att kopiera</span><span class="sxs-lookup"><span data-stu-id="ff3fe-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="ff3fe-121">Det här kommandot hämtar behållaren med namnet ContosoUploads med cmdleten **Get-AzureStorageContainer** och överför sedan behållaren till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-121">This command gets the container named ContosoUploads, by using the **Get-AzureStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ff3fe-122">Denna cmdlet startar kopieringen av blobben med namnet ContosoPlanning2015.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="ff3fe-123">Föregående cmdlet tillhandahåller käll behållaren.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="ff3fe-124">Parametern *DestContainer* anger ContosoArchives som mål behållare.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="ff3fe-125">Exempel 3: Hämta alla blobbar i en behållare och kopiera dem</span><span class="sxs-lookup"><span data-stu-id="ff3fe-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzureStorageBlob -Container "ContosoUploads" | Start-AzureStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="ff3fe-126">Det här kommandot hämtar blobben i behållaren med namnet ContosoUploads med cmdleten **Get-AzureStorageBlob** och skickar sedan resultaten till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzureStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ff3fe-127">Denna cmdlet startar kopieringen av blobben till behållaren med namnet ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="ff3fe-128">Exempel 4: kopiera en blob som angetts som ett objekt</span><span class="sxs-lookup"><span data-stu-id="ff3fe-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzureStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzureStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzureStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="ff3fe-129">Det första kommandot får blobben med namnet ContosoPlanning2015 i behållaren med namnet ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="ff3fe-130">Kommandot lagrar objektet i $SrcBlob variabel.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="ff3fe-131">Det andra kommandot hämtar blobben med namnet ContosoPlanning2015Archived i behållaren med namnet ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="ff3fe-132">Kommandot lagrar objektet i $DestBlob variabel.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="ff3fe-133">Med kommandot senaste startas kopieringen från käll behållaren till mål behållaren.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="ff3fe-134">Kommandot använder standard punkt notation för att ange **ICloudBlob** -objekten för $SrcBlob-och $DestBlob-blob.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="ff3fe-135">Exempel 5: kopiera en BLOB från en URI</span><span class="sxs-lookup"><span data-stu-id="ff3fe-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzureStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="ff3fe-136">Det här kommandot skapar en kontext för kontot med namnet ContosoGeneral som använder den angivna tangenten och lagrar sedan den tangenten i $Context variabel.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="ff3fe-137">Det andra kommandot kopierar filen från angiven URI till blobben med namnet ContosoPlanning i behållaren med namnet ContosoArchive.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="ff3fe-138">Kommandot startar kopieringen i kontexten som lagras i $Context.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-138">The command starts the copy operation in the context stored in $Context.</span></span>

## <span data-ttu-id="ff3fe-139">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff3fe-139">PARAMETERS</span></span>

### <span data-ttu-id="ff3fe-140">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="ff3fe-140">-AbsoluteUri</span></span>
<span data-ttu-id="ff3fe-141">Anger den absoluta URI: n för en fil som ska kopieras till en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-141">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="ff3fe-142">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ff3fe-142">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ff3fe-143">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-143">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ff3fe-144">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-144">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ff3fe-145">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-145">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ff3fe-146">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ff3fe-146">-CloudBlob</span></span>
<span data-ttu-id="ff3fe-147">Anger ett **CloudBlob** -objekt från ett Azure Storage-bibliotek.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-147">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="ff3fe-148">För att hämta ett **CloudBlob** -objekt, Använd cmdleten Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-148">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff3fe-149">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ff3fe-149">-CloudBlobContainer</span></span>
<span data-ttu-id="ff3fe-150">Anger ett **CloudBlobContainer** -objekt från klient bibliotek för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-150">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="ff3fe-151">Denna cmdlet kopierar en BLOB från den behållare som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-151">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="ff3fe-152">För att hämta ett **CloudBlobContainer** -objekt, Använd cmdleten Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-152">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff3fe-153">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ff3fe-153">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ff3fe-154">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-154">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ff3fe-155">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-155">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ff3fe-156">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-156">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ff3fe-157">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-157">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ff3fe-158">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-158">The default value is 10.</span></span>

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

### <span data-ttu-id="ff3fe-159">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ff3fe-159">-Context</span></span>
<span data-ttu-id="ff3fe-160">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ff3fe-161">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ff3fe-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff3fe-162">-DefaultProfile</span></span>
<span data-ttu-id="ff3fe-163">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff3fe-164">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="ff3fe-164">-DestBlob</span></span>
<span data-ttu-id="ff3fe-165">Anger namnet på mål-bloben.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-165">Specifies the name of the destination blob.</span></span>

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

### <span data-ttu-id="ff3fe-166">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="ff3fe-166">-DestCloudBlob</span></span>
<span data-ttu-id="ff3fe-167">Anger ett mål **CloudBlob** -objekt</span><span class="sxs-lookup"><span data-stu-id="ff3fe-167">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff3fe-168">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="ff3fe-168">-DestContainer</span></span>
<span data-ttu-id="ff3fe-169">Anger namnet på mål behållaren.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-169">Specifies the name of the destination container.</span></span>

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

### <span data-ttu-id="ff3fe-170">-DestContext</span><span class="sxs-lookup"><span data-stu-id="ff3fe-170">-DestContext</span></span>
<span data-ttu-id="ff3fe-171">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-171">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ff3fe-172">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-172">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ff3fe-173">-Force</span><span class="sxs-lookup"><span data-stu-id="ff3fe-173">-Force</span></span>
<span data-ttu-id="ff3fe-174">Anger att denna cmdlet skriver över mål-BLOB utan att be dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-174">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="ff3fe-175">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="ff3fe-175">-PremiumPageBlobTier</span></span>
<span data-ttu-id="ff3fe-176">Premie sidans BLOB-nivå</span><span class="sxs-lookup"><span data-stu-id="ff3fe-176">Premium Page Blob Tier</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff3fe-177">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ff3fe-177">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ff3fe-178">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-178">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="ff3fe-179">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-179">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="ff3fe-180">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="ff3fe-180">-SrcBlob</span></span>
<span data-ttu-id="ff3fe-181">Anger namnet på käll-blob.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-181">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="ff3fe-182">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="ff3fe-182">-SrcContainer</span></span>
<span data-ttu-id="ff3fe-183">Anger namnet på käll behållaren.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-183">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="ff3fe-184">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="ff3fe-184">-SrcDir</span></span>
<span data-ttu-id="ff3fe-185">Anger ett **CloudFileDirectory** -objekt från ett Azure Storage-bibliotek.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-185">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff3fe-186">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="ff3fe-186">-SrcFile</span></span>
<span data-ttu-id="ff3fe-187">Specifes ett **CloudFile** -objekt från ett Azure Storage-bibliotek.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-187">Specifes a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="ff3fe-188">Du kan skapa det eller använda Get-AzureStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-188">You can create it or use Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff3fe-189">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="ff3fe-189">-SrcFilePath</span></span>
<span data-ttu-id="ff3fe-190">Anger den relativa sökvägen till käll katalogen eller käll resursen.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-190">Specifies the source file relative path of source directory or source share.</span></span>

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

### <span data-ttu-id="ff3fe-191">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="ff3fe-191">-SrcShare</span></span>
<span data-ttu-id="ff3fe-192">Anger ett **CloudFileShare** -objekt från ett Azure Storage-bibliotek.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-192">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="ff3fe-193">Du kan skapa det eller använda Get-AzureStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-193">You can create it or use Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff3fe-194">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="ff3fe-194">-SrcShareName</span></span>
<span data-ttu-id="ff3fe-195">Anger namnet på käll resursen.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-195">Specifies the source share name.</span></span>

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

### <span data-ttu-id="ff3fe-196">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ff3fe-196">-Confirm</span></span>
<span data-ttu-id="ff3fe-197">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff3fe-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff3fe-198">-WhatIf</span></span>
<span data-ttu-id="ff3fe-199">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-199">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff3fe-200">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff3fe-201">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff3fe-201">CommonParameters</span></span>
<span data-ttu-id="ff3fe-202">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff3fe-202">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff3fe-203">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff3fe-203">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff3fe-204">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff3fe-204">INPUTS</span></span>

### <span data-ttu-id="ff3fe-205">Microsoft. WindowsAzure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ff3fe-205">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="ff3fe-206">Microsoft. WindowsAzure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ff3fe-206">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="ff3fe-207">Microsoft. WindowsAzure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="ff3fe-207">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="ff3fe-208">Parametrar: SrcFile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ff3fe-208">Parameters: SrcFile (ByValue)</span></span>

### <span data-ttu-id="ff3fe-209">System. String</span><span class="sxs-lookup"><span data-stu-id="ff3fe-209">System.String</span></span>

### <span data-ttu-id="ff3fe-210">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ff3fe-210">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ff3fe-211">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff3fe-211">OUTPUTS</span></span>

### <span data-ttu-id="ff3fe-212">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ff3fe-212">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="ff3fe-213">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff3fe-213">NOTES</span></span>

## <span data-ttu-id="ff3fe-214">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff3fe-214">RELATED LINKS</span></span>

[<span data-ttu-id="ff3fe-215">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="ff3fe-215">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)

[<span data-ttu-id="ff3fe-216">Stopp-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ff3fe-216">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)
