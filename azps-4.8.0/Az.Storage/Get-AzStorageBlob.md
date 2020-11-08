---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
ms.openlocfilehash: 44c14b1f5aa8426bfb78205fa66a53d7db7e3440
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258510"
---
# <span data-ttu-id="a2c99-101">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a2c99-101">Get-AzStorageBlob</span></span>

## <span data-ttu-id="a2c99-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a2c99-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c99-103">Visar blobbar i en behållare.</span><span class="sxs-lookup"><span data-stu-id="a2c99-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="a2c99-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a2c99-104">SYNTAX</span></span>

### <span data-ttu-id="a2c99-105">BlobName (standard)</span><span class="sxs-lookup"><span data-stu-id="a2c99-105">BlobName (Default)</span></span>
```
Get-AzStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2c99-106">SingleBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="a2c99-106">SingleBlobSnapshotTime</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -SnapshotTime <DateTimeOffset>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a2c99-107">SingleBlobVersionID</span><span class="sxs-lookup"><span data-stu-id="a2c99-107">SingleBlobVersionID</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -VersionId <String>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a2c99-108">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="a2c99-108">BlobPrefix</span></span>
```
Get-AzStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-IncludeVersion]
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a2c99-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a2c99-109">DESCRIPTION</span></span>
<span data-ttu-id="a2c99-110">Cmdleten **Get-AzStorageBlob** visar blobbar i den angivna behållaren i ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="a2c99-110">The **Get-AzStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="a2c99-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a2c99-111">EXAMPLES</span></span>

### <span data-ttu-id="a2c99-112">Exempel 1: skaffa en BLOB per BLOB-namn</span><span class="sxs-lookup"><span data-stu-id="a2c99-112">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="a2c99-113">Det här kommandot använder ett BLOB-namn och ett jokertecken för att hämta en blob.</span><span class="sxs-lookup"><span data-stu-id="a2c99-113">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="a2c99-114">Exempel 2: skaffa blobs i en container med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="a2c99-114">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Name container* | Get-AzStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

<span data-ttu-id="a2c99-115">Det här kommandot använder pipeline för att hämta alla blobbar (inklusive BLOB i borttaget) i en behållare.</span><span class="sxs-lookup"><span data-stu-id="a2c99-115">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="a2c99-116">Exempel 3: Hämta blobs efter namn</span><span class="sxs-lookup"><span data-stu-id="a2c99-116">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="a2c99-117">Det här kommandot använder ett namn prefix för att hämta blob.</span><span class="sxs-lookup"><span data-stu-id="a2c99-117">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="a2c99-118">Exempel 4: list-BLOB i flera batchar</span><span class="sxs-lookup"><span data-stu-id="a2c99-118">Example 4: List blobs in multiple batches</span></span>
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

<span data-ttu-id="a2c99-119">I det här exemplet används parametrarna *MaxCount* och *ContinuationToken* för att lista Azure Storage BLOB i flera batchar.</span><span class="sxs-lookup"><span data-stu-id="a2c99-119">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="a2c99-120">De första fyra kommandona tilldelar värden till variabler som ska användas i exemplet.</span><span class="sxs-lookup"><span data-stu-id="a2c99-120">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="a2c99-121">Det femte kommandot anger en **do-while-** sats som använder cmdleten **Get-AzStorageBlob** för att hämta blobs.</span><span class="sxs-lookup"><span data-stu-id="a2c99-121">The fifth command specifies a **Do-While** statement that uses the **Get-AzStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="a2c99-122">Uttrycket innehåller det tilläggs token som lagras i $Token variabeln.</span><span class="sxs-lookup"><span data-stu-id="a2c99-122">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="a2c99-123">$Token ändrar värde när slingan körs.</span><span class="sxs-lookup"><span data-stu-id="a2c99-123">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="a2c99-124">Om du vill ha mer information skriver du `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="a2c99-124">For more information, type `Get-Help About_Do`.</span></span>
<span data-ttu-id="a2c99-125">Det sista kommandot använder kommandot **ECHO** för att visa summan.</span><span class="sxs-lookup"><span data-stu-id="a2c99-125">The final command uses the **Echo** command to display the total.</span></span>

### <span data-ttu-id="a2c99-126">Exempel 5: Hämta alla BLOB i en container inkluderar blob-version</span><span class="sxs-lookup"><span data-stu-id="a2c99-126">Example 5: Get all blobs in a container include blob version</span></span>
```
PS C:\>Get-AzStorageBlob -Container "containername"  -IncludeVersion 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot                                     False      2020-07-06T06:56:06.2432658Z  
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False                                    
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot                                     False      2020-07-06T06:56:06.8598431Z *  
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z  
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:35Z Hot                                     False      2020-07-03T16:19:35.2381110Z *
```

<span data-ttu-id="a2c99-127">Det här kommandot får alla blobbar i en container inklusive BLOB-versionen.</span><span class="sxs-lookup"><span data-stu-id="a2c99-127">This command gets all blobs in a container include blob version.</span></span>

### <span data-ttu-id="a2c99-128">Exempel 6: skaffa en enda blob-version</span><span class="sxs-lookup"><span data-stu-id="a2c99-128">Example 6: Get a single blob version</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z" 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z
```

