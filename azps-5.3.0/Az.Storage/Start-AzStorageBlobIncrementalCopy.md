---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobincrementalcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
ms.openlocfilehash: 126d89ca600c9696a1300054c2dc82cb1d9f5d2a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419968"
---
# <span data-ttu-id="4bdd5-101">Start-AzStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="4bdd5-101">Start-AzStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="4bdd5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4bdd5-102">SYNOPSIS</span></span>
<span data-ttu-id="4bdd5-103">Starta en stegvis kopiering från en sid-BLOB-ögonblicksbild till den angivna mål sid-blob.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="4bdd5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4bdd5-104">SYNTAX</span></span>

### <span data-ttu-id="4bdd5-105">ContainerInstance (standard)</span><span class="sxs-lookup"><span data-stu-id="4bdd5-105">ContainerInstance (Default)</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bdd5-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="4bdd5-106">BlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bdd5-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="4bdd5-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bdd5-108">Hålla</span><span class="sxs-lookup"><span data-stu-id="4bdd5-108">ContainerName</span></span>
```
Start-AzStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bdd5-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="4bdd5-109">UriPipeline</span></span>
```
Start-AzStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bdd5-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4bdd5-110">DESCRIPTION</span></span>
<span data-ttu-id="4bdd5-111">Starta en stegvis kopiering från en sid-BLOB-ögonblicksbild till den angivna mål sid-blob.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="4bdd5-112">Mer information om funktionen finns i https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="4bdd5-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="4bdd5-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-113">EXAMPLES</span></span>

### <span data-ttu-id="4bdd5-114">Exempel 1: starta stegvis kopiering per BLOB-namn och ögonblicks bild</span><span class="sxs-lookup"><span data-stu-id="4bdd5-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="4bdd5-115">Det här kommandot startar stegvis kopiering per BLOB-namn och ögonblicks bild</span><span class="sxs-lookup"><span data-stu-id="4bdd5-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="4bdd5-116">Exempel 2: starta stegvis kopiering med käll-URI</span><span class="sxs-lookup"><span data-stu-id="4bdd5-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="4bdd5-117">Det här kommandot startar stegvis kopiering med käll-URI</span><span class="sxs-lookup"><span data-stu-id="4bdd5-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="4bdd5-118">Exempel 3: starta stegvis kopiering med behållar ledning från GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4bdd5-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzStorageContainer -Container container1 | Start-AzStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="4bdd5-119">Det här kommandot startar stegvis kopiering med hjälp av container pipeline från GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4bdd5-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="4bdd5-120">Exempel 4: starta stegvis kopiering från CloudPageBlob-objekt till mål-BLOB med blobb namn</span><span class="sxs-lookup"><span data-stu-id="4bdd5-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="4bdd5-121">Det här kommandot startar stegvis kopiering från CloudPageBlob-objekt till mål-BLOB med blobb namn</span><span class="sxs-lookup"><span data-stu-id="4bdd5-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="4bdd5-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4bdd5-122">PARAMETERS</span></span>

### <span data-ttu-id="4bdd5-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="4bdd5-123">-AbsoluteUri</span></span>
<span data-ttu-id="4bdd5-124">Absolut URI till källan.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-124">Absolute Uri to the source.</span></span> <span data-ttu-id="4bdd5-125">Observera att autentiseringsuppgiften bör tillhandahållas i URI: n om källan kräver något.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

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

### <span data-ttu-id="4bdd5-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4bdd5-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4bdd5-127">Maximalt utförda klient sidan för varje begäran i sekunder.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="4bdd5-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="4bdd5-128">-CloudBlob</span></span>
<span data-ttu-id="4bdd5-129">CloudBlob-objekt från klient bibliotek för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="4bdd5-130">Du kan skapa det eller använda Get-AzStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-130">You can create it or use Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bdd5-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="4bdd5-131">-CloudBlobContainer</span></span>
<span data-ttu-id="4bdd5-132">CloudBlobContainer-objekt från klient bibliotek för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="4bdd5-133">Du kan skapa det eller använda Get-AzStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-133">You can create it or use Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="4bdd5-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4bdd5-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4bdd5-135">Totalt antal samtidiga asynkrona uppgifter.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="4bdd5-136">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-136">The default value is 10.</span></span>

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

