---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: 388adccb9578c695055815ab6e6de5478958621f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521979"
---
# <span data-ttu-id="45b14-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="45b14-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="45b14-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45b14-102">SYNOPSIS</span></span>
<span data-ttu-id="45b14-103">Laddar upp en lokal fil till en Azure-lagrings-blob.</span><span class="sxs-lookup"><span data-stu-id="45b14-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="45b14-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45b14-104">SYNTAX</span></span>

### <span data-ttu-id="45b14-105">SendManual (standard)</span><span class="sxs-lookup"><span data-stu-id="45b14-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>]
 [-StandardBlobTier <String>] [-EncryptionScope <String>] [-Force] [-AsJob] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45b14-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="45b14-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-EncryptionScope <String>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45b14-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="45b14-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-EncryptionScope <String>] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45b14-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45b14-108">DESCRIPTION</span></span>
<span data-ttu-id="45b14-109">Cmdleten **set-AzStorageBlobContent** laddar upp en lokal fil till en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="45b14-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="45b14-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45b14-110">EXAMPLES</span></span>

### <span data-ttu-id="45b14-111">Exempel 1: Ladda upp en namngiven fil</span><span class="sxs-lookup"><span data-stu-id="45b14-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="45b14-112">Det här kommandot laddar upp filen med namnet PlanningData till en blob som heter Planning2015.</span><span class="sxs-lookup"><span data-stu-id="45b14-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="45b14-113">Exempel 2: Ladda upp alla filer under den aktuella mappen</span><span class="sxs-lookup"><span data-stu-id="45b14-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="45b14-114">I det här kommandot används den grundläggande Windows PowerShell-cmdleten Get-ChildItem för att hämta alla filer i den aktuella mappen och i undermappar och skickar dem till den aktuella cmdleten med operatören.</span><span class="sxs-lookup"><span data-stu-id="45b14-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="45b14-115">Cmdleten **set-AzStorageBlobContent** laddar upp filerna till behållaren med namnet ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="45b14-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="45b14-116">Exempel 3: Skriv över en befintlig BLOB</span><span class="sxs-lookup"><span data-stu-id="45b14-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="45b14-117">Det här kommandot hämtar blobben med namnet Planning2015 i ContosoUploads-behållaren genom att använda Get-AzStorageBlob cmdlet och sedan överföra denna blob till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45b14-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="45b14-118">Kommandot laddar upp filen med namnet ContosoPlanning som Planning2015.</span><span class="sxs-lookup"><span data-stu-id="45b14-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="45b14-119">Det här kommandot anger inte parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="45b14-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="45b14-120">Med kommandot uppmanas du att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="45b14-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="45b14-121">Om du bekräftar kommandot skriver cmdleten över den befintliga blobben.</span><span class="sxs-lookup"><span data-stu-id="45b14-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="45b14-122">Exempel 4: Ladda upp en fil till en behållare med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="45b14-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="45b14-123">Det här kommandot hämtar behållaren som börjar med strängen ContosoUpload med hjälp av cmdleten **Get-AzStorageContainer** och överför sedan blobben till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45b14-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="45b14-124">Kommandot laddar upp filen med namnet ContosoPlanning som Planning2015.</span><span class="sxs-lookup"><span data-stu-id="45b14-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="45b14-125">Exempel 5: Ladda upp en fil till Page BLOB med metadata och PremiumPageBlobTier som P10</span><span class="sxs-lookup"><span data-stu-id="45b14-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="45b14-126">Det första kommandot skapar en hash-tabell som innehåller metadata för en blob och lagrar denna hash-tabell i $Metadata variabeln.</span><span class="sxs-lookup"><span data-stu-id="45b14-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="45b14-127">Det andra kommandot laddar upp filen med namnet ContosoPlanning till behållaren med namnet ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="45b14-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="45b14-128">Blobben innehåller metadata som lagras i $Metadata och har PremiumPageBlobTier som P10.</span><span class="sxs-lookup"><span data-stu-id="45b14-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="45b14-129">Exempel 6: Ladda upp en fil till blob med angivna BLOB-egenskaper och ange StandardBlobTier som coolt</span><span class="sxs-lookup"><span data-stu-id="45b14-129">Example 6: Upload a file to blob with specified blob properties, and set StandardBlobTier as Cool</span></span>
```
PS C:\> $filepath = "c:\temp\index.html"
PS C:\> Set-AzStorageBlobContent -File $filepath -Container "contosouploads" -Properties @{"ContentType" = [System.Web.MimeMapping]::GetMimeMapping($filepath); "ContentMD5" = "i727sP7HigloQDsqadNLHw=="} -StandardBlobTier Cool

   AccountName: storageaccountname, ContainerName: contosouploads

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
index.html           BlockBlob 403116          text/html                      2020-09-22 08:06:53Z Cool                                    False
```