<span data-ttu-id="a2c99-129">Det här kommandot får en verion med VersionId.</span><span class="sxs-lookup"><span data-stu-id="a2c99-129">This command gets a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="a2c99-130">Exempel 7: skaffa en enda BLOB-stillbild</span><span class="sxs-lookup"><span data-stu-id="a2c99-130">Example 7: Get a single blob snapshot</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False
```

<span data-ttu-id="a2c99-131">Det här kommandot får en enda blobbar med SnapshotTime.</span><span class="sxs-lookup"><span data-stu-id="a2c99-131">This command gets a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="a2c99-132">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a2c99-132">PARAMETERS</span></span>

### <span data-ttu-id="a2c99-133">-BLOB</span><span class="sxs-lookup"><span data-stu-id="a2c99-133">-Blob</span></span>
<span data-ttu-id="a2c99-134">Anger ett namn eller namn mönster som kan användas för sökning med jokertecken.</span><span class="sxs-lookup"><span data-stu-id="a2c99-134">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="a2c99-135">Om inget BLOB-namn anges visar cmdleten alla blobbar i den angivna behållaren.</span><span class="sxs-lookup"><span data-stu-id="a2c99-135">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="a2c99-136">Om du anger ett värde för den här parametern visar cmdleten alla blobbar med namn som matchar den här parametern.</span><span class="sxs-lookup"><span data-stu-id="a2c99-136">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span> <span data-ttu-id="a2c99-137">Den här parametern stöder jokertecken var som helst i strängen.</span><span class="sxs-lookup"><span data-stu-id="a2c99-137">This parameter supports wildcards anywhere in the string.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SingleBlobSnapshotTime, SingleBlobVersionID
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c99-138">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a2c99-138">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a2c99-139">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="a2c99-139">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a2c99-140">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="a2c99-140">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a2c99-141">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="a2c99-141">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a2c99-142">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a2c99-142">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a2c99-143">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="a2c99-143">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a2c99-144">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="a2c99-144">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a2c99-145">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="a2c99-145">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a2c99-146">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="a2c99-146">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a2c99-147">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="a2c99-147">The default value is 10.</span></span>

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

### <span data-ttu-id="a2c99-148">-Container</span><span class="sxs-lookup"><span data-stu-id="a2c99-148">-Container</span></span>
<span data-ttu-id="a2c99-149">Anger namnet på behållaren.</span><span class="sxs-lookup"><span data-stu-id="a2c99-149">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c99-150">-Kontext</span><span class="sxs-lookup"><span data-stu-id="a2c99-150">-Context</span></span>
<span data-ttu-id="a2c99-151">Anger det Azure Storage-konto som du vill få en lista över blobs från.</span><span class="sxs-lookup"><span data-stu-id="a2c99-151">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="a2c99-152">Du kan använda New-AzStorageContext cmdlet för att skapa en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="a2c99-152">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="a2c99-153">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="a2c99-153">-ContinuationToken</span></span>
<span data-ttu-id="a2c99-154">Anger ett fortsättnings-token för BLOB-listan.</span><span class="sxs-lookup"><span data-stu-id="a2c99-154">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="a2c99-155">Använd den här parametern och parametern *MaxCount* om du vill visa blobs i flera batchar.</span><span class="sxs-lookup"><span data-stu-id="a2c99-155">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c99-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c99-156">-DefaultProfile</span></span>
<span data-ttu-id="a2c99-157">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a2c99-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2c99-158">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="a2c99-158">-IncludeDeleted</span></span>
<span data-ttu-id="a2c99-159">Ta bort blob som standard tar inte bort blob.</span><span class="sxs-lookup"><span data-stu-id="a2c99-159">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

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

### <span data-ttu-id="a2c99-160">-IncludeVersion</span><span class="sxs-lookup"><span data-stu-id="a2c99-160">-IncludeVersion</span></span>
<span data-ttu-id="a2c99-161">BLOB-versioner visas bara om den här parametern finns, som standard innehåller endast BLOB-versioner.</span><span class="sxs-lookup"><span data-stu-id="a2c99-161">Blob versions will be listed only if this parameter is present, by default get blob won't include blob versions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c99-162">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="a2c99-162">-MaxCount</span></span>
<span data-ttu-id="a2c99-163">Anger det maximala antalet objekt som denna cmdlet returnerar.</span><span class="sxs-lookup"><span data-stu-id="a2c99-163">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="a2c99-164">-Prefix</span><span class="sxs-lookup"><span data-stu-id="a2c99-164">-Prefix</span></span>
<span data-ttu-id="a2c99-165">Anger ett prefix för de BLOB-namn som du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="a2c99-165">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="a2c99-166">Den här parametern stöder inte användning av vanliga uttryck eller jokertecken för att söka.</span><span class="sxs-lookup"><span data-stu-id="a2c99-166">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="a2c99-167">Det innebär att om behållaren bara innehåller blobbar med namnet "My", "MyBlob1" och "MyBlob2" och du anger "-prefix My \*", returnerar cmdleten inga blob.</span><span class="sxs-lookup"><span data-stu-id="a2c99-167">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="a2c99-168">Men om du anger "prefixet My" returnerar cmdleten "My", "MyBlob1" och "MyBlob2".</span><span class="sxs-lookup"><span data-stu-id="a2c99-168">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c99-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a2c99-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a2c99-170">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="a2c99-170">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="a2c99-171">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="a2c99-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="a2c99-172">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="a2c99-172">-SnapshotTime</span></span>
<span data-ttu-id="a2c99-173">Blobb SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="a2c99-173">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: SingleBlobSnapshotTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c99-174">-VersionId</span><span class="sxs-lookup"><span data-stu-id="a2c99-174">-VersionId</span></span>
<span data-ttu-id="a2c99-175">Blobb VersionId</span><span class="sxs-lookup"><span data-stu-id="a2c99-175">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: SingleBlobVersionID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c99-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c99-176">CommonParameters</span></span>
<span data-ttu-id="a2c99-177">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2c99-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c99-178">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2c99-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c99-179">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a2c99-179">INPUTS</span></span>

### <span data-ttu-id="a2c99-180">System. String</span><span class="sxs-lookup"><span data-stu-id="a2c99-180">System.String</span></span>

### <span data-ttu-id="a2c99-181">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a2c99-181">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a2c99-182">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a2c99-182">OUTPUTS</span></span>

### <span data-ttu-id="a2c99-183">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a2c99-183">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="a2c99-184">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a2c99-184">NOTES</span></span>

## <span data-ttu-id="a2c99-185">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a2c99-185">RELATED LINKS</span></span>

[<span data-ttu-id="a2c99-186">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a2c99-186">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="a2c99-187">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a2c99-187">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)

[<span data-ttu-id="a2c99-188">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a2c99-188">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)