### <span data-ttu-id="4bdd5-137">-Kontext</span><span class="sxs-lookup"><span data-stu-id="4bdd5-137">-Context</span></span>
<span data-ttu-id="4bdd5-138">Käll Azure-lagringsplatsen.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-138">Source Azure Storage Context.</span></span> <span data-ttu-id="4bdd5-139">Du kan skapa den via New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-139">You can create it by New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerInstance, BlobInstance, BlobInstanceToBlobInstance, ContainerName
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

### <span data-ttu-id="4bdd5-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bdd5-140">-DefaultProfile</span></span>
<span data-ttu-id="4bdd5-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bdd5-142">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="4bdd5-142">-DestBlob</span></span>
<span data-ttu-id="4bdd5-143">Mål-BLOB-namn</span><span class="sxs-lookup"><span data-stu-id="4bdd5-143">Destination blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName
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

### <span data-ttu-id="4bdd5-144">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="4bdd5-144">-DestCloudBlob</span></span>
<span data-ttu-id="4bdd5-145">Mål CloudBlob-objekt</span><span class="sxs-lookup"><span data-stu-id="4bdd5-145">Destination CloudBlob object</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bdd5-146">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="4bdd5-146">-DestContainer</span></span>
<span data-ttu-id="4bdd5-147">Namn på mål behållare</span><span class="sxs-lookup"><span data-stu-id="4bdd5-147">Destination container name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bdd5-148">-DestContext</span><span class="sxs-lookup"><span data-stu-id="4bdd5-148">-DestContext</span></span>
<span data-ttu-id="4bdd5-149">Mål Azure-lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-149">Destination Azure Storage Context.</span></span> <span data-ttu-id="4bdd5-150">Du kan skapa den via New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-150">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4bdd5-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4bdd5-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4bdd5-152">Timeout för varje begäran i sekunder.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-152">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="4bdd5-153">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="4bdd5-153">-SrcBlob</span></span>
<span data-ttu-id="4bdd5-154">Käll sidans BLOB-namn.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-154">Source page blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bdd5-155">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="4bdd5-155">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="4bdd5-156">Ögonblicks bild av BLOB för källan.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-156">Source page blob snapshot time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlobSnapshotTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bdd5-157">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="4bdd5-157">-SrcContainer</span></span>
<span data-ttu-id="4bdd5-158">Namn på käll behållare</span><span class="sxs-lookup"><span data-stu-id="4bdd5-158">Source Container name</span></span>

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

### <span data-ttu-id="4bdd5-159">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4bdd5-159">-Confirm</span></span>
<span data-ttu-id="4bdd5-160">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bdd5-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bdd5-161">-WhatIf</span></span>
<span data-ttu-id="4bdd5-162">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bdd5-163">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bdd5-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bdd5-164">CommonParameters</span></span>
<span data-ttu-id="4bdd5-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bdd5-166">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bdd5-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bdd5-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-167">INPUTS</span></span>

### <span data-ttu-id="4bdd5-168">Microsoft. Azure. Storage. blob. CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="4bdd5-168">Microsoft.Azure.Storage.Blob.CloudPageBlob</span></span>

### <span data-ttu-id="4bdd5-169">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="4bdd5-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="4bdd5-170">System. String</span><span class="sxs-lookup"><span data-stu-id="4bdd5-170">System.String</span></span>

### <span data-ttu-id="4bdd5-171">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4bdd5-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4bdd5-172">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4bdd5-172">OUTPUTS</span></span>

### <span data-ttu-id="4bdd5-173">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="4bdd5-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="4bdd5-174">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4bdd5-174">NOTES</span></span>

## <span data-ttu-id="4bdd5-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4bdd5-175">RELATED LINKS</span></span>
