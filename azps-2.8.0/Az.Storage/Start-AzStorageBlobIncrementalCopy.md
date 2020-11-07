---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobincrementalcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
ms.openlocfilehash: cbd108d884f229b8148ef83506e656e56de10149
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920791"
---
# <span data-ttu-id="b55f9-101">Start-AzStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="b55f9-101">Start-AzStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="b55f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b55f9-102">SYNOPSIS</span></span>
<span data-ttu-id="b55f9-103">Starta en stegvis kopiering från en sid-BLOB-ögonblicksbild till den angivna mål sid-blob.</span><span class="sxs-lookup"><span data-stu-id="b55f9-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="b55f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b55f9-104">SYNTAX</span></span>

### <span data-ttu-id="b55f9-105">ContainerInstance (standard)</span><span class="sxs-lookup"><span data-stu-id="b55f9-105">ContainerInstance (Default)</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b55f9-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="b55f9-106">BlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b55f9-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="b55f9-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b55f9-108">Hålla</span><span class="sxs-lookup"><span data-stu-id="b55f9-108">ContainerName</span></span>
```
Start-AzStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b55f9-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="b55f9-109">UriPipeline</span></span>
```
Start-AzStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b55f9-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b55f9-110">DESCRIPTION</span></span>
<span data-ttu-id="b55f9-111">Starta en stegvis kopiering från en sid-BLOB-ögonblicksbild till den angivna mål sid-blob.</span><span class="sxs-lookup"><span data-stu-id="b55f9-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="b55f9-112">Mer information om funktionen finns i https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="b55f9-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="b55f9-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b55f9-113">EXAMPLES</span></span>

### <span data-ttu-id="b55f9-114">Exempel 1: starta stegvis kopiering per BLOB-namn och ögonblicks bild</span><span class="sxs-lookup"><span data-stu-id="b55f9-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="b55f9-115">Det här kommandot startar stegvis kopiering per BLOB-namn och ögonblicks bild</span><span class="sxs-lookup"><span data-stu-id="b55f9-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="b55f9-116">Exempel 2: starta stegvis kopiering med käll-URI</span><span class="sxs-lookup"><span data-stu-id="b55f9-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="b55f9-117">Det här kommandot startar stegvis kopiering med käll-URI</span><span class="sxs-lookup"><span data-stu-id="b55f9-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="b55f9-118">Exempel 3: starta stegvis kopiering med behållar ledning från GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b55f9-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzStorageContainer -Container container1 | Start-AzStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="b55f9-119">Det här kommandot startar stegvis kopiering med hjälp av container pipeline från GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b55f9-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="b55f9-120">Exempel 4: starta stegvis kopiering från CloudPageBlob-objekt till mål-BLOB med blobb namn</span><span class="sxs-lookup"><span data-stu-id="b55f9-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="b55f9-121">Det här kommandot startar stegvis kopiering från CloudPageBlob-objekt till mål-BLOB med blobb namn</span><span class="sxs-lookup"><span data-stu-id="b55f9-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="b55f9-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b55f9-122">PARAMETERS</span></span>

### <span data-ttu-id="b55f9-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="b55f9-123">-AbsoluteUri</span></span>
<span data-ttu-id="b55f9-124">Absolut URI till källan.</span><span class="sxs-lookup"><span data-stu-id="b55f9-124">Absolute Uri to the source.</span></span> <span data-ttu-id="b55f9-125">Observera att autentiseringsuppgiften bör tillhandahållas i URI: n om källan kräver något.</span><span class="sxs-lookup"><span data-stu-id="b55f9-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

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

### <span data-ttu-id="b55f9-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b55f9-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b55f9-127">Maximalt utförda klient sidan för varje begäran i sekunder.</span><span class="sxs-lookup"><span data-stu-id="b55f9-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="b55f9-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b55f9-128">-CloudBlob</span></span>
<span data-ttu-id="b55f9-129">CloudBlob-objekt från klient bibliotek för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="b55f9-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="b55f9-130">Du kan skapa det eller använda Get-AzStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b55f9-130">You can create it or use Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="b55f9-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b55f9-131">-CloudBlobContainer</span></span>
<span data-ttu-id="b55f9-132">CloudBlobContainer-objekt från klient bibliotek för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="b55f9-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="b55f9-133">Du kan skapa det eller använda Get-AzStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b55f9-133">You can create it or use Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="b55f9-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b55f9-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b55f9-135">Totalt antal samtidiga asynkrona uppgifter.</span><span class="sxs-lookup"><span data-stu-id="b55f9-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="b55f9-136">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="b55f9-136">The default value is 10.</span></span>

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

