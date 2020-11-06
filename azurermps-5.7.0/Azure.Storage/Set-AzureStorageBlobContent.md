---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
ms.openlocfilehash: eddc442dd442fbb64f7b075f49a3c638ea6920e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580479"
---
# <span data-ttu-id="45069-101">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="45069-101">Set-AzureStorageBlobContent</span></span>

## <span data-ttu-id="45069-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45069-102">SYNOPSIS</span></span>
<span data-ttu-id="45069-103">Laddar upp en lokal fil till en Azure-lagrings-blob.</span><span class="sxs-lookup"><span data-stu-id="45069-103">Uploads a local file to an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45069-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45069-104">SYNTAX</span></span>

### <span data-ttu-id="45069-105">SendManual (standard)</span><span class="sxs-lookup"><span data-stu-id="45069-105">SendManual (Default)</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45069-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="45069-106">ContainerPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45069-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="45069-107">BlobPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45069-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45069-108">DESCRIPTION</span></span>
<span data-ttu-id="45069-109">Cmdleten **set-AzureStorageBlobContent** laddar upp en lokal fil till en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="45069-109">The **Set-AzureStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="45069-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45069-110">EXAMPLES</span></span>

### <span data-ttu-id="45069-111">Exempel 1: Ladda upp en namngiven fil</span><span class="sxs-lookup"><span data-stu-id="45069-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzureStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="45069-112">Det här kommandot laddar upp filen med namnet PlanningData till en blob som heter Planning2015.</span><span class="sxs-lookup"><span data-stu-id="45069-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="45069-113">Exempel 2: Ladda upp alla filer under den aktuella mappen</span><span class="sxs-lookup"><span data-stu-id="45069-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzureStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="45069-114">I det här kommandot används den grundläggande Windows PowerShell-cmdleten Get-ChildItem för att hämta alla filer i den aktuella mappen och i undermappar och skickar dem till den aktuella cmdleten med operatören.</span><span class="sxs-lookup"><span data-stu-id="45069-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="45069-115">Cmdleten **set-AzureStorageBlobContent** laddar upp filerna till behållaren med namnet ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="45069-115">The **Set-AzureStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="45069-116">Exempel 3: Skriv över en befintlig BLOB</span><span class="sxs-lookup"><span data-stu-id="45069-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzureStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="45069-117">Det här kommandot hämtar blobben med namnet Planning2015 i ContosoUploads-behållaren genom att använda Get-AzureStorageBlob cmdlet och sedan överföra denna blob till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45069-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzureStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="45069-118">Kommandot laddar upp filen med namnet ContosoPlanning som Planning2015.</span><span class="sxs-lookup"><span data-stu-id="45069-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="45069-119">Det här kommandot anger inte parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="45069-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="45069-120">Med kommandot uppmanas du att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="45069-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="45069-121">Om du bekräftar kommandot skriver cmdleten över den befintliga blobben.</span><span class="sxs-lookup"><span data-stu-id="45069-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="45069-122">Exempel 4: Ladda upp en fil till en behållare med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="45069-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container "ContosoUpload*" | Set-AzureStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="45069-123">Det här kommandot hämtar behållaren som börjar med strängen ContosoUpload med hjälp av cmdleten **Get-AzureStorageContainer** och överför sedan blobben till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45069-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzureStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="45069-124">Kommandot laddar upp filen med namnet ContosoPlanning som Planning2015.</span><span class="sxs-lookup"><span data-stu-id="45069-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="45069-125">Exempel 5: Ladda upp en fil till Page BLOB med metadata och PremiumPageBlobTier som P10</span><span class="sxs-lookup"><span data-stu-id="45069-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="45069-126">Det första kommandot skapar en hash-tabell som innehåller metadata för en blob och lagrar denna hash-tabell i $Metadata variabeln.</span><span class="sxs-lookup"><span data-stu-id="45069-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>

<span data-ttu-id="45069-127">Det andra kommandot laddar upp filen med namnet ContosoPlanning till behållaren med namnet ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="45069-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="45069-128">Blobben innehåller metadata som lagras i $Metadata och har PremiumPageBlobTier som P10.</span><span class="sxs-lookup"><span data-stu-id="45069-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="45069-129">Exempel 6: Ladda upp en fil till blobben med angivna BLOB-egenskaper</span><span class="sxs-lookup"><span data-stu-id="45069-129">Example 6: Upload a file to blob with specified blob properties</span></span>
```
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Properties @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="}
```

<span data-ttu-id="45069-130">Det här kommandot laddar upp filen som heter ContosoPlanning till behållaren med namnet ContosoUploads med angivna BLOB-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="45069-130">This command  uploads the file that is named ContosoPlanning to the container named ContosoUploads with specified blob properties.</span></span>

## <span data-ttu-id="45069-131">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45069-131">PARAMETERS</span></span>

