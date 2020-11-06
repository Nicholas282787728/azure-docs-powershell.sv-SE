---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: ''
schema: 2.0.0
ms.openlocfilehash: f7b68be6981343d14f7d1d8530a0af3c3eee199c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572408"
---
# <span data-ttu-id="21580-101">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="21580-101">Get-AzureStorageBlob</span></span>

## <span data-ttu-id="21580-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="21580-102">SYNOPSIS</span></span>
<span data-ttu-id="21580-103">Visar blobbar i en behållare.</span><span class="sxs-lookup"><span data-stu-id="21580-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="21580-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="21580-104">SYNTAX</span></span>

### <span data-ttu-id="21580-105">BlobName (standard)</span><span class="sxs-lookup"><span data-stu-id="21580-105">BlobName (Default)</span></span>
```
Get-AzureStorageBlob [[-Blob] <String>] [-Container] <String> [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="21580-106">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="21580-106">BlobPrefix</span></span>
```
Get-AzureStorageBlob [-Prefix <String>] [-Container] <String> [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="21580-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="21580-107">DESCRIPTION</span></span>
<span data-ttu-id="21580-108">Cmdleten **Get-AzureStorageBlob** visar blobbar i den angivna behållaren i ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="21580-108">The **Get-AzureStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="21580-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="21580-109">EXAMPLES</span></span>

### <span data-ttu-id="21580-110">Exempel 1: skaffa en BLOB per BLOB-namn</span><span class="sxs-lookup"><span data-stu-id="21580-110">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="21580-111">Det här kommandot använder ett BLOB-namn och ett jokertecken för att hämta en blob.</span><span class="sxs-lookup"><span data-stu-id="21580-111">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="21580-112">Exempel 2: skaffa en BLOB genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="21580-112">Example 2: Get a blob by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container* | Get-AzureStorageBlob
```

<span data-ttu-id="21580-113">Det här kommandot använder pipeline för att skaffa en blob.</span><span class="sxs-lookup"><span data-stu-id="21580-113">This command uses the pipeline to get a blob.</span></span>

### <span data-ttu-id="21580-114">Exempel 3: skaffa en BLOB efter namn</span><span class="sxs-lookup"><span data-stu-id="21580-114">Example 3: Get a blob by name prefix</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="21580-115">Det här kommandot använder ett namn-prefix för att hämta en blob.</span><span class="sxs-lookup"><span data-stu-id="21580-115">This command uses a name prefix to get a blob.</span></span>

### <span data-ttu-id="21580-116">Exempel 4: list-BLOB i flera batchar</span><span class="sxs-lookup"><span data-stu-id="21580-116">Example 4: List blobs in multiple batches</span></span>
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzureStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

<span data-ttu-id="21580-117">I det här exemplet används parametrarna *MaxCount* och *ContinuationToken* för att lista Azure Storage BLOB i flera batchar.</span><span class="sxs-lookup"><span data-stu-id="21580-117">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="21580-118">De första fyra kommandona tilldelar värden till variabler som ska användas i exemplet.</span><span class="sxs-lookup"><span data-stu-id="21580-118">The first four commands assign values to variables to use in the example.</span></span>

<span data-ttu-id="21580-119">Det femte kommandot anger en **do-while-** sats som använder cmdleten **Get-AzureStorageBlob** för att hämta blobs.</span><span class="sxs-lookup"><span data-stu-id="21580-119">The fifth command specifies a **Do-While** statement that uses the **Get-AzureStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="21580-120">Uttrycket innehåller det tilläggs token som lagras i $Token variabeln.</span><span class="sxs-lookup"><span data-stu-id="21580-120">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="21580-121">$Token ändrar värde när slingan körs.</span><span class="sxs-lookup"><span data-stu-id="21580-121">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="21580-122">Om du vill ha mer information skriver du `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="21580-122">For more information, type `Get-Help About_Do`.</span></span>

<span data-ttu-id="21580-123">Det sista kommandot använder kommandot **ECHO** för att visa summan.</span><span class="sxs-lookup"><span data-stu-id="21580-123">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="21580-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="21580-124">PARAMETERS</span></span>

### <span data-ttu-id="21580-125">-BLOB</span><span class="sxs-lookup"><span data-stu-id="21580-125">-Blob</span></span>
<span data-ttu-id="21580-126">Anger ett namn eller namn mönster som kan användas för sökning med jokertecken.</span><span class="sxs-lookup"><span data-stu-id="21580-126">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="21580-127">Om inget BLOB-namn anges visar cmdleten alla blobbar i den angivna behållaren.</span><span class="sxs-lookup"><span data-stu-id="21580-127">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="21580-128">Om du anger ett värde för den här parametern visar cmdleten alla blobbar med namn som matchar den här parametern.</span><span class="sxs-lookup"><span data-stu-id="21580-128">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span>

```yaml
Type: String
Parameter Sets: BlobName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21580-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="21580-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="21580-130">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="21580-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="21580-131">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="21580-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="21580-132">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="21580-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="21580-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="21580-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="21580-134">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="21580-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="21580-135">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="21580-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="21580-136">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="21580-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="21580-137">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="21580-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="21580-138">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="21580-138">The default value is 10.</span></span>

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

### <span data-ttu-id="21580-139">-Container</span><span class="sxs-lookup"><span data-stu-id="21580-139">-Container</span></span>
<span data-ttu-id="21580-140">Anger namnet på behållaren.</span><span class="sxs-lookup"><span data-stu-id="21580-140">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21580-141">-Kontext</span><span class="sxs-lookup"><span data-stu-id="21580-141">-Context</span></span>
<span data-ttu-id="21580-142">Anger det Azure Storage-konto som du vill få en lista över blobs från.</span><span class="sxs-lookup"><span data-stu-id="21580-142">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="21580-143">Du kan använda New-AzureStorageContext cmdlet för att skapa en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="21580-143">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="21580-144">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="21580-144">-ContinuationToken</span></span>
<span data-ttu-id="21580-145">Anger ett fortsättnings-token för BLOB-listan.</span><span class="sxs-lookup"><span data-stu-id="21580-145">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="21580-146">Använd den här parametern och parametern *MaxCount* om du vill visa blobs i flera batchar.</span><span class="sxs-lookup"><span data-stu-id="21580-146">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21580-147">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="21580-147">-MaxCount</span></span>
<span data-ttu-id="21580-148">Anger det maximala antalet objekt som denna cmdlet returnerar.</span><span class="sxs-lookup"><span data-stu-id="21580-148">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="21580-149">-Prefix</span><span class="sxs-lookup"><span data-stu-id="21580-149">-Prefix</span></span>
<span data-ttu-id="21580-150">Anger ett prefix för de BLOB-namn som du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="21580-150">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="21580-151">Den här parametern stöder inte användning av vanliga uttryck eller jokertecken för att söka.</span><span class="sxs-lookup"><span data-stu-id="21580-151">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="21580-152">Det innebär att om behållaren bara innehåller blobbar med namnet "My", "MyBlob1" och "MyBlob2" och du anger "-prefix My \*", returnerar cmdleten inga blob.</span><span class="sxs-lookup"><span data-stu-id="21580-152">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="21580-153">Men om du anger "prefixet My" returnerar cmdleten "My", "MyBlob1" och "MyBlob2".</span><span class="sxs-lookup"><span data-stu-id="21580-153">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

```yaml
Type: String
Parameter Sets: BlobPrefix
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21580-154">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="21580-154">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="21580-155">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="21580-155">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="21580-156">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="21580-156">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="21580-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21580-157">CommonParameters</span></span>
<span data-ttu-id="21580-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21580-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21580-159">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21580-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21580-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="21580-160">INPUTS</span></span>

## <span data-ttu-id="21580-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="21580-161">OUTPUTS</span></span>

### <span data-ttu-id="21580-162">AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="21580-162">AzureStorageBlob</span></span>

## <span data-ttu-id="21580-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="21580-163">NOTES</span></span>
* <span data-ttu-id="21580-164">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="21580-164">SYNOPSIS</span></span>

## <span data-ttu-id="21580-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="21580-165">RELATED LINKS</span></span>

[<span data-ttu-id="21580-166">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="21580-166">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="21580-167">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="21580-167">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)

[<span data-ttu-id="21580-168">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="21580-168">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)


