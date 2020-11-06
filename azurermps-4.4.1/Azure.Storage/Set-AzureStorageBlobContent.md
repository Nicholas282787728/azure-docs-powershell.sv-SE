---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
gitcommit: https://github.com/Azure/azure-powershell/blob/a2772c13c7cb665d7485636044c46f8c9222fc68
ms.openlocfilehash: c7acda834cda53a86073692dc6c888ce2803d859
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583936"
---
# <span data-ttu-id="9bcba-101">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="9bcba-101">Set-AzureStorageBlobContent</span></span>

## <span data-ttu-id="9bcba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9bcba-102">SYNOPSIS</span></span>
<span data-ttu-id="9bcba-103">Laddar upp en lokal fil till en Azure-lagrings-blob.</span><span class="sxs-lookup"><span data-stu-id="9bcba-103">Uploads a local file to an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bcba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9bcba-104">SYNTAX</span></span>

### <span data-ttu-id="9bcba-105">SendManual (standard)</span><span class="sxs-lookup"><span data-stu-id="9bcba-105">SendManual (Default)</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bcba-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="9bcba-106">ContainerPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bcba-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="9bcba-107">BlobPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bcba-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9bcba-108">DESCRIPTION</span></span>
<span data-ttu-id="9bcba-109">Cmdleten **set-AzureStorageBlobContent** laddar upp en lokal fil till en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="9bcba-109">The **Set-AzureStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="9bcba-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9bcba-110">EXAMPLES</span></span>

### <span data-ttu-id="9bcba-111">Exempel 1: Ladda upp en namngiven fil</span><span class="sxs-lookup"><span data-stu-id="9bcba-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzureStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="9bcba-112">Det här kommandot laddar upp filen med namnet PlanningData till en blob som heter Planning2015.</span><span class="sxs-lookup"><span data-stu-id="9bcba-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="9bcba-113">Exempel 2: Ladda upp alla filer under den aktuella mappen</span><span class="sxs-lookup"><span data-stu-id="9bcba-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzureStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="9bcba-114">I det här kommandot används den grundläggande Windows PowerShell-cmdleten Get-ChildItem för att hämta alla filer i den aktuella mappen och i undermappar och skickar dem till den aktuella cmdleten med operatören.</span><span class="sxs-lookup"><span data-stu-id="9bcba-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9bcba-115">Cmdleten **set-AzureStorageBlobContent** laddar upp filerna till behållaren med namnet ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="9bcba-115">The **Set-AzureStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="9bcba-116">Exempel 3: Skriv över en befintlig BLOB</span><span class="sxs-lookup"><span data-stu-id="9bcba-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzureStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="9bcba-117">Det här kommandot hämtar blobben med namnet Planning2015 i ContosoUploads-behållaren genom att använda Get-AzureStorageBlob cmdlet och sedan överföra denna blob till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9bcba-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzureStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="9bcba-118">Kommandot laddar upp filen med namnet ContosoPlanning som Planning2015.</span><span class="sxs-lookup"><span data-stu-id="9bcba-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="9bcba-119">Det här kommandot anger inte parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="9bcba-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="9bcba-120">Med kommandot uppmanas du att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="9bcba-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="9bcba-121">Om du bekräftar kommandot skriver cmdleten över den befintliga blobben.</span><span class="sxs-lookup"><span data-stu-id="9bcba-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="9bcba-122">Exempel 4: Ladda upp en fil till en behållare med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="9bcba-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container "ContosoUpload*" | Set-AzureStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="9bcba-123">Det här kommandot hämtar behållaren som börjar med strängen ContosoUpload med hjälp av cmdleten **Get-AzureStorageContainer** och överför sedan blobben till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9bcba-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzureStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="9bcba-124">Kommandot laddar upp filen med namnet ContosoPlanning som Planning2015.</span><span class="sxs-lookup"><span data-stu-id="9bcba-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="9bcba-125">Exempel 5: Ladda upp en fil till Page BLOB med metadata och PremiumPageBlobTier som P10</span><span class="sxs-lookup"><span data-stu-id="9bcba-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="9bcba-126">Det första kommandot skapar en hash-tabell som innehåller metadata för en blob och lagrar denna hash-tabell i $Metadata variabeln.</span><span class="sxs-lookup"><span data-stu-id="9bcba-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>

<span data-ttu-id="9bcba-127">Det andra kommandot laddar upp filen med namnet ContosoPlanning till behållaren med namnet ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="9bcba-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="9bcba-128">Blobben innehåller metadata som lagras i $Metadata och har PremiumPageBlobTier som P10.</span><span class="sxs-lookup"><span data-stu-id="9bcba-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

## <span data-ttu-id="9bcba-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9bcba-129">PARAMETERS</span></span>

### <span data-ttu-id="9bcba-130">-BLOB</span><span class="sxs-lookup"><span data-stu-id="9bcba-130">-Blob</span></span>
<span data-ttu-id="9bcba-131">Anger namnet på en blob.</span><span class="sxs-lookup"><span data-stu-id="9bcba-131">Specifies the name of a blob.</span></span>
<span data-ttu-id="9bcba-132">Denna cmdlet laddar upp en fil till den Azure Storage blob som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="9bcba-132">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="9bcba-133">-BlobType</span><span class="sxs-lookup"><span data-stu-id="9bcba-133">-BlobType</span></span>
<span data-ttu-id="9bcba-134">Anger typen för blobben som denna cmdlet laddar upp.</span><span class="sxs-lookup"><span data-stu-id="9bcba-134">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="9bcba-135">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="9bcba-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9bcba-136">Spärrade</span><span class="sxs-lookup"><span data-stu-id="9bcba-136">Block</span></span>
- <span data-ttu-id="9bcba-137">Mallsida</span><span class="sxs-lookup"><span data-stu-id="9bcba-137">Page</span></span>