<span data-ttu-id="45b14-130">Det här kommandot laddar upp filen c:\temp\index.html till behållaren med namnet contosouploads med angivna BLOB-egenskaper och anger StandardBlobTier som coolt.</span><span class="sxs-lookup"><span data-stu-id="45b14-130">This command uploads the file c:\temp\index.html to the container named contosouploads with specified blob properties, and set StandardBlobTier as Cool.</span></span>
<span data-ttu-id="45b14-131">Det här kommandot får värdet för ContentType angett för BLOB-egenskaper av [system. Web. MimeMapping]:: GetMimeMapping () API.</span><span class="sxs-lookup"><span data-stu-id="45b14-131">This command gets ContentType value set to blob properties by [System.Web.MimeMapping]::GetMimeMapping() API.</span></span>

### <span data-ttu-id="45b14-132">Exempel 7: Ladda upp en fil till en blob med krypterings omfattning</span><span class="sxs-lookup"><span data-stu-id="45b14-132">Example 7: Upload a file to a blob with Encryption Scope</span></span>
```
PS C:\> $blob = Set-AzStorageBlobContent  -File "mylocalfile" -Container "mycontainer" -Blob "myblob"  -EncryptionScope "myencryptscope"

PS C:\> $blob.BlobProperties.EncryptionScope
myencryptscope
```

<span data-ttu-id="45b14-133">Det här kommandot laddar upp en fil till en blob med krypterings omfattning.</span><span class="sxs-lookup"><span data-stu-id="45b14-133">This command  uploads a file to a blob with Encryption Scope.</span></span>

## <span data-ttu-id="45b14-134">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45b14-134">PARAMETERS</span></span>

### <span data-ttu-id="45b14-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45b14-135">-AsJob</span></span>
<span data-ttu-id="45b14-136">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="45b14-136">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="45b14-137">-BLOB</span><span class="sxs-lookup"><span data-stu-id="45b14-137">-Blob</span></span>
<span data-ttu-id="45b14-138">Anger namnet på en blob.</span><span class="sxs-lookup"><span data-stu-id="45b14-138">Specifies the name of a blob.</span></span>
<span data-ttu-id="45b14-139">Denna cmdlet laddar upp en fil till den Azure Storage blob som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="45b14-139">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b14-140">-BlobType</span><span class="sxs-lookup"><span data-stu-id="45b14-140">-BlobType</span></span>
<span data-ttu-id="45b14-141">Anger typen för blobben som denna cmdlet laddar upp.</span><span class="sxs-lookup"><span data-stu-id="45b14-141">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="45b14-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="45b14-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="45b14-143">Spärrade</span><span class="sxs-lookup"><span data-stu-id="45b14-143">Block</span></span>
- <span data-ttu-id="45b14-144">Mallsida</span><span class="sxs-lookup"><span data-stu-id="45b14-144">Page</span></span>
- <span data-ttu-id="45b14-145">Lägg till standardvärdet är block.</span><span class="sxs-lookup"><span data-stu-id="45b14-145">Append The default value is Block.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Block, Page, Append

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b14-146">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="45b14-146">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="45b14-147">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="45b14-147">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="45b14-148">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="45b14-148">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="45b14-149">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="45b14-149">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="45b14-150">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="45b14-150">-CloudBlob</span></span>
<span data-ttu-id="45b14-151">Anger ett **CloudBlob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="45b14-151">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="45b14-152">För att hämta ett **CloudBlob** -objekt, Använd cmdleten Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="45b14-152">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="45b14-153">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="45b14-153">-CloudBlobContainer</span></span>
<span data-ttu-id="45b14-154">Anger ett **CloudBlobContainer** -objekt från klient bibliotek för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="45b14-154">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="45b14-155">Denna cmdlet laddar upp innehåll till en BLOB i behållaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="45b14-155">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="45b14-156">För att hämta ett **CloudBlobContainer** -objekt, Använd cmdleten Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="45b14-156">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="45b14-157">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="45b14-157">-ConcurrentTaskCount</span></span>
<span data-ttu-id="45b14-158">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="45b14-158">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="45b14-159">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="45b14-159">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="45b14-160">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="45b14-160">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="45b14-161">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="45b14-161">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="45b14-162">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="45b14-162">The default value is 10.</span></span>

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

