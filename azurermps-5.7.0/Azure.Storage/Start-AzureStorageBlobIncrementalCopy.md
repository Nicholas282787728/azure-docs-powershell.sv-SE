---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/start-azurestorageblobincrementalcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageBlobIncrementalCopy.md
ms.openlocfilehash: 8b33a964109bae2770a0ac6a7d668c7fa365c62b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758241"
---
# <span data-ttu-id="09850-101">Start-AzureStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="09850-101">Start-AzureStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="09850-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09850-102">SYNOPSIS</span></span>
<span data-ttu-id="09850-103">Starta en stegvis kopiering från en sid-BLOB-ögonblicksbild till den angivna mål sid-blob.</span><span class="sxs-lookup"><span data-stu-id="09850-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09850-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09850-104">SYNTAX</span></span>

### <span data-ttu-id="09850-105">ContainerInstance (standard)</span><span class="sxs-lookup"><span data-stu-id="09850-105">ContainerInstance (Default)</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09850-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="09850-106">BlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09850-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="09850-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09850-108">Hålla</span><span class="sxs-lookup"><span data-stu-id="09850-108">ContainerName</span></span>
```
Start-AzureStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09850-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="09850-109">UriPipeline</span></span>
```
Start-AzureStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09850-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09850-110">DESCRIPTION</span></span>
<span data-ttu-id="09850-111">Starta en stegvis kopiering från en sid-BLOB-ögonblicksbild till den angivna mål sid-blob.</span><span class="sxs-lookup"><span data-stu-id="09850-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="09850-112">Mer information om funktionen finns i https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="09850-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="09850-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09850-113">EXAMPLES</span></span>

### <span data-ttu-id="09850-114">Exempel 1: starta stegvis kopiering per BLOB-namn och ögonblicks bild</span><span class="sxs-lookup"><span data-stu-id="09850-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="09850-115">Det här kommandot startar stegvis kopiering per BLOB-namn och ögonblicks bild</span><span class="sxs-lookup"><span data-stu-id="09850-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="09850-116">Exempel 2: starta stegvis kopiering med käll-URI</span><span class="sxs-lookup"><span data-stu-id="09850-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="09850-117">Det här kommandot startar stegvis kopiering med käll-URI</span><span class="sxs-lookup"><span data-stu-id="09850-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="09850-118">Exempel 3: starta stegvis kopiering med behållar ledning från GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="09850-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzureStorageContainer -Container container1 | Start-AzureStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="09850-119">Det här kommandot startar stegvis kopiering med hjälp av container pipeline från GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="09850-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="09850-120">Exempel 4: starta stegvis kopiering från CloudPageBlob-objekt till mål-BLOB med blobb namn</span><span class="sxs-lookup"><span data-stu-id="09850-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzureStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzureStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="09850-121">Det här kommandot startar stegvis kopiering från CloudPageBlob-objekt till mål-BLOB med blobb namn</span><span class="sxs-lookup"><span data-stu-id="09850-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="09850-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09850-122">PARAMETERS</span></span>

### <span data-ttu-id="09850-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="09850-123">-AbsoluteUri</span></span>
<span data-ttu-id="09850-124">Absolut URI till källan.</span><span class="sxs-lookup"><span data-stu-id="09850-124">Absolute Uri to the source.</span></span> <span data-ttu-id="09850-125">Observera att autentiseringsuppgiften bör tillhandahållas i URI: n om källan kräver något.</span><span class="sxs-lookup"><span data-stu-id="09850-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

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

### <span data-ttu-id="09850-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="09850-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="09850-127">Maximalt utförda klient sidan för varje begäran i sekunder.</span><span class="sxs-lookup"><span data-stu-id="09850-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="09850-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="09850-128">-CloudBlob</span></span>
<span data-ttu-id="09850-129">CloudBlob-objekt från klient bibliotek för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="09850-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="09850-130">Du kan skapa det eller använda Get-AzureStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09850-130">You can create it or use Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09850-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="09850-131">-CloudBlobContainer</span></span>
<span data-ttu-id="09850-132">CloudBlobContainer-objekt från klient bibliotek för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="09850-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="09850-133">Du kan skapa det eller använda Get-AzureStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09850-133">You can create it or use Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="09850-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="09850-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="09850-135">Totalt antal samtidiga asynkrona uppgifter.</span><span class="sxs-lookup"><span data-stu-id="09850-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="09850-136">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="09850-136">The default value is 10.</span></span>

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