<span data-ttu-id="9bcba-138">Standardvärdet är block.</span><span class="sxs-lookup"><span data-stu-id="9bcba-138">The default value is Block.</span></span>

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

### <span data-ttu-id="9bcba-139">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9bcba-139">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9bcba-140">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="9bcba-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9bcba-141">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="9bcba-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9bcba-142">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="9bcba-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9bcba-143">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="9bcba-143">-CloudBlob</span></span>
<span data-ttu-id="9bcba-144">Anger ett **CloudBlob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="9bcba-144">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="9bcba-145">För att hämta ett **CloudBlob** -objekt, Använd cmdleten Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="9bcba-145">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="9bcba-146">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="9bcba-146">-CloudBlobContainer</span></span>
<span data-ttu-id="9bcba-147">Anger ett **CloudBlobContainer** -objekt från klient bibliotek för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="9bcba-147">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="9bcba-148">Denna cmdlet laddar upp innehåll till en BLOB i behållaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="9bcba-148">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="9bcba-149">För att hämta ett **CloudBlobContainer** -objekt, Använd cmdleten Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="9bcba-149">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="9bcba-150">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9bcba-150">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9bcba-151">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="9bcba-151">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9bcba-152">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="9bcba-152">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9bcba-153">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="9bcba-153">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9bcba-154">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="9bcba-154">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9bcba-155">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="9bcba-155">The default value is 10.</span></span>

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

### <span data-ttu-id="9bcba-156">-Container</span><span class="sxs-lookup"><span data-stu-id="9bcba-156">-Container</span></span>
<span data-ttu-id="9bcba-157">Anger namnet på en behållare.</span><span class="sxs-lookup"><span data-stu-id="9bcba-157">Specifies the name of a container.</span></span>
<span data-ttu-id="9bcba-158">Denna cmdlet laddar upp en fil till en BLOB i behållaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="9bcba-158">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="9bcba-159">-Kontext</span><span class="sxs-lookup"><span data-stu-id="9bcba-159">-Context</span></span>
<span data-ttu-id="9bcba-160">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="9bcba-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9bcba-161">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="9bcba-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9bcba-162">-Fil</span><span class="sxs-lookup"><span data-stu-id="9bcba-162">-File</span></span>
<span data-ttu-id="9bcba-163">Anger en lokal fil Sök väg för en fil som ska laddas upp som BLOB-innehåll.</span><span class="sxs-lookup"><span data-stu-id="9bcba-163">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="9bcba-164">-Force</span><span class="sxs-lookup"><span data-stu-id="9bcba-164">-Force</span></span>
<span data-ttu-id="9bcba-165">Anger att denna cmdlet skriver över en befintlig BLOB utan att be dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="9bcba-165">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="9bcba-166">-Metadata</span><span class="sxs-lookup"><span data-stu-id="9bcba-166">-Metadata</span></span>
<span data-ttu-id="9bcba-167">Anger metadata för den uppladdade blobben.</span><span class="sxs-lookup"><span data-stu-id="9bcba-167">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="9bcba-168">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="9bcba-168">-PremiumPageBlobTier</span></span>
<span data-ttu-id="9bcba-169">BLOB Tier</span><span class="sxs-lookup"><span data-stu-id="9bcba-169">Page Blob Tier</span></span>

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

### <span data-ttu-id="9bcba-170">-Egenskaper</span><span class="sxs-lookup"><span data-stu-id="9bcba-170">-Properties</span></span>
<span data-ttu-id="9bcba-171">Anger egenskaper för den uppladdade blobben.</span><span class="sxs-lookup"><span data-stu-id="9bcba-171">Specifies properties for the uploaded blob.</span></span>

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

### <span data-ttu-id="9bcba-172">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9bcba-172">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9bcba-173">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="9bcba-173">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="9bcba-174">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="9bcba-174">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="9bcba-175">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9bcba-175">-Confirm</span></span>
<span data-ttu-id="9bcba-176">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9bcba-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bcba-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bcba-177">-WhatIf</span></span>
<span data-ttu-id="9bcba-178">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9bcba-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bcba-179">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9bcba-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bcba-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bcba-180">CommonParameters</span></span>
<span data-ttu-id="9bcba-181">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bcba-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bcba-182">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bcba-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bcba-183">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9bcba-183">INPUTS</span></span>

### <span data-ttu-id="9bcba-184">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9bcba-184">IStorageContext</span></span>

<span data-ttu-id="9bcba-185">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="9bcba-185">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="9bcba-186">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9bcba-186">OUTPUTS</span></span>

### <span data-ttu-id="9bcba-187">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9bcba-187">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="9bcba-188">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9bcba-188">NOTES</span></span>

## <span data-ttu-id="9bcba-189">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9bcba-189">RELATED LINKS</span></span>

[<span data-ttu-id="9bcba-190">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="9bcba-190">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="9bcba-191">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9bcba-191">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="9bcba-192">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9bcba-192">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