### <span data-ttu-id="b55f9-137">-Kontext</span><span class="sxs-lookup"><span data-stu-id="b55f9-137">-Context</span></span>
<span data-ttu-id="b55f9-138">Käll Azure-lagringsplatsen.</span><span class="sxs-lookup"><span data-stu-id="b55f9-138">Source Azure Storage Context.</span></span> <span data-ttu-id="b55f9-139">Du kan skapa den via New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b55f9-139">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b55f9-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b55f9-140">-DefaultProfile</span></span>
<span data-ttu-id="b55f9-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b55f9-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b55f9-142">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="b55f9-142">-DestBlob</span></span>
<span data-ttu-id="b55f9-143">Mål-BLOB-namn</span><span class="sxs-lookup"><span data-stu-id="b55f9-143">Destination blob name</span></span>

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

### <span data-ttu-id="b55f9-144">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="b55f9-144">-DestCloudBlob</span></span>
<span data-ttu-id="b55f9-145">Mål CloudBlob-objekt</span><span class="sxs-lookup"><span data-stu-id="b55f9-145">Destination CloudBlob object</span></span>

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

### <span data-ttu-id="b55f9-146">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="b55f9-146">-DestContainer</span></span>
<span data-ttu-id="b55f9-147">Namn på mål behållare</span><span class="sxs-lookup"><span data-stu-id="b55f9-147">Destination container name</span></span>

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

### <span data-ttu-id="b55f9-148">-DestContext</span><span class="sxs-lookup"><span data-stu-id="b55f9-148">-DestContext</span></span>
<span data-ttu-id="b55f9-149">Mål Azure-lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="b55f9-149">Destination Azure Storage Context.</span></span> <span data-ttu-id="b55f9-150">Du kan skapa den via New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b55f9-150">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b55f9-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b55f9-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b55f9-152">Timeout för varje begäran i sekunder.</span><span class="sxs-lookup"><span data-stu-id="b55f9-152">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="b55f9-153">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="b55f9-153">-SrcBlob</span></span>
<span data-ttu-id="b55f9-154">Käll sidans BLOB-namn.</span><span class="sxs-lookup"><span data-stu-id="b55f9-154">Source page blob name.</span></span>

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

### <span data-ttu-id="b55f9-155">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="b55f9-155">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="b55f9-156">Ögonblicks bild av BLOB för källan.</span><span class="sxs-lookup"><span data-stu-id="b55f9-156">Source page blob snapshot time.</span></span>

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

### <span data-ttu-id="b55f9-157">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="b55f9-157">-SrcContainer</span></span>
<span data-ttu-id="b55f9-158">Namn på käll behållare</span><span class="sxs-lookup"><span data-stu-id="b55f9-158">Source Container name</span></span>

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

### <span data-ttu-id="b55f9-159">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b55f9-159">-Confirm</span></span>
<span data-ttu-id="b55f9-160">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b55f9-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b55f9-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b55f9-161">-WhatIf</span></span>
<span data-ttu-id="b55f9-162">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b55f9-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b55f9-163">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b55f9-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b55f9-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b55f9-164">CommonParameters</span></span>
<span data-ttu-id="b55f9-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b55f9-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b55f9-166">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b55f9-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b55f9-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b55f9-167">INPUTS</span></span>

### <span data-ttu-id="b55f9-168">Microsoft. Azure. Storage. blob. CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="b55f9-168">Microsoft.Azure.Storage.Blob.CloudPageBlob</span></span>

### <span data-ttu-id="b55f9-169">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b55f9-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="b55f9-170">System. String</span><span class="sxs-lookup"><span data-stu-id="b55f9-170">System.String</span></span>

### <span data-ttu-id="b55f9-171">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b55f9-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b55f9-172">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b55f9-172">OUTPUTS</span></span>

### <span data-ttu-id="b55f9-173">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b55f9-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="b55f9-174">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b55f9-174">NOTES</span></span>

## <span data-ttu-id="b55f9-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b55f9-175">RELATED LINKS</span></span>
