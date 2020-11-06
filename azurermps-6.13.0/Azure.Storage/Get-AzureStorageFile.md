---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFile.md
ms.openlocfilehash: 5f1834eb603c5023ee49722ee0d7772af40f821c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576371"
---
# <span data-ttu-id="398ab-101">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="398ab-101">Get-AzureStorageFile</span></span>

## <span data-ttu-id="398ab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="398ab-102">SYNOPSIS</span></span>
<span data-ttu-id="398ab-103">Visar en lista över kataloger och filer för en sökväg.</span><span class="sxs-lookup"><span data-stu-id="398ab-103">Lists directories and files for a path.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="398ab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="398ab-104">SYNTAX</span></span>

### <span data-ttu-id="398ab-105">Resurs namn (standard)</span><span class="sxs-lookup"><span data-stu-id="398ab-105">ShareName (Default)</span></span>
```
Get-AzureStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="398ab-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="398ab-106">Share</span></span>
```
Get-AzureStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="398ab-107">Katalogen</span><span class="sxs-lookup"><span data-stu-id="398ab-107">Directory</span></span>
```
Get-AzureStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="398ab-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="398ab-108">DESCRIPTION</span></span>
<span data-ttu-id="398ab-109">Cmdleten **Get-AzureStorageFile** innehåller en lista över kataloger och filer för den delning eller katalog som du anger.</span><span class="sxs-lookup"><span data-stu-id="398ab-109">The **Get-AzureStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="398ab-110">Ange parametern *Path* för att få en instans av en katalog eller fil på den angivna sökvägen.</span><span class="sxs-lookup"><span data-stu-id="398ab-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>
<span data-ttu-id="398ab-111">Denna cmdlet returnerar **AzureStorageFile** -och **AzureStorageDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="398ab-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="398ab-112">Du kan använda egenskapen **IsDirectory** för att skilja mellan mappar och filer.</span><span class="sxs-lookup"><span data-stu-id="398ab-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="398ab-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="398ab-113">EXAMPLES</span></span>

### <span data-ttu-id="398ab-114">Exempel 1: lista kataloger i en resurs</span><span class="sxs-lookup"><span data-stu-id="398ab-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

<span data-ttu-id="398ab-115">Det här kommandot listar bara katalogerna i avsnittet Dela ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="398ab-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="398ab-116">Den hämtar först både filer och kataloger, skickar dem till operatorn **WHERE** genom att använda pipeline-operatorn och ignorera sedan alla objekt vars typ inte är "CloudFileDirectory".</span><span class="sxs-lookup"><span data-stu-id="398ab-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "CloudFileDirectory".</span></span>

### <span data-ttu-id="398ab-117">Exempel 2: lista en fil katalog</span><span class="sxs-lookup"><span data-stu-id="398ab-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzureStorageFile
```

<span data-ttu-id="398ab-118">Det här kommandot listar filerna och mapparna i katalogen ContosoWorkingFolder under fliken Dela ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="398ab-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="398ab-119">Den först får katalog instansen och går sedan till cmdleten **Get-AzureStorageFile** för att lista katalogen.</span><span class="sxs-lookup"><span data-stu-id="398ab-119">It first gets the directory instance, and then pipelines it to the **Get-AzureStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="398ab-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="398ab-120">PARAMETERS</span></span>

### <span data-ttu-id="398ab-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="398ab-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="398ab-122">Anger tids gräns för klient sidan i sekunder för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="398ab-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="398ab-123">Om det föregående samtalet inte fungerar inom det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="398ab-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="398ab-124">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="398ab-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="398ab-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="398ab-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="398ab-126">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="398ab-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="398ab-127">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="398ab-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="398ab-128">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="398ab-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="398ab-129">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="398ab-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="398ab-130">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="398ab-130">The default value is 10.</span></span>

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