### <span data-ttu-id="45069-132">-BLOB</span><span class="sxs-lookup"><span data-stu-id="45069-132">-Blob</span></span>
<span data-ttu-id="45069-133">Anger namnet på en blob.</span><span class="sxs-lookup"><span data-stu-id="45069-133">Specifies the name of a blob.</span></span>
<span data-ttu-id="45069-134">Denna cmdlet laddar upp en fil till den Azure Storage blob som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="45069-134">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: SendManual, ContainerPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45069-135">-BlobType</span><span class="sxs-lookup"><span data-stu-id="45069-135">-BlobType</span></span>
<span data-ttu-id="45069-136">Anger typen för blobben som denna cmdlet laddar upp.</span><span class="sxs-lookup"><span data-stu-id="45069-136">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="45069-137">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="45069-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="45069-138">Spärrade</span><span class="sxs-lookup"><span data-stu-id="45069-138">Block</span></span>
- <span data-ttu-id="45069-139">Mallsida</span><span class="sxs-lookup"><span data-stu-id="45069-139">Page</span></span>

<span data-ttu-id="45069-140">Standardvärdet är block.</span><span class="sxs-lookup"><span data-stu-id="45069-140">The default value is Block.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Block, Page, Append

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45069-141">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="45069-141">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="45069-142">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="45069-142">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="45069-143">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="45069-143">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="45069-144">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="45069-144">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="45069-145">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="45069-145">-CloudBlob</span></span>
<span data-ttu-id="45069-146">Anger ett **CloudBlob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="45069-146">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="45069-147">För att hämta ett **CloudBlob** -objekt, Använd cmdleten Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="45069-147">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="45069-148">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="45069-148">-CloudBlobContainer</span></span>
<span data-ttu-id="45069-149">Anger ett **CloudBlobContainer** -objekt från klient bibliotek för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="45069-149">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="45069-150">Denna cmdlet laddar upp innehåll till en BLOB i behållaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="45069-150">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="45069-151">För att hämta ett **CloudBlobContainer** -objekt, Använd cmdleten Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="45069-151">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="45069-152">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="45069-152">-ConcurrentTaskCount</span></span>
<span data-ttu-id="45069-153">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="45069-153">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="45069-154">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="45069-154">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="45069-155">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="45069-155">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="45069-156">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="45069-156">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="45069-157">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="45069-157">The default value is 10.</span></span>

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

### <span data-ttu-id="45069-158">-Container</span><span class="sxs-lookup"><span data-stu-id="45069-158">-Container</span></span>
<span data-ttu-id="45069-159">Anger namnet på en behållare.</span><span class="sxs-lookup"><span data-stu-id="45069-159">Specifies the name of a container.</span></span>
<span data-ttu-id="45069-160">Denna cmdlet laddar upp en fil till en BLOB i behållaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="45069-160">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: SendManual
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45069-161">-Kontext</span><span class="sxs-lookup"><span data-stu-id="45069-161">-Context</span></span>
<span data-ttu-id="45069-162">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="45069-162">Specifies an Azure storage context.</span></span>
<span data-ttu-id="45069-163">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="45069-163">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="45069-164">-Fil</span><span class="sxs-lookup"><span data-stu-id="45069-164">-File</span></span>
<span data-ttu-id="45069-165">Anger en lokal fil Sök väg för en fil som ska laddas upp som BLOB-innehåll.</span><span class="sxs-lookup"><span data-stu-id="45069-165">Specifies a local file path for a file to upload as blob content.</span></span>

```yaml
Type: String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45069-166">-Force</span><span class="sxs-lookup"><span data-stu-id="45069-166">-Force</span></span>
<span data-ttu-id="45069-167">Anger att denna cmdlet skriver över en befintlig BLOB utan att be dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="45069-167">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="45069-168">-Metadata</span><span class="sxs-lookup"><span data-stu-id="45069-168">-Metadata</span></span>
<span data-ttu-id="45069-169">Anger metadata för den uppladdade blobben.</span><span class="sxs-lookup"><span data-stu-id="45069-169">Specifies metadata for the uploaded blob.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45069-170">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="45069-170">-PremiumPageBlobTier</span></span>
<span data-ttu-id="45069-171">BLOB Tier</span><span class="sxs-lookup"><span data-stu-id="45069-171">Page Blob Tier</span></span>

```yaml
Type: PremiumPageBlobTier
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45069-172">-Egenskaper</span><span class="sxs-lookup"><span data-stu-id="45069-172">-Properties</span></span>
<span data-ttu-id="45069-173">Anger egenskaper för den uppladdade blobben.</span><span class="sxs-lookup"><span data-stu-id="45069-173">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="45069-174">De egenskaper som stöds är: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="45069-174">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45069-175">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="45069-175">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="45069-176">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="45069-176">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="45069-177">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="45069-177">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="45069-178">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="45069-178">-Confirm</span></span>
<span data-ttu-id="45069-179">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45069-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45069-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45069-180">-WhatIf</span></span>
<span data-ttu-id="45069-181">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="45069-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45069-182">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="45069-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45069-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45069-183">CommonParameters</span></span>
<span data-ttu-id="45069-184">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45069-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45069-185">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45069-185">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45069-186">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45069-186">INPUTS</span></span>

### <span data-ttu-id="45069-187">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="45069-187">IStorageContext</span></span>

<span data-ttu-id="45069-188">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="45069-188">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="45069-189">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45069-189">OUTPUTS</span></span>

### <span data-ttu-id="45069-190">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="45069-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="45069-191">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45069-191">NOTES</span></span>

## <span data-ttu-id="45069-192">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45069-192">RELATED LINKS</span></span>

[<span data-ttu-id="45069-193">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="45069-193">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="45069-194">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="45069-194">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="45069-195">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="45069-195">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
