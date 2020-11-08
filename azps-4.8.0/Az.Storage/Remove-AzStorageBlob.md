---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: 37ae4192e973d218bd0cb23f9ccba16367098d30
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100740"
---
# <span data-ttu-id="29912-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="29912-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="29912-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29912-102">SYNOPSIS</span></span>
<span data-ttu-id="29912-103">Tar bort angiven lagrings-blob.</span><span class="sxs-lookup"><span data-stu-id="29912-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="29912-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29912-104">SYNTAX</span></span>

### <span data-ttu-id="29912-105">NamePipeline (standard)</span><span class="sxs-lookup"><span data-stu-id="29912-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29912-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="29912-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29912-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="29912-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot]
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29912-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29912-108">DESCRIPTION</span></span>
<span data-ttu-id="29912-109">Cmdleten **Remove-AzStorageBlob** tar bort angiven BLOB från ett lagrings konto i Azure.</span><span class="sxs-lookup"><span data-stu-id="29912-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="29912-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29912-110">EXAMPLES</span></span>

### <span data-ttu-id="29912-111">Exempel 1: ta bort en lagrings-BLOB efter namn</span><span class="sxs-lookup"><span data-stu-id="29912-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="29912-112">Det här kommandot tar bort en blob som identifieras genom dess namn.</span><span class="sxs-lookup"><span data-stu-id="29912-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="29912-113">Exempel 2: ta bort en lagrings-BLOB med pipelinen</span><span class="sxs-lookup"><span data-stu-id="29912-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="29912-114">I det här kommandot används pipeline.</span><span class="sxs-lookup"><span data-stu-id="29912-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="29912-115">Exempel 3: ta bort lagrings-BLOB med pipelinen</span><span class="sxs-lookup"><span data-stu-id="29912-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="29912-116">Det här kommandot använder jokertecknet (\*) och pipeline för att hämta blobben eller BLOB och sedan ta bort dem.</span><span class="sxs-lookup"><span data-stu-id="29912-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

### <span data-ttu-id="29912-117">Exempel 4: ta bort en blob-version</span><span class="sxs-lookup"><span data-stu-id="29912-117">Example 4: Remove a single blob version</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z"
```

<span data-ttu-id="29912-118">Det här kommandot tar bort en BLOB-verion med VersionId.</span><span class="sxs-lookup"><span data-stu-id="29912-118">This command removes a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="29912-119">Exempel 5: ta bort en enda BLOB-ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="29912-119">Example 5: Remove a single blob snapshot</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"
```

<span data-ttu-id="29912-120">Det här kommandot tar bort en ögonblicks bild av en blob med SnapshotTime.</span><span class="sxs-lookup"><span data-stu-id="29912-120">This command removes a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="29912-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29912-121">PARAMETERS</span></span>

### <span data-ttu-id="29912-122">-BLOB</span><span class="sxs-lookup"><span data-stu-id="29912-122">-Blob</span></span>
<span data-ttu-id="29912-123">Anger namnet på den blob som du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="29912-123">Specifies the name of the blob you want to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29912-124">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="29912-124">-BlobBaseClient</span></span>
<span data-ttu-id="29912-125">BlobBaseClient-objekt</span><span class="sxs-lookup"><span data-stu-id="29912-125">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29912-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="29912-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="29912-127">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="29912-127">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="29912-128">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="29912-128">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="29912-129">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="29912-129">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="29912-130">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="29912-130">-CloudBlob</span></span>
<span data-ttu-id="29912-131">Anger en moln-blob.</span><span class="sxs-lookup"><span data-stu-id="29912-131">Specifies a cloud blob.</span></span>
<span data-ttu-id="29912-132">För att hämta ett **CloudBlob** -objekt, Använd cmdleten Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="29912-132">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29912-133">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="29912-133">-CloudBlobContainer</span></span>
<span data-ttu-id="29912-134">Anger ett **CloudBlobContainer** -objekt från klient bibliotek för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="29912-134">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="29912-135">Du kan använda Get-AzStorageContainer cmdlet för att få den.</span><span class="sxs-lookup"><span data-stu-id="29912-135">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29912-136">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="29912-136">-ConcurrentTaskCount</span></span>
<span data-ttu-id="29912-137">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="29912-137">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="29912-138">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="29912-138">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="29912-139">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="29912-139">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="29912-140">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="29912-140">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="29912-141">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="29912-141">The default value is 10.</span></span>

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

