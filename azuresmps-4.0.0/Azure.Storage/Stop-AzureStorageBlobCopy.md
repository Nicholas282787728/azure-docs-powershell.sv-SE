---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9bdb5a02f474f575f90406ad9026b4437194dffb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572460"
---
# <span data-ttu-id="11137-101">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="11137-101">Stop-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="11137-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11137-102">SYNOPSIS</span></span>
<span data-ttu-id="11137-103">Avbryter en kopierings åtgärd.</span><span class="sxs-lookup"><span data-stu-id="11137-103">Stops a copy operation.</span></span>

## <span data-ttu-id="11137-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11137-104">SYNTAX</span></span>

### <span data-ttu-id="11137-105">NamePipeline (standard)</span><span class="sxs-lookup"><span data-stu-id="11137-105">NamePipeline (Default)</span></span>
```
Stop-AzureStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11137-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="11137-106">BlobPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11137-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="11137-107">ContainerPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11137-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11137-108">DESCRIPTION</span></span>
<span data-ttu-id="11137-109">Cmdleten **Stop-AzureStorageBlobCopy** stoppar en kopierings åtgärd till angiven destinations-blob.</span><span class="sxs-lookup"><span data-stu-id="11137-109">The **Stop-AzureStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="11137-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11137-110">EXAMPLES</span></span>

### <span data-ttu-id="11137-111">Exempel 1: stoppa kopierings åtgärd efter namn</span><span class="sxs-lookup"><span data-stu-id="11137-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzureStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="11137-112">Det här kommandot stoppar kopierings åtgärden efter namn.</span><span class="sxs-lookup"><span data-stu-id="11137-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="11137-113">Exempel 2: Stoppa kopieringen genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="11137-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Stop-AzureStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="11137-114">Det här kommandot stoppar kopieringen genom att skicka behållaren i pipeline från **Get-AzureStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="11137-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="11137-115">Exempel 3: Stoppa kopieringen med hjälp av pipeline och Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="11137-115">Example 3: Stop copy operation by using the pipeline and Get-AzureStorageBlob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" | Stop-AzureStorageBlobCopy -Force
```

<span data-ttu-id="11137-116">I det här exemplet avbryts kopieringen genom att behållaren skickas från Get-AzureStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11137-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzureStorageBlob cmdlet.</span></span>

## <span data-ttu-id="11137-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11137-117">PARAMETERS</span></span>

### <span data-ttu-id="11137-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="11137-118">-Blob</span></span>
<span data-ttu-id="11137-119">Anger namnet på blobben.</span><span class="sxs-lookup"><span data-stu-id="11137-119">Specifies the name of the blob.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11137-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="11137-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="11137-121">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="11137-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="11137-122">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="11137-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="11137-123">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="11137-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="11137-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="11137-124">-CloudBlob</span></span>
<span data-ttu-id="11137-125">Anger ett **CloudBlob** -objekt från ett Azure Storage-bibliotek.</span><span class="sxs-lookup"><span data-stu-id="11137-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="11137-126">För att hämta ett **CloudBlob** -objekt, Använd cmdleten Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="11137-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11137-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="11137-127">-CloudBlobContainer</span></span>
<span data-ttu-id="11137-128">Anger ett **CloudBlobContainer** -objekt från klient bibliotek för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="11137-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="11137-129">Du kan skapa objektet eller använda Get-AzureStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11137-129">You can create the object or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11137-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="11137-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="11137-131">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="11137-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="11137-132">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="11137-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="11137-133">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="11137-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="11137-134">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="11137-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="11137-135">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="11137-135">The default value is 10.</span></span>

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

### <span data-ttu-id="11137-136">-Container</span><span class="sxs-lookup"><span data-stu-id="11137-136">-Container</span></span>
<span data-ttu-id="11137-137">Anger namnet på behållaren.</span><span class="sxs-lookup"><span data-stu-id="11137-137">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11137-138">-Kontext</span><span class="sxs-lookup"><span data-stu-id="11137-138">-Context</span></span>
<span data-ttu-id="11137-139">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="11137-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="11137-140">Du kan skapa kontexten med hjälp av New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11137-140">You can create the context by using the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11137-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="11137-141">-CopyId</span></span>
<span data-ttu-id="11137-142">Anger kopie-ID.</span><span class="sxs-lookup"><span data-stu-id="11137-142">Specifies the copy ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11137-143">-Force</span><span class="sxs-lookup"><span data-stu-id="11137-143">-Force</span></span>
<span data-ttu-id="11137-144">Stoppar den aktuella kopierings aktiviteten för angiven BLOB utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="11137-144">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="11137-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="11137-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="11137-146">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="11137-146">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="11137-147">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="11137-147">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="11137-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="11137-148">-Confirm</span></span>
<span data-ttu-id="11137-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="11137-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11137-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11137-150">-WhatIf</span></span>
<span data-ttu-id="11137-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="11137-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11137-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="11137-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11137-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11137-153">CommonParameters</span></span>
<span data-ttu-id="11137-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11137-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11137-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11137-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11137-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11137-156">INPUTS</span></span>

## <span data-ttu-id="11137-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11137-157">OUTPUTS</span></span>

## <span data-ttu-id="11137-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11137-158">NOTES</span></span>

## <span data-ttu-id="11137-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11137-159">RELATED LINKS</span></span>

[<span data-ttu-id="11137-160">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="11137-160">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="11137-161">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="11137-161">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="11137-162">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="11137-162">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="11137-163">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="11137-163">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)
