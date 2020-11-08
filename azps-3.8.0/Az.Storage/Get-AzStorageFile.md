---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: aadbbbaaefe1090b221e049d310bf262fdddf28c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088958"
---
# <span data-ttu-id="e2e3b-101">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="e2e3b-101">Get-AzStorageFile</span></span>

## <span data-ttu-id="e2e3b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2e3b-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e3b-103">Visar en lista över kataloger och filer för en sökväg.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="e2e3b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2e3b-104">SYNTAX</span></span>

### <span data-ttu-id="e2e3b-105">Resurs namn (standard)</span><span class="sxs-lookup"><span data-stu-id="e2e3b-105">ShareName (Default)</span></span>
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e2e3b-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="e2e3b-106">Share</span></span>
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2e3b-107">Katalogen</span><span class="sxs-lookup"><span data-stu-id="e2e3b-107">Directory</span></span>
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2e3b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2e3b-108">DESCRIPTION</span></span>
<span data-ttu-id="e2e3b-109">Cmdleten **Get-AzStorageFile** innehåller en lista över kataloger och filer för den delning eller katalog som du anger.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-109">The **Get-AzStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="e2e3b-110">Ange parametern *Path* för att få en instans av en katalog eller fil på den angivna sökvägen.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>
<span data-ttu-id="e2e3b-111">Denna cmdlet returnerar **AzureStorageFile** -och **AzureStorageDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="e2e3b-112">Du kan använda egenskapen **IsDirectory** för att skilja mellan mappar och filer.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="e2e3b-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2e3b-113">EXAMPLES</span></span>

### <span data-ttu-id="e2e3b-114">Exempel 1: lista kataloger i en resurs</span><span class="sxs-lookup"><span data-stu-id="e2e3b-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

<span data-ttu-id="e2e3b-115">Det här kommandot listar bara katalogerna i avsnittet Dela ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="e2e3b-116">Den hämtar först både filer och kataloger, skickar dem till operatorn **WHERE** genom att använda pipeline-operatorn och ignorera sedan alla objekt vars typ inte är "CloudFileDirectory".</span><span class="sxs-lookup"><span data-stu-id="e2e3b-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "CloudFileDirectory".</span></span>

### <span data-ttu-id="e2e3b-117">Exempel 2: lista en fil katalog</span><span class="sxs-lookup"><span data-stu-id="e2e3b-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

<span data-ttu-id="e2e3b-118">Det här kommandot listar filerna och mapparna i katalogen ContosoWorkingFolder under fliken Dela ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="e2e3b-119">Den först får katalog instansen och går sedan till cmdleten **Get-AzStorageFile** för att lista katalogen.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-119">It first gets the directory instance, and then pipelines it to the **Get-AzStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="e2e3b-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2e3b-120">PARAMETERS</span></span>

### <span data-ttu-id="e2e3b-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e2e3b-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e2e3b-122">Anger tids gräns för klient sidan i sekunder för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e2e3b-123">Om det föregående samtalet inte fungerar inom det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e2e3b-124">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e2e3b-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e2e3b-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e2e3b-126">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e2e3b-127">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e2e3b-128">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e2e3b-129">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e2e3b-130">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-130">The default value is 10.</span></span>

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

### <span data-ttu-id="e2e3b-131">-Kontext</span><span class="sxs-lookup"><span data-stu-id="e2e3b-131">-Context</span></span>
<span data-ttu-id="e2e3b-132">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="e2e3b-133">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-133">To obtain a Storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e3b-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e3b-134">-DefaultProfile</span></span>
<span data-ttu-id="e2e3b-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2e3b-136">-Katalog</span><span class="sxs-lookup"><span data-stu-id="e2e3b-136">-Directory</span></span>
<span data-ttu-id="e2e3b-137">Anger en mapp som ett **CloudFileDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="e2e3b-138">Denna cmdlet tar fram den mapp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-138">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="e2e3b-139">Använd New-AzStorageDirectory cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-139">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="e2e3b-140">Du kan också använda cmdleten **Get-AzStorageFile** för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-140">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e3b-141">-Path</span><span class="sxs-lookup"><span data-stu-id="e2e3b-141">-Path</span></span>
<span data-ttu-id="e2e3b-142">Anger sökvägen till en mapp.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-142">Specifies the path of a folder.</span></span>
<span data-ttu-id="e2e3b-143">Om du utelämnar parametern *Path* visas **katalogerna** och filerna i den angivna fil resursen eller katalogen.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-143">If you omit the *Path* parameter, **Get-AzStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="e2e3b-144">Om du inkluderar parametern *Path* returnerar **Get-AzStorageFile** en instans av en katalog eller fil i den angivna sökvägen.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-144">If you include the *Path* parameter, **Get-AzStorageFile** returns an instance of a directory or file in the specified path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e3b-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e2e3b-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e2e3b-146">Anger timeout-intervallet i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-146">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="e2e3b-147">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-147">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="e2e3b-148">-Dela</span><span class="sxs-lookup"><span data-stu-id="e2e3b-148">-Share</span></span>
<span data-ttu-id="e2e3b-149">Anger ett **CloudFileShare** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="e2e3b-150">Denna cmdlet hämtar en fil eller katalog från fil resursen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-150">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="e2e3b-151">För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="e2e3b-152">Det här objektet innehåller lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-152">This object contains the Storage context.</span></span>
<span data-ttu-id="e2e3b-153">Om du anger den här parametern ska du inte ange en *kontext* parameter.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e3b-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="e2e3b-154">-ShareName</span></span>
<span data-ttu-id="e2e3b-155">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="e2e3b-156">Denna cmdlet hämtar en fil eller katalog från fil resursen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-156">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e3b-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e3b-157">CommonParameters</span></span>
<span data-ttu-id="e2e3b-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e3b-159">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2e3b-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e3b-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2e3b-160">INPUTS</span></span>

### <span data-ttu-id="e2e3b-161">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="e2e3b-161">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="e2e3b-162">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="e2e3b-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="e2e3b-163">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e2e3b-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e2e3b-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2e3b-164">OUTPUTS</span></span>

### <span data-ttu-id="e2e3b-165">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="e2e3b-165">Microsoft.Azure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="e2e3b-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2e3b-166">NOTES</span></span>

## <span data-ttu-id="e2e3b-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2e3b-167">RELATED LINKS</span></span>

[<span data-ttu-id="e2e3b-168">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e2e3b-168">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="e2e3b-169">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="e2e3b-169">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="e2e3b-170">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="e2e3b-170">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="e2e3b-171">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="e2e3b-171">Remove-AzStorageFile</span></span>](./Remove-AzStorageFile.md)

[<span data-ttu-id="e2e3b-172">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e2e3b-172">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


