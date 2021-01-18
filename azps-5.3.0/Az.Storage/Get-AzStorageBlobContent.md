---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
ms.openlocfilehash: eec7d4b29f752d3bf302dc9f5c35fa5c6da51c6f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522176"
---
# <span data-ttu-id="9ad8b-101">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="9ad8b-101">Get-AzStorageBlobContent</span></span>

## <span data-ttu-id="9ad8b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9ad8b-102">SYNOPSIS</span></span>
<span data-ttu-id="9ad8b-103">Laddar ner en lagrings-blob.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-103">Downloads a storage blob.</span></span>

## <span data-ttu-id="9ad8b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9ad8b-104">SYNTAX</span></span>

### <span data-ttu-id="9ad8b-105">ReceiveManual (standard)</span><span class="sxs-lookup"><span data-stu-id="9ad8b-105">ReceiveManual (Default)</span></span>
```
Get-AzStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ad8b-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="9ad8b-106">BlobPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ad8b-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="9ad8b-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ad8b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9ad8b-108">DESCRIPTION</span></span>
<span data-ttu-id="9ad8b-109">Cmdleten **Get-AzStorageBlobContent** laddar ned angiven lagrings-blob.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-109">The **Get-AzStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="9ad8b-110">Om BLOB-namnet inte är giltigt för den lokala datorn löses det automatiskt om det är möjligt.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="9ad8b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9ad8b-111">EXAMPLES</span></span>

### <span data-ttu-id="9ad8b-112">Exempel 1: Ladda ned BLOB-innehåll efter namn</span><span class="sxs-lookup"><span data-stu-id="9ad8b-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="9ad8b-113">Det här kommandot laddar ned en BLOB efter namn.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="9ad8b-114">Exempel 2: Ladda ned BLOB-innehåll med pipeline</span><span class="sxs-lookup"><span data-stu-id="9ad8b-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container containername -Blob blobname | Get-AzStorageBlobContent
```

<span data-ttu-id="9ad8b-115">Det här kommandot använder pipeline för att hitta och ladda ner BLOB-innehåll.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="9ad8b-116">Exempel 3: Ladda ned BLOB-innehåll med pipeline och ett jokertecken</span><span class="sxs-lookup"><span data-stu-id="9ad8b-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzStorageContainer container* | Get-AzStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="9ad8b-117">I det här exemplet används jokertecknet asterisk och pipeline för att hitta och ladda ner BLOB-innehåll.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="9ad8b-118">Exempel 4: Hämta ett BLOB-objekt och spara det i en variabel och hämta sedan BLOB-innehåll med BLOB-objektet</span><span class="sxs-lookup"><span data-stu-id="9ad8b-118">Example 4: Get a blob object and save it in a variable, then download blob content with the blob object</span></span>
```
PS C:\>$blob = Get-AzStorageBlob -Container containername -Blob blobname 
PS C:\>Get-AzStorageBlobContent -CloudBlob $blob.ICloudBlob -Destination "C:\test"
```

<span data-ttu-id="9ad8b-119">Det här exemplet får först ett BLOB-objekt och spara det i en variabel och sedan ladda ned BLOB-innehåll med BLOB-objektet.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-119">This example first get a blob object and save it in a variable, then download blob content with the blob object.</span></span> 

## <span data-ttu-id="9ad8b-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9ad8b-120">PARAMETERS</span></span>