### <span data-ttu-id="09850-137">-Kontext</span><span class="sxs-lookup"><span data-stu-id="09850-137">-Context</span></span>
<span data-ttu-id="09850-138">Käll Azure-lagringsplatsen.</span><span class="sxs-lookup"><span data-stu-id="09850-138">Source Azure Storage Context.</span></span> <span data-ttu-id="09850-139">Du kan skapa den via New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09850-139">You can create it by New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerInstance, BlobInstance, BlobInstanceToBlobInstance, ContainerName
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

### <span data-ttu-id="09850-140">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="09850-140">-DestBlob</span></span>
<span data-ttu-id="09850-141">Mål-BLOB-namn</span><span class="sxs-lookup"><span data-stu-id="09850-141">Destination blob name</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName
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

### <span data-ttu-id="09850-142">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="09850-142">-DestCloudBlob</span></span>
<span data-ttu-id="09850-143">Mål CloudBlob-objekt</span><span class="sxs-lookup"><span data-stu-id="09850-143">Destination CloudBlob object</span></span>

```yaml
Type: CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09850-144">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="09850-144">-DestContainer</span></span>
<span data-ttu-id="09850-145">Namn på mål behållare</span><span class="sxs-lookup"><span data-stu-id="09850-145">Destination container name</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09850-146">-DestContext</span><span class="sxs-lookup"><span data-stu-id="09850-146">-DestContext</span></span>
<span data-ttu-id="09850-147">Mål Azure-lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="09850-147">Destination Azure Storage Context.</span></span> <span data-ttu-id="09850-148">Du kan skapa den via New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09850-148">You can create it by New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="09850-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="09850-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="09850-150">Timeout för varje begäran i sekunder.</span><span class="sxs-lookup"><span data-stu-id="09850-150">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="09850-151">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="09850-151">-SrcBlob</span></span>
<span data-ttu-id="09850-152">Käll sidans BLOB-namn.</span><span class="sxs-lookup"><span data-stu-id="09850-152">Source page blob name.</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09850-153">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="09850-153">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="09850-154">Ögonblicks bild av BLOB för källan.</span><span class="sxs-lookup"><span data-stu-id="09850-154">Source page blob snapshot time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlobSnapshotTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09850-155">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="09850-155">-SrcContainer</span></span>
<span data-ttu-id="09850-156">Namn på käll behållare</span><span class="sxs-lookup"><span data-stu-id="09850-156">Source Container name</span></span>

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

### <span data-ttu-id="09850-157">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="09850-157">-Confirm</span></span>
<span data-ttu-id="09850-158">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="09850-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09850-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09850-159">-WhatIf</span></span>
<span data-ttu-id="09850-160">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="09850-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09850-161">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="09850-161">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09850-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09850-162">CommonParameters</span></span>
<span data-ttu-id="09850-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09850-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09850-164">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09850-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09850-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09850-165">INPUTS</span></span>

### <span data-ttu-id="09850-166">Microsoft. WindowsAzure. Storage. blob. CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="09850-166">Microsoft.WindowsAzure.Storage.Blob.CloudPageBlob</span></span>
<span data-ttu-id="09850-167">Microsoft. WindowsAzure. Storage. blob. CloudBlobContainer system. String Microsoft. WindowsAzure. commands. Common. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="09850-167">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer System.String Microsoft.WindowsAzure.Commands.Common.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="09850-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09850-168">OUTPUTS</span></span>

### <span data-ttu-id="09850-169">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="09850-169">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="09850-170">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09850-170">NOTES</span></span>

## <span data-ttu-id="09850-171">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09850-171">RELATED LINKS</span></span>

