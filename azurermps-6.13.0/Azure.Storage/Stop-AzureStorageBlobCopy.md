---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/stop-azurestorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageBlobCopy.md
ms.openlocfilehash: 67a6a9d706b8865ebca4290649a30bc8e9817569
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756425"
---
# <span data-ttu-id="df1d9-101">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="df1d9-101">Stop-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="df1d9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df1d9-102">SYNOPSIS</span></span>
<span data-ttu-id="df1d9-103">Avbryter en kopierings åtgärd.</span><span class="sxs-lookup"><span data-stu-id="df1d9-103">Stops a copy operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df1d9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df1d9-104">SYNTAX</span></span>

### <span data-ttu-id="df1d9-105">NamePipeline (standard)</span><span class="sxs-lookup"><span data-stu-id="df1d9-105">NamePipeline (Default)</span></span>
```
Stop-AzureStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df1d9-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="df1d9-106">BlobPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df1d9-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="df1d9-107">ContainerPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df1d9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df1d9-108">DESCRIPTION</span></span>
<span data-ttu-id="df1d9-109">Cmdleten **Stop-AzureStorageBlobCopy** stoppar en kopierings åtgärd till angiven destinations-blob.</span><span class="sxs-lookup"><span data-stu-id="df1d9-109">The **Stop-AzureStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="df1d9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df1d9-110">EXAMPLES</span></span>

### <span data-ttu-id="df1d9-111">Exempel 1: stoppa kopierings åtgärd efter namn</span><span class="sxs-lookup"><span data-stu-id="df1d9-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzureStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="df1d9-112">Det här kommandot stoppar kopierings åtgärden efter namn.</span><span class="sxs-lookup"><span data-stu-id="df1d9-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="df1d9-113">Exempel 2: Stoppa kopieringen genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="df1d9-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Stop-AzureStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="df1d9-114">Det här kommandot stoppar kopieringen genom att skicka behållaren i pipeline från **Get-AzureStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="df1d9-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="df1d9-115">Exempel 3: Stoppa kopieringen med hjälp av pipeline och Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="df1d9-115">Example 3: Stop copy operation by using the pipeline and Get-AzureStorageBlob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" | Stop-AzureStorageBlobCopy -Force
```

<span data-ttu-id="df1d9-116">I det här exemplet avbryts kopieringen genom att behållaren skickas från Get-AzureStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df1d9-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzureStorageBlob cmdlet.</span></span>

## <span data-ttu-id="df1d9-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df1d9-117">PARAMETERS</span></span>

### <span data-ttu-id="df1d9-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="df1d9-118">-Blob</span></span>
<span data-ttu-id="df1d9-119">Anger namnet på blobben.</span><span class="sxs-lookup"><span data-stu-id="df1d9-119">Specifies the name of the blob.</span></span>

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

### <span data-ttu-id="df1d9-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="df1d9-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="df1d9-121">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="df1d9-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="df1d9-122">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="df1d9-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="df1d9-123">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="df1d9-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="df1d9-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="df1d9-124">-CloudBlob</span></span>
<span data-ttu-id="df1d9-125">Anger ett **CloudBlob** -objekt från ett Azure Storage-bibliotek.</span><span class="sxs-lookup"><span data-stu-id="df1d9-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="df1d9-126">För att hämta ett **CloudBlob** -objekt, Använd cmdleten Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="df1d9-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df1d9-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="df1d9-127">-CloudBlobContainer</span></span>
<span data-ttu-id="df1d9-128">Anger ett **CloudBlobContainer** -objekt från klient bibliotek för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="df1d9-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="df1d9-129">Du kan skapa objektet eller använda Get-AzureStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df1d9-129">You can create the object or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df1d9-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="df1d9-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="df1d9-131">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="df1d9-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="df1d9-132">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="df1d9-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="df1d9-133">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="df1d9-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="df1d9-134">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="df1d9-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="df1d9-135">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="df1d9-135">The default value is 10.</span></span>

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

### <span data-ttu-id="df1d9-136">-Container</span><span class="sxs-lookup"><span data-stu-id="df1d9-136">-Container</span></span>
<span data-ttu-id="df1d9-137">Anger namnet på behållaren.</span><span class="sxs-lookup"><span data-stu-id="df1d9-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="df1d9-138">-Kontext</span><span class="sxs-lookup"><span data-stu-id="df1d9-138">-Context</span></span>
<span data-ttu-id="df1d9-139">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="df1d9-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="df1d9-140">Du kan skapa kontexten med hjälp av New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df1d9-140">You can create the context by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="df1d9-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="df1d9-141">-CopyId</span></span>
<span data-ttu-id="df1d9-142">Anger kopie-ID.</span><span class="sxs-lookup"><span data-stu-id="df1d9-142">Specifies the copy ID.</span></span>

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

### <span data-ttu-id="df1d9-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df1d9-143">-DefaultProfile</span></span>
<span data-ttu-id="df1d9-144">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="df1d9-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df1d9-145">-Force</span><span class="sxs-lookup"><span data-stu-id="df1d9-145">-Force</span></span>
<span data-ttu-id="df1d9-146">Stoppar den aktuella kopierings aktiviteten för angiven BLOB utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="df1d9-146">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="df1d9-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="df1d9-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="df1d9-148">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="df1d9-148">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="df1d9-149">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="df1d9-149">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="df1d9-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="df1d9-150">-Confirm</span></span>
<span data-ttu-id="df1d9-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="df1d9-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df1d9-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df1d9-152">-WhatIf</span></span>
<span data-ttu-id="df1d9-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="df1d9-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df1d9-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="df1d9-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df1d9-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df1d9-155">CommonParameters</span></span>
<span data-ttu-id="df1d9-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df1d9-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df1d9-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df1d9-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df1d9-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df1d9-158">INPUTS</span></span>

### <span data-ttu-id="df1d9-159">Microsoft. WindowsAzure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="df1d9-159">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="df1d9-160">Microsoft. WindowsAzure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="df1d9-160">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="df1d9-161">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="df1d9-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="df1d9-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df1d9-162">OUTPUTS</span></span>

### <span data-ttu-id="df1d9-163">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="df1d9-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="df1d9-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df1d9-164">NOTES</span></span>

## <span data-ttu-id="df1d9-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df1d9-165">RELATED LINKS</span></span>

[<span data-ttu-id="df1d9-166">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="df1d9-166">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="df1d9-167">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="df1d9-167">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="df1d9-168">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="df1d9-168">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="df1d9-169">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="df1d9-169">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)