### <span data-ttu-id="45b14-163">-Container</span><span class="sxs-lookup"><span data-stu-id="45b14-163">-Container</span></span>
<span data-ttu-id="45b14-164">Anger namnet på en behållare.</span><span class="sxs-lookup"><span data-stu-id="45b14-164">Specifies the name of a container.</span></span>
<span data-ttu-id="45b14-165">Denna cmdlet laddar upp en fil till en BLOB i behållaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="45b14-165">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b14-166">-Kontext</span><span class="sxs-lookup"><span data-stu-id="45b14-166">-Context</span></span>
<span data-ttu-id="45b14-167">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="45b14-167">Specifies an Azure storage context.</span></span>
<span data-ttu-id="45b14-168">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="45b14-168">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="45b14-169">Om du vill använda en lagrings kontext som skapats från en SAS-token utan Läs behörighet behöver du tilläggs parametern för att hoppa över kontroll av BLOB-existens.</span><span class="sxs-lookup"><span data-stu-id="45b14-169">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existence.</span></span>

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

### <span data-ttu-id="45b14-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b14-170">-DefaultProfile</span></span>
<span data-ttu-id="45b14-171">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="45b14-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45b14-172">-EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="45b14-172">-EncryptionScope</span></span>
<span data-ttu-id="45b14-173">Krypterings omfång som ska användas vid begäran till blobben.</span><span class="sxs-lookup"><span data-stu-id="45b14-173">Encryption scope to be used when making requests to the blob.</span></span>

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

### <span data-ttu-id="45b14-174">-Fil</span><span class="sxs-lookup"><span data-stu-id="45b14-174">-File</span></span>
<span data-ttu-id="45b14-175">Anger en lokal fil Sök väg för en fil som ska laddas upp som BLOB-innehåll.</span><span class="sxs-lookup"><span data-stu-id="45b14-175">Specifies a local file path for a file to upload as blob content.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45b14-176">-Force</span><span class="sxs-lookup"><span data-stu-id="45b14-176">-Force</span></span>
<span data-ttu-id="45b14-177">Anger att denna cmdlet skriver över en befintlig BLOB utan att be dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="45b14-177">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="45b14-178">-Metadata</span><span class="sxs-lookup"><span data-stu-id="45b14-178">-Metadata</span></span>
<span data-ttu-id="45b14-179">Anger metadata för den uppladdade blobben.</span><span class="sxs-lookup"><span data-stu-id="45b14-179">Specifies metadata for the uploaded blob.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b14-180">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="45b14-180">-PremiumPageBlobTier</span></span>
<span data-ttu-id="45b14-181">BLOB Tier</span><span class="sxs-lookup"><span data-stu-id="45b14-181">Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60, P70, P80

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b14-182">-Egenskaper</span><span class="sxs-lookup"><span data-stu-id="45b14-182">-Properties</span></span>
<span data-ttu-id="45b14-183">Anger egenskaper för den uppladdade blobben.</span><span class="sxs-lookup"><span data-stu-id="45b14-183">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="45b14-184">De egenskaper som stöds är: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="45b14-184">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b14-185">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="45b14-185">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="45b14-186">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="45b14-186">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="45b14-187">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="45b14-187">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="45b14-188">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="45b14-188">-StandardBlobTier</span></span>
<span data-ttu-id="45b14-189">Block Blob Tier, giltiga värden är varm/coolt/arkiverat.</span><span class="sxs-lookup"><span data-stu-id="45b14-189">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="45b14-190">Se detalj i https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="45b14-190">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool, Archive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b14-191">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="45b14-191">-Confirm</span></span>
<span data-ttu-id="45b14-192">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45b14-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45b14-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45b14-193">-WhatIf</span></span>
<span data-ttu-id="45b14-194">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="45b14-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45b14-195">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="45b14-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45b14-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b14-196">CommonParameters</span></span>
<span data-ttu-id="45b14-197">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45b14-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b14-198">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45b14-198">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b14-199">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45b14-199">INPUTS</span></span>

### <span data-ttu-id="45b14-200">System. String</span><span class="sxs-lookup"><span data-stu-id="45b14-200">System.String</span></span>

### <span data-ttu-id="45b14-201">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="45b14-201">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="45b14-202">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="45b14-202">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="45b14-203">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="45b14-203">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="45b14-204">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45b14-204">OUTPUTS</span></span>

### <span data-ttu-id="45b14-205">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="45b14-205">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="45b14-206">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45b14-206">NOTES</span></span>

## <span data-ttu-id="45b14-207">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45b14-207">RELATED LINKS</span></span>

[<span data-ttu-id="45b14-208">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="45b14-208">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="45b14-209">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="45b14-209">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="45b14-210">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="45b14-210">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