### <span data-ttu-id="29912-142">-Container</span><span class="sxs-lookup"><span data-stu-id="29912-142">-Container</span></span>
<span data-ttu-id="29912-143">Anger namnet på behållaren.</span><span class="sxs-lookup"><span data-stu-id="29912-143">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29912-144">-Kontext</span><span class="sxs-lookup"><span data-stu-id="29912-144">-Context</span></span>
<span data-ttu-id="29912-145">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="29912-145">Specifies the Azure storage context.</span></span>
<span data-ttu-id="29912-146">Du kan använda New-AzStorageContext cmdlet för att skapa den.</span><span class="sxs-lookup"><span data-stu-id="29912-146">You can use the New-AzStorageContext cmdlet to create it.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29912-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29912-147">-DefaultProfile</span></span>
<span data-ttu-id="29912-148">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="29912-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29912-149">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="29912-149">-DeleteSnapshot</span></span>
<span data-ttu-id="29912-150">Anger att alla stillbilder ska tas bort, men inte bas-blob.</span><span class="sxs-lookup"><span data-stu-id="29912-150">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="29912-151">Om den här parametern inte anges tas bas-blob och dess ögonblicks bilder bort tillsammans.</span><span class="sxs-lookup"><span data-stu-id="29912-151">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="29912-152">Användaren uppmanas att bekräfta borttagningen.</span><span class="sxs-lookup"><span data-stu-id="29912-152">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="29912-153">-Force</span><span class="sxs-lookup"><span data-stu-id="29912-153">-Force</span></span>
<span data-ttu-id="29912-154">Anger att denna cmdlet tar bort blobben och dess ögonblicks bild utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="29912-154">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="29912-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29912-155">-PassThru</span></span>
<span data-ttu-id="29912-156">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="29912-156">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="29912-157">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="29912-157">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="29912-158">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="29912-158">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="29912-159">Anger Azure-profilen för den cmdlet som ska läsas.</span><span class="sxs-lookup"><span data-stu-id="29912-159">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="29912-160">Om det inte anges läser cmdleten från standard profilen.</span><span class="sxs-lookup"><span data-stu-id="29912-160">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="29912-161">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="29912-161">-SnapshotTime</span></span>
<span data-ttu-id="29912-162">Blobb SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="29912-162">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29912-163">-VersionId</span><span class="sxs-lookup"><span data-stu-id="29912-163">-VersionId</span></span>
<span data-ttu-id="29912-164">Blobb VersionId</span><span class="sxs-lookup"><span data-stu-id="29912-164">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29912-165">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="29912-165">-Confirm</span></span>
<span data-ttu-id="29912-166">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="29912-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29912-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29912-167">-WhatIf</span></span>
<span data-ttu-id="29912-168">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="29912-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29912-169">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="29912-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29912-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29912-170">CommonParameters</span></span>
<span data-ttu-id="29912-171">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29912-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29912-172">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29912-172">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29912-173">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29912-173">INPUTS</span></span>

### <span data-ttu-id="29912-174">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="29912-174">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="29912-175">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="29912-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="29912-176">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="29912-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="29912-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29912-177">OUTPUTS</span></span>

### <span data-ttu-id="29912-178">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="29912-178">System.Boolean</span></span>

## <span data-ttu-id="29912-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29912-179">NOTES</span></span>

## <span data-ttu-id="29912-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29912-180">RELATED LINKS</span></span>

[<span data-ttu-id="29912-181">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="29912-181">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="29912-182">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="29912-182">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="29912-183">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="29912-183">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)