### <span data-ttu-id="9ad8b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ad8b-121">-AsJob</span></span>
<span data-ttu-id="9ad8b-122">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-122">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="9ad8b-123">-BLOB</span><span class="sxs-lookup"><span data-stu-id="9ad8b-123">-Blob</span></span>
<span data-ttu-id="9ad8b-124">Anger namnet på blobben som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-124">Specifies the name of the blob to be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ad8b-125">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="9ad8b-125">-BlobBaseClient</span></span>
<span data-ttu-id="9ad8b-126">BlobBaseClient-objekt</span><span class="sxs-lookup"><span data-stu-id="9ad8b-126">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="9ad8b-127">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="9ad8b-127">-CheckMd5</span></span>
<span data-ttu-id="9ad8b-128">Anger om Md5-summan för den hämtade filen ska kontrol leras.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-128">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="9ad8b-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9ad8b-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9ad8b-130">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9ad8b-131">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9ad8b-132">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9ad8b-133">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="9ad8b-133">-CloudBlob</span></span>
<span data-ttu-id="9ad8b-134">Anger en moln-blob.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-134">Specifies a cloud blob.</span></span>
<span data-ttu-id="9ad8b-135">För att hämta ett **CloudBlob** -objekt, Använd cmdleten Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-135">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="9ad8b-136">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="9ad8b-136">-CloudBlobContainer</span></span>
<span data-ttu-id="9ad8b-137">Anger ett **CloudBlobContainer** -objekt från klient bibliotek för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-137">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="9ad8b-138">Du kan skapa det eller använda cmdleten Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-138">You can create it or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="9ad8b-139">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9ad8b-139">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9ad8b-140">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-140">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9ad8b-141">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-141">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9ad8b-142">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-142">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9ad8b-143">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-143">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9ad8b-144">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-144">The default value is 10.</span></span>

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

### <span data-ttu-id="9ad8b-145">-Container</span><span class="sxs-lookup"><span data-stu-id="9ad8b-145">-Container</span></span>
<span data-ttu-id="9ad8b-146">Anger namnet på den behållare vars BLOB du vill ladda ned.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-146">Specifies the name of container that has the blob you want to download.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ad8b-147">-Kontext</span><span class="sxs-lookup"><span data-stu-id="9ad8b-147">-Context</span></span>
<span data-ttu-id="9ad8b-148">Anger det Azure Storage-konto som du vill ladda ned BLOB-innehåll från.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-148">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="9ad8b-149">Du kan använda New-AzStorageContext cmdlet för att skapa en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-149">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="9ad8b-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ad8b-150">-DefaultProfile</span></span>
<span data-ttu-id="9ad8b-151">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ad8b-152">-Mål</span><span class="sxs-lookup"><span data-stu-id="9ad8b-152">-Destination</span></span>
<span data-ttu-id="9ad8b-153">Anger platsen där den hämtade filen ska lagras.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-153">Specifies the location to store the downloaded file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ad8b-154">-Force</span><span class="sxs-lookup"><span data-stu-id="9ad8b-154">-Force</span></span>
<span data-ttu-id="9ad8b-155">Skriver över en befintlig fil utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-155">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="9ad8b-156">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9ad8b-156">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9ad8b-157">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-157">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="9ad8b-158">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-158">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="9ad8b-159">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9ad8b-159">-Confirm</span></span>
<span data-ttu-id="9ad8b-160">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ad8b-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ad8b-161">-WhatIf</span></span>
<span data-ttu-id="9ad8b-162">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ad8b-163">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ad8b-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ad8b-164">CommonParameters</span></span>
<span data-ttu-id="9ad8b-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ad8b-166">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ad8b-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ad8b-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9ad8b-167">INPUTS</span></span>

### <span data-ttu-id="9ad8b-168">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="9ad8b-168">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="9ad8b-169">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="9ad8b-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="9ad8b-170">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9ad8b-170">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9ad8b-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9ad8b-171">OUTPUTS</span></span>

### <span data-ttu-id="9ad8b-172">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9ad8b-172">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="9ad8b-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9ad8b-173">NOTES</span></span>
* <span data-ttu-id="9ad8b-174">Om BLOB-namnet är ogiltigt för den lokala datorn kan den här cmdleten lösa problemet, om det är möjligt.</span><span class="sxs-lookup"><span data-stu-id="9ad8b-174">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="9ad8b-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9ad8b-175">RELATED LINKS</span></span>

[<span data-ttu-id="9ad8b-176">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="9ad8b-176">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)

[<span data-ttu-id="9ad8b-177">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9ad8b-177">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="9ad8b-178">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9ad8b-178">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
