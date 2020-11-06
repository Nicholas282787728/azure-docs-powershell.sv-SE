---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b40585f584cc8c2634acab54e6862e4163c6b7a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572092"
---
# <span data-ttu-id="cd052-101">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cd052-101">Remove-AzureStorageBlob</span></span>

## <span data-ttu-id="cd052-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd052-102">SYNOPSIS</span></span>
<span data-ttu-id="cd052-103">Tar bort angiven lagrings-blob.</span><span class="sxs-lookup"><span data-stu-id="cd052-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="cd052-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd052-104">SYNTAX</span></span>

### <span data-ttu-id="cd052-105">NamePipeline (standard)</span><span class="sxs-lookup"><span data-stu-id="cd052-105">NamePipeline (Default)</span></span>
```
Remove-AzureStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd052-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="cd052-106">BlobPipeline</span></span>
```
Remove-AzureStorageBlob -CloudBlob <CloudBlob> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd052-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="cd052-107">ContainerPipeline</span></span>
```
Remove-AzureStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd052-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd052-108">DESCRIPTION</span></span>
<span data-ttu-id="cd052-109">Cmdleten **Remove-AzureStorageBlob** tar bort angiven BLOB från ett lagrings konto i Azure.</span><span class="sxs-lookup"><span data-stu-id="cd052-109">The **Remove-AzureStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="cd052-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd052-110">EXAMPLES</span></span>

### <span data-ttu-id="cd052-111">Exempel 1: ta bort en lagrings-BLOB efter namn</span><span class="sxs-lookup"><span data-stu-id="cd052-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzureStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="cd052-112">Det här kommandot tar bort en blob som identifieras genom dess namn.</span><span class="sxs-lookup"><span data-stu-id="cd052-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="cd052-113">Exempel 2: ta bort en lagrings-BLOB med pipelinen</span><span class="sxs-lookup"><span data-stu-id="cd052-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzureStorageBlob
```

<span data-ttu-id="cd052-114">I det här kommandot används pipeline.</span><span class="sxs-lookup"><span data-stu-id="cd052-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="cd052-115">Exempel 3: ta bort lagrings-BLOB med pipelinen</span><span class="sxs-lookup"><span data-stu-id="cd052-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container container* | Remove-AzureStorageBlob -Blob "BlobName"
```

<span data-ttu-id="cd052-116">Det här kommandot använder jokertecknet (\*) och pipeline för att hämta blobben eller BLOB och sedan ta bort dem.</span><span class="sxs-lookup"><span data-stu-id="cd052-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

## <span data-ttu-id="cd052-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd052-117">PARAMETERS</span></span>

### <span data-ttu-id="cd052-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="cd052-118">-Blob</span></span>
<span data-ttu-id="cd052-119">Anger namnet på den blob som du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="cd052-119">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="cd052-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cd052-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cd052-121">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="cd052-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cd052-122">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="cd052-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cd052-123">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="cd052-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="cd052-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="cd052-124">-CloudBlob</span></span>
<span data-ttu-id="cd052-125">Anger en moln-blob.</span><span class="sxs-lookup"><span data-stu-id="cd052-125">Specifies a cloud blob.</span></span>
<span data-ttu-id="cd052-126">För att hämta ett **CloudBlob** -objekt, Använd cmdleten Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="cd052-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="cd052-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="cd052-127">-CloudBlobContainer</span></span>
<span data-ttu-id="cd052-128">Anger ett **CloudBlobContainer** -objekt från klient bibliotek för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="cd052-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="cd052-129">Du kan använda Get-AzureStorageContainer cmdlet för att få den.</span><span class="sxs-lookup"><span data-stu-id="cd052-129">You can use the Get-AzureStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="cd052-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cd052-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cd052-131">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="cd052-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cd052-132">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="cd052-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cd052-133">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="cd052-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cd052-134">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="cd052-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cd052-135">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="cd052-135">The default value is 10.</span></span>

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

### <span data-ttu-id="cd052-136">-Container</span><span class="sxs-lookup"><span data-stu-id="cd052-136">-Container</span></span>
<span data-ttu-id="cd052-137">Anger namnet på behållaren.</span><span class="sxs-lookup"><span data-stu-id="cd052-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="cd052-138">-Kontext</span><span class="sxs-lookup"><span data-stu-id="cd052-138">-Context</span></span>
<span data-ttu-id="cd052-139">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="cd052-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="cd052-140">Du kan använda New-AzureStorageContext cmdlet för att skapa den.</span><span class="sxs-lookup"><span data-stu-id="cd052-140">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="cd052-141">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="cd052-141">-DeleteSnapshot</span></span>
<span data-ttu-id="cd052-142">Anger att alla stillbilder ska tas bort, men inte bas-blob.</span><span class="sxs-lookup"><span data-stu-id="cd052-142">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="cd052-143">Om den här parametern inte anges tas bas-blob och dess ögonblicks bilder bort tillsammans.</span><span class="sxs-lookup"><span data-stu-id="cd052-143">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="cd052-144">Användaren uppmanas att bekräfta borttagningen.</span><span class="sxs-lookup"><span data-stu-id="cd052-144">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="cd052-145">-Force</span><span class="sxs-lookup"><span data-stu-id="cd052-145">-Force</span></span>
<span data-ttu-id="cd052-146">Anger att denna cmdlet tar bort blobben och dess ögonblicks bild utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="cd052-146">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="cd052-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd052-147">-PassThru</span></span>
<span data-ttu-id="cd052-148">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="cd052-148">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="cd052-149">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="cd052-149">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="cd052-150">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cd052-150">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cd052-151">Anger Azure-profilen för den cmdlet som ska läsas.</span><span class="sxs-lookup"><span data-stu-id="cd052-151">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="cd052-152">Om det inte anges läser cmdleten från standard profilen.</span><span class="sxs-lookup"><span data-stu-id="cd052-152">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="cd052-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cd052-153">-Confirm</span></span>
<span data-ttu-id="cd052-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cd052-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd052-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd052-155">-WhatIf</span></span>
<span data-ttu-id="cd052-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cd052-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd052-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cd052-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd052-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd052-158">CommonParameters</span></span>
<span data-ttu-id="cd052-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd052-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd052-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd052-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd052-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd052-161">INPUTS</span></span>

## <span data-ttu-id="cd052-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd052-162">OUTPUTS</span></span>

## <span data-ttu-id="cd052-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd052-163">NOTES</span></span>

## <span data-ttu-id="cd052-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd052-164">RELATED LINKS</span></span>

[<span data-ttu-id="cd052-165">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cd052-165">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="cd052-166">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cd052-166">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="cd052-167">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cd052-167">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)
