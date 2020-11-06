---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobContent.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 9eb7337ee39ed0e9c4d179a6a89401398a0d80f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581592"
---
# <span data-ttu-id="d8237-101">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d8237-101">Get-AzureStorageBlobContent</span></span>

## <span data-ttu-id="d8237-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8237-102">SYNOPSIS</span></span>
<span data-ttu-id="d8237-103">Laddar ner en lagrings-blob.</span><span class="sxs-lookup"><span data-stu-id="d8237-103">Downloads a storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8237-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8237-104">SYNTAX</span></span>

### <span data-ttu-id="d8237-105">ReceiveManual (standard)</span><span class="sxs-lookup"><span data-stu-id="d8237-105">ReceiveManual (Default)</span></span>
```
Get-AzureStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8237-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="d8237-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8237-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="d8237-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8237-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8237-108">DESCRIPTION</span></span>
<span data-ttu-id="d8237-109">Cmdleten **Get-AzureStorageBlobContent** laddar ned angiven lagrings-blob.</span><span class="sxs-lookup"><span data-stu-id="d8237-109">The **Get-AzureStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="d8237-110">Om BLOB-namnet inte är giltigt för den lokala datorn löses det automatiskt om det är möjligt.</span><span class="sxs-lookup"><span data-stu-id="d8237-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="d8237-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8237-111">EXAMPLES</span></span>

### <span data-ttu-id="d8237-112">Exempel 1: Ladda ned BLOB-innehåll efter namn</span><span class="sxs-lookup"><span data-stu-id="d8237-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzureStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="d8237-113">Det här kommandot laddar ned en BLOB efter namn.</span><span class="sxs-lookup"><span data-stu-id="d8237-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="d8237-114">Exempel 2: Ladda ned BLOB-innehåll med pipeline</span><span class="sxs-lookup"><span data-stu-id="d8237-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container containername -Blob blobname | Get-AzureStorageBlobContent
```

<span data-ttu-id="d8237-115">Det här kommandot använder pipeline för att hitta och ladda ner BLOB-innehåll.</span><span class="sxs-lookup"><span data-stu-id="d8237-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="d8237-116">Exempel 3: Ladda ned BLOB-innehåll med pipeline och ett jokertecken</span><span class="sxs-lookup"><span data-stu-id="d8237-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Get-AzureStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="d8237-117">I det här exemplet används jokertecknet asterisk och pipeline för att hitta och ladda ner BLOB-innehåll.</span><span class="sxs-lookup"><span data-stu-id="d8237-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

## <span data-ttu-id="d8237-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8237-118">PARAMETERS</span></span>

### <span data-ttu-id="d8237-119">-BLOB</span><span class="sxs-lookup"><span data-stu-id="d8237-119">-Blob</span></span>
<span data-ttu-id="d8237-120">Anger namnet på blobben som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="d8237-120">Specifies the name of the blob to be downloaded.</span></span>

```yaml
Type: String
Parameter Sets: ReceiveManual, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8237-121">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="d8237-121">-CheckMd5</span></span>
<span data-ttu-id="d8237-122">Anger om Md5-summan för den hämtade filen ska kontrol leras.</span><span class="sxs-lookup"><span data-stu-id="d8237-122">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="d8237-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d8237-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d8237-124">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="d8237-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d8237-125">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="d8237-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d8237-126">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="d8237-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d8237-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="d8237-127">-CloudBlob</span></span>
<span data-ttu-id="d8237-128">Anger en moln-blob.</span><span class="sxs-lookup"><span data-stu-id="d8237-128">Specifies a cloud blob.</span></span>
<span data-ttu-id="d8237-129">För att hämta ett **CloudBlob** -objekt, Använd cmdleten Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="d8237-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="d8237-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="d8237-130">-CloudBlobContainer</span></span>
<span data-ttu-id="d8237-131">Anger ett **CloudBlobContainer** -objekt från klient bibliotek för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="d8237-131">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="d8237-132">Du kan skapa det eller använda cmdleten Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="d8237-132">You can create it or use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="d8237-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d8237-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d8237-134">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="d8237-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d8237-135">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="d8237-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d8237-136">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="d8237-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d8237-137">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="d8237-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d8237-138">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="d8237-138">The default value is 10.</span></span>

<span data-ttu-id="d8237-139">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="d8237-139">The default value is 10.</span></span>

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

### <span data-ttu-id="d8237-140">-Container</span><span class="sxs-lookup"><span data-stu-id="d8237-140">-Container</span></span>
<span data-ttu-id="d8237-141">Anger namnet på den behållare vars BLOB du vill ladda ned.</span><span class="sxs-lookup"><span data-stu-id="d8237-141">Specifies the name of container that has the blob you want to download.</span></span>

```yaml
Type: String
Parameter Sets: ReceiveManual
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8237-142">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d8237-142">-Context</span></span>
<span data-ttu-id="d8237-143">Anger det Azure Storage-konto som du vill ladda ned BLOB-innehåll från.</span><span class="sxs-lookup"><span data-stu-id="d8237-143">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="d8237-144">Du kan använda New-AzureStorageContext cmdlet för att skapa en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="d8237-144">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="d8237-145">-Mål</span><span class="sxs-lookup"><span data-stu-id="d8237-145">-Destination</span></span>
<span data-ttu-id="d8237-146">Anger platsen där den hämtade filen ska lagras.</span><span class="sxs-lookup"><span data-stu-id="d8237-146">Specifies the location to store the downloaded file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8237-147">-Force</span><span class="sxs-lookup"><span data-stu-id="d8237-147">-Force</span></span>
<span data-ttu-id="d8237-148">Skriver över en befintlig fil utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d8237-148">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="d8237-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d8237-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d8237-150">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="d8237-150">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="d8237-151">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="d8237-151">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="d8237-152">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d8237-152">-Confirm</span></span>
<span data-ttu-id="d8237-153">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d8237-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8237-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8237-154">-WhatIf</span></span>
<span data-ttu-id="d8237-155">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d8237-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8237-156">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d8237-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8237-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8237-157">CommonParameters</span></span>
<span data-ttu-id="d8237-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8237-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8237-159">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8237-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8237-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8237-160">INPUTS</span></span>

### <span data-ttu-id="d8237-161">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d8237-161">IStorageContext</span></span>

<span data-ttu-id="d8237-162">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d8237-162">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="d8237-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8237-163">OUTPUTS</span></span>

### <span data-ttu-id="d8237-164">AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d8237-164">AzureStorageContainer</span></span>

## <span data-ttu-id="d8237-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8237-165">NOTES</span></span>
* <span data-ttu-id="d8237-166">Om BLOB-namnet är ogiltigt för den lokala datorn kan den här cmdleten lösa problemet, om det är möjligt.</span><span class="sxs-lookup"><span data-stu-id="d8237-166">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="d8237-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8237-167">RELATED LINKS</span></span>

[<span data-ttu-id="d8237-168">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d8237-168">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)

[<span data-ttu-id="d8237-169">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d8237-169">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="d8237-170">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d8237-170">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
