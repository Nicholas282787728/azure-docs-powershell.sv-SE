---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageDirectory.md
ms.openlocfilehash: bc83da1cd177585b76d68eb0b55cdd15120ff22e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577320"
---
# <span data-ttu-id="fa3e4-101">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="fa3e4-101">New-AzureStorageDirectory</span></span>

## <span data-ttu-id="fa3e4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fa3e4-102">SYNOPSIS</span></span>
<span data-ttu-id="fa3e4-103">Skapar en katalog.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-103">Creates a directory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa3e4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fa3e4-104">SYNTAX</span></span>

### <span data-ttu-id="fa3e4-105">Resurs namn (standard)</span><span class="sxs-lookup"><span data-stu-id="fa3e4-105">ShareName (Default)</span></span>
```
New-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="fa3e4-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="fa3e4-106">Share</span></span>
```
New-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="fa3e4-107">Katalogen</span><span class="sxs-lookup"><span data-stu-id="fa3e4-107">Directory</span></span>
```
New-AzureStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="fa3e4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fa3e4-108">DESCRIPTION</span></span>
<span data-ttu-id="fa3e4-109">Cmdleten **New-AzureStorageDirectory** skapar en katalog.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-109">The **New-AzureStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="fa3e4-110">Denna cmdlet returnerar ett **CloudFileDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="fa3e4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fa3e4-111">EXAMPLES</span></span>

### <span data-ttu-id="fa3e4-112">Exempel 1: skapa en mapp i en fil resurs</span><span class="sxs-lookup"><span data-stu-id="fa3e4-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="fa3e4-113">Det här kommandot skapar en mapp med namnet ContosoWorkingFolder i fil resursen som heter ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="fa3e4-114">Exempel 2: skapa en mapp i en fil resurs som anges i ett fildelnings objekt</span><span class="sxs-lookup"><span data-stu-id="fa3e4-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | New-AzureStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="fa3e4-115">Det här kommandot använder cmdleten **Get-AzureStorageShare** för att få fil resursen som heter ContosoShare06 och skickar den sedan till den aktuella cmdleten med operatören.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fa3e4-116">Den aktuella cmdleten skapar mappen som heter ContosoWorkingFolder i ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="fa3e4-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fa3e4-117">PARAMETERS</span></span>

### <span data-ttu-id="fa3e4-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fa3e4-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fa3e4-119">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fa3e4-120">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fa3e4-121">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fa3e4-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fa3e4-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fa3e4-123">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fa3e4-124">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fa3e4-125">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fa3e4-126">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fa3e4-127">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-127">The default value is 10.</span></span>

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

### <span data-ttu-id="fa3e4-128">-Kontext</span><span class="sxs-lookup"><span data-stu-id="fa3e4-128">-Context</span></span>
<span data-ttu-id="fa3e4-129">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fa3e4-130">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="fa3e4-131">-Katalog</span><span class="sxs-lookup"><span data-stu-id="fa3e4-131">-Directory</span></span>
<span data-ttu-id="fa3e4-132">Anger en mapp som ett **CloudFileDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-132">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="fa3e4-133">Denna cmdlet skapar mappen på den plats som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-133">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="fa3e4-134">Använd New-AzureStorageDirectory cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-134">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="fa3e4-135">Du kan också använda Get-AzureStorageFile cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-135">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="fa3e4-136">-Path</span><span class="sxs-lookup"><span data-stu-id="fa3e4-136">-Path</span></span>
<span data-ttu-id="fa3e4-137">Anger sökvägen till en mapp.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-137">Specifies the path of a folder.</span></span>
<span data-ttu-id="fa3e4-138">Denna cmdlet skapar en mapp för sökvägen som anges i denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-138">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa3e4-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fa3e4-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fa3e4-140">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-140">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="fa3e4-141">-Dela</span><span class="sxs-lookup"><span data-stu-id="fa3e4-141">-Share</span></span>
<span data-ttu-id="fa3e4-142">Anger ett **CloudFileShare** -objekt.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-142">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="fa3e4-143">Denna cmdlet skapar en mapp i fil resursen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-143">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="fa3e4-144">För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-144">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="fa3e4-145">Det här objektet innehåller lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-145">This object contains the storage context.</span></span>
<span data-ttu-id="fa3e4-146">Om du anger den här parametern ska du inte ange en *kontext* parameter.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-146">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="fa3e4-147">-ShareName</span><span class="sxs-lookup"><span data-stu-id="fa3e4-147">-ShareName</span></span>
<span data-ttu-id="fa3e4-148">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-148">Specifies the name of the file share.</span></span>
<span data-ttu-id="fa3e4-149">Denna cmdlet skapar en mapp i fil resursen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-149">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="fa3e4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa3e4-150">CommonParameters</span></span>
<span data-ttu-id="fa3e4-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa3e4-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa3e4-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa3e4-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fa3e4-153">INPUTS</span></span>

### <span data-ttu-id="fa3e4-154">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fa3e4-154">IStorageContext</span></span>

<span data-ttu-id="fa3e4-155">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="fa3e4-155">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="fa3e4-156">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="fa3e4-156">CloudFileDirectory</span></span>

<span data-ttu-id="fa3e4-157">Parametern ' Directory ' godkänner värdet av typen ' CloudFileDirectory ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="fa3e4-157">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="fa3e4-158">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="fa3e4-158">String</span></span>

<span data-ttu-id="fa3e4-159">Parametern ' path ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="fa3e4-159">Parameter 'Path' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="fa3e4-160">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="fa3e4-160">CloudFileShare</span></span>

<span data-ttu-id="fa3e4-161">Parametern ' Share ' godkänner värdet av typen ' CloudFileShare ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="fa3e4-161">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="fa3e4-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fa3e4-162">OUTPUTS</span></span>

## <span data-ttu-id="fa3e4-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fa3e4-163">NOTES</span></span>

## <span data-ttu-id="fa3e4-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fa3e4-164">RELATED LINKS</span></span>

[<span data-ttu-id="fa3e4-165">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="fa3e4-165">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="fa3e4-166">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="fa3e4-166">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="fa3e4-167">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="fa3e4-167">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="fa3e4-168">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="fa3e4-168">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="fa3e4-169">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="fa3e4-169">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)