### <span data-ttu-id="398ab-131">-Kontext</span><span class="sxs-lookup"><span data-stu-id="398ab-131">-Context</span></span>
<span data-ttu-id="398ab-132">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="398ab-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="398ab-133">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="398ab-133">To obtain a Storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="398ab-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="398ab-134">-DefaultProfile</span></span>
<span data-ttu-id="398ab-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="398ab-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="398ab-136">-Katalog</span><span class="sxs-lookup"><span data-stu-id="398ab-136">-Directory</span></span>
<span data-ttu-id="398ab-137">Anger en mapp som ett **CloudFileDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="398ab-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="398ab-138">Denna cmdlet tar fram den mapp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="398ab-138">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="398ab-139">Använd New-AzureStorageDirectory cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="398ab-139">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="398ab-140">Du kan också använda cmdleten **Get-AzureStorageFile** för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="398ab-140">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="398ab-141">-Path</span><span class="sxs-lookup"><span data-stu-id="398ab-141">-Path</span></span>
<span data-ttu-id="398ab-142">Anger sökvägen till en mapp.</span><span class="sxs-lookup"><span data-stu-id="398ab-142">Specifies the path of a folder.</span></span>
<span data-ttu-id="398ab-143">Om du utelämnar parametern *Path* visas **katalogerna** och filerna i den angivna fil resursen eller katalogen.</span><span class="sxs-lookup"><span data-stu-id="398ab-143">If you omit the *Path* parameter, **Get-AzureStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="398ab-144">Om du inkluderar parametern *Path* returnerar **Get-AzureStorageFile** en instans av en katalog eller fil i den angivna sökvägen.</span><span class="sxs-lookup"><span data-stu-id="398ab-144">If you include the *Path* parameter, **Get-AzureStorageFile** returns an instance of a directory or file in the specified path.</span></span>

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

### <span data-ttu-id="398ab-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="398ab-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="398ab-146">Anger timeout-intervallet i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="398ab-146">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="398ab-147">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="398ab-147">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="398ab-148">-Dela</span><span class="sxs-lookup"><span data-stu-id="398ab-148">-Share</span></span>
<span data-ttu-id="398ab-149">Anger ett **CloudFileShare** -objekt.</span><span class="sxs-lookup"><span data-stu-id="398ab-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="398ab-150">Denna cmdlet hämtar en fil eller katalog från fil resursen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="398ab-150">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="398ab-151">För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="398ab-151">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="398ab-152">Det här objektet innehåller lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="398ab-152">This object contains the Storage context.</span></span>
<span data-ttu-id="398ab-153">Om du anger den här parametern ska du inte ange en *kontext* parameter.</span><span class="sxs-lookup"><span data-stu-id="398ab-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="398ab-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="398ab-154">-ShareName</span></span>
<span data-ttu-id="398ab-155">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="398ab-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="398ab-156">Denna cmdlet hämtar en fil eller katalog från fil resursen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="398ab-156">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="398ab-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="398ab-157">CommonParameters</span></span>
<span data-ttu-id="398ab-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="398ab-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="398ab-159">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="398ab-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="398ab-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="398ab-160">INPUTS</span></span>

### <span data-ttu-id="398ab-161">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="398ab-161">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="398ab-162">Parametrar: dela (ByValue)</span><span class="sxs-lookup"><span data-stu-id="398ab-162">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="398ab-163">Microsoft. WindowsAzure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="398ab-163">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="398ab-164">Parametrar: katalog (ByValue)</span><span class="sxs-lookup"><span data-stu-id="398ab-164">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="398ab-165">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="398ab-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="398ab-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="398ab-166">OUTPUTS</span></span>

### <span data-ttu-id="398ab-167">Microsoft. WindowsAzure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="398ab-167">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="398ab-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="398ab-168">NOTES</span></span>

## <span data-ttu-id="398ab-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="398ab-169">RELATED LINKS</span></span>

[<span data-ttu-id="398ab-170">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="398ab-170">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="398ab-171">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="398ab-171">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="398ab-172">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="398ab-172">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="398ab-173">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="398ab-173">Remove-AzureStorageFile</span></span>](./Remove-AzureStorageFile.md)

[<span data-ttu-id="398ab-174">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="398ab-174">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


