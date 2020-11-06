---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3b84deae0307114efa274cdfa6fc708d1b268ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572380"
---
# <span data-ttu-id="2e079-101">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="2e079-101">Get-AzureStorageFile</span></span>

## <span data-ttu-id="2e079-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2e079-102">SYNOPSIS</span></span>
<span data-ttu-id="2e079-103">Visar en lista över kataloger och filer för en sökväg.</span><span class="sxs-lookup"><span data-stu-id="2e079-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="2e079-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2e079-104">SYNTAX</span></span>

### <span data-ttu-id="2e079-105">Resurs namn (standard)</span><span class="sxs-lookup"><span data-stu-id="2e079-105">ShareName (Default)</span></span>
```
Get-AzureStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e079-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="2e079-106">Share</span></span>
```
Get-AzureStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2e079-107">Katalogen</span><span class="sxs-lookup"><span data-stu-id="2e079-107">Directory</span></span>
```
Get-AzureStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="2e079-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2e079-108">DESCRIPTION</span></span>
<span data-ttu-id="2e079-109">Cmdleten **Get-AzureStorageFile** innehåller en lista över kataloger och filer för den delning eller katalog som du anger.</span><span class="sxs-lookup"><span data-stu-id="2e079-109">The **Get-AzureStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="2e079-110">Ange parametern *Path* för att få en instans av en katalog eller fil på den angivna sökvägen.</span><span class="sxs-lookup"><span data-stu-id="2e079-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>

<span data-ttu-id="2e079-111">Denna cmdlet returnerar **AzureStorageFile** -och **AzureStorageDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2e079-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="2e079-112">Du kan använda egenskapen **IsDirectory** för att skilja mellan mappar och filer.</span><span class="sxs-lookup"><span data-stu-id="2e079-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="2e079-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2e079-113">EXAMPLES</span></span>

### <span data-ttu-id="2e079-114">Exempel 1: lista kataloger i en resurs</span><span class="sxs-lookup"><span data-stu-id="2e079-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName "share1" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

<span data-ttu-id="2e079-115">Det här kommandot listar bara katalogerna i avsnittet Dela ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="2e079-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="2e079-116">Den hämtar först både filer och kataloger, skickar dem till operatorn **WHERE** genom att använda pipeline-operatorn och ignorera sedan alla objekt vars typ inte är "CloudFileDirectory".</span><span class="sxs-lookup"><span data-stu-id="2e079-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "CloudFileDirectory".</span></span>

### <span data-ttu-id="2e079-117">Exempel 2: lista en fil katalog</span><span class="sxs-lookup"><span data-stu-id="2e079-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzureStorageFile
```

<span data-ttu-id="2e079-118">Det här kommandot listar filerna och mapparna i katalogen ContosoWorkingFolder under fliken Dela ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="2e079-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="2e079-119">Den först får katalog instansen och går sedan till cmdleten **Get-AzureStorageFile** för att lista katalogen.</span><span class="sxs-lookup"><span data-stu-id="2e079-119">It first gets the directory instance, and then pipelines it to the **Get-AzureStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="2e079-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2e079-120">PARAMETERS</span></span>

### <span data-ttu-id="2e079-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2e079-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2e079-122">Anger tids gräns för klient sidan i sekunder för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="2e079-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2e079-123">Om det föregående samtalet inte fungerar inom det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="2e079-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2e079-124">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="2e079-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2e079-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2e079-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2e079-126">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="2e079-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2e079-127">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="2e079-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2e079-128">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="2e079-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2e079-129">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="2e079-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2e079-130">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="2e079-130">The default value is 10.</span></span>

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

### <span data-ttu-id="2e079-131">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2e079-131">-Context</span></span>
<span data-ttu-id="2e079-132">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="2e079-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="2e079-133">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="2e079-133">To obtain a Storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e079-134">-Katalog</span><span class="sxs-lookup"><span data-stu-id="2e079-134">-Directory</span></span>
<span data-ttu-id="2e079-135">Anger en mapp som ett **CloudFileDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2e079-135">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="2e079-136">Denna cmdlet tar fram den mapp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="2e079-136">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="2e079-137">Använd New-AzureStorageDirectory cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="2e079-137">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="2e079-138">Du kan också använda cmdleten **Get-AzureStorageFile** för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="2e079-138">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e079-139">-Path</span><span class="sxs-lookup"><span data-stu-id="2e079-139">-Path</span></span>
<span data-ttu-id="2e079-140">Anger sökvägen till en mapp.</span><span class="sxs-lookup"><span data-stu-id="2e079-140">Specifies the path of a folder.</span></span>

<span data-ttu-id="2e079-141">Om du utelämnar parametern *Path* visas **katalogerna** och filerna i den angivna fil resursen eller katalogen.</span><span class="sxs-lookup"><span data-stu-id="2e079-141">If you omit the *Path* parameter, **Get-AzureStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="2e079-142">Om du inkluderar parametern *Path* returnerar **Get-AzureStorageFile** en instans av en katalog eller fil i den angivna sökvägen.</span><span class="sxs-lookup"><span data-stu-id="2e079-142">If you include the *Path* parameter, **Get-AzureStorageFile** returns an instance of a directory or file in the specified path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e079-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2e079-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2e079-144">Anger timeout-intervallet i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="2e079-144">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="2e079-145">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="2e079-145">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="2e079-146">-Dela</span><span class="sxs-lookup"><span data-stu-id="2e079-146">-Share</span></span>
<span data-ttu-id="2e079-147">Anger ett **CloudFileShare** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2e079-147">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="2e079-148">Denna cmdlet hämtar en fil eller katalog från fil resursen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="2e079-148">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="2e079-149">För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="2e079-149">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="2e079-150">Det här objektet innehåller lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="2e079-150">This object contains the Storage context.</span></span>
<span data-ttu-id="2e079-151">Om du anger den här parametern ska du inte ange en *kontext* parameter.</span><span class="sxs-lookup"><span data-stu-id="2e079-151">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e079-152">-ShareName</span><span class="sxs-lookup"><span data-stu-id="2e079-152">-ShareName</span></span>
<span data-ttu-id="2e079-153">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="2e079-153">Specifies the name of the file share.</span></span>
<span data-ttu-id="2e079-154">Denna cmdlet hämtar en fil eller katalog från fil resursen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="2e079-154">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e079-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e079-155">CommonParameters</span></span>
<span data-ttu-id="2e079-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e079-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e079-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e079-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e079-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2e079-158">INPUTS</span></span>

## <span data-ttu-id="2e079-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2e079-159">OUTPUTS</span></span>

## <span data-ttu-id="2e079-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2e079-160">NOTES</span></span>

## <span data-ttu-id="2e079-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2e079-161">RELATED LINKS</span></span>

[<span data-ttu-id="2e079-162">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2e079-162">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="2e079-163">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="2e079-163">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="2e079-164">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="2e079-164">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="2e079-165">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="2e079-165">Remove-AzureStorageFile</span></span>](./Remove-AzureStorageFile.md)

[<span data-ttu-id="2e079-166">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2e079-166">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


