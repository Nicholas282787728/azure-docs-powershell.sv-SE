---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1bd97057cfafc48b3f1edd8539e7808056599117
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572027"
---
# <span data-ttu-id="810fa-101">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="810fa-101">New-AzureStorageDirectory</span></span>

## <span data-ttu-id="810fa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="810fa-102">SYNOPSIS</span></span>
<span data-ttu-id="810fa-103">Skapar en katalog.</span><span class="sxs-lookup"><span data-stu-id="810fa-103">Creates a directory.</span></span>

## <span data-ttu-id="810fa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="810fa-104">SYNTAX</span></span>

### <span data-ttu-id="810fa-105">Resurs namn (standard)</span><span class="sxs-lookup"><span data-stu-id="810fa-105">ShareName (Default)</span></span>
```
New-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="810fa-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="810fa-106">Share</span></span>
```
New-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="810fa-107">Katalogen</span><span class="sxs-lookup"><span data-stu-id="810fa-107">Directory</span></span>
```
New-AzureStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="810fa-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="810fa-108">DESCRIPTION</span></span>
<span data-ttu-id="810fa-109">Cmdleten **New-AzureStorageDirectory** skapar en katalog.</span><span class="sxs-lookup"><span data-stu-id="810fa-109">The **New-AzureStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="810fa-110">Denna cmdlet returnerar ett **CloudFileDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="810fa-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="810fa-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="810fa-111">EXAMPLES</span></span>

### <span data-ttu-id="810fa-112">Exempel 1: skapa en mapp i en fil resurs</span><span class="sxs-lookup"><span data-stu-id="810fa-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="810fa-113">Det här kommandot skapar en mapp med namnet ContosoWorkingFolder i fil resursen som heter ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="810fa-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="810fa-114">Exempel 2: skapa en mapp i en fil resurs som anges i ett fildelnings objekt</span><span class="sxs-lookup"><span data-stu-id="810fa-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | New-AzureStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="810fa-115">Det här kommandot använder cmdleten **Get-AzureStorageShare** för att få fil resursen som heter ContosoShare06 och skickar den sedan till den aktuella cmdleten med operatören.</span><span class="sxs-lookup"><span data-stu-id="810fa-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="810fa-116">Den aktuella cmdleten skapar mappen som heter ContosoWorkingFolder i ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="810fa-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="810fa-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="810fa-117">PARAMETERS</span></span>

### <span data-ttu-id="810fa-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="810fa-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="810fa-119">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="810fa-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="810fa-120">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="810fa-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="810fa-121">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="810fa-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="810fa-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="810fa-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="810fa-123">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="810fa-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="810fa-124">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="810fa-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="810fa-125">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="810fa-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="810fa-126">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="810fa-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="810fa-127">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="810fa-127">The default value is 10.</span></span>

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

### <span data-ttu-id="810fa-128">-Kontext</span><span class="sxs-lookup"><span data-stu-id="810fa-128">-Context</span></span>
<span data-ttu-id="810fa-129">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="810fa-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="810fa-130">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="810fa-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="810fa-131">-Katalog</span><span class="sxs-lookup"><span data-stu-id="810fa-131">-Directory</span></span>
<span data-ttu-id="810fa-132">Anger en mapp som ett **CloudFileDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="810fa-132">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="810fa-133">Denna cmdlet skapar mappen på den plats som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="810fa-133">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="810fa-134">Använd New-AzureStorageDirectory cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="810fa-134">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="810fa-135">Du kan också använda Get-AzureStorageFile cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="810fa-135">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="810fa-136">-Path</span><span class="sxs-lookup"><span data-stu-id="810fa-136">-Path</span></span>
<span data-ttu-id="810fa-137">Anger sökvägen till en mapp.</span><span class="sxs-lookup"><span data-stu-id="810fa-137">Specifies the path of a folder.</span></span>
<span data-ttu-id="810fa-138">Denna cmdlet skapar en mapp för sökvägen som anges i denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="810fa-138">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="810fa-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="810fa-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="810fa-140">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="810fa-140">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="810fa-141">-Dela</span><span class="sxs-lookup"><span data-stu-id="810fa-141">-Share</span></span>
<span data-ttu-id="810fa-142">Anger ett **CloudFileShare** -objekt.</span><span class="sxs-lookup"><span data-stu-id="810fa-142">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="810fa-143">Denna cmdlet skapar en mapp i fil resursen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="810fa-143">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="810fa-144">För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="810fa-144">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="810fa-145">Det här objektet innehåller lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="810fa-145">This object contains the storage context.</span></span>
<span data-ttu-id="810fa-146">Om du anger den här parametern ska du inte ange en *kontext* parameter.</span><span class="sxs-lookup"><span data-stu-id="810fa-146">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="810fa-147">-ShareName</span><span class="sxs-lookup"><span data-stu-id="810fa-147">-ShareName</span></span>
<span data-ttu-id="810fa-148">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="810fa-148">Specifies the name of the file share.</span></span>
<span data-ttu-id="810fa-149">Denna cmdlet skapar en mapp i fil resursen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="810fa-149">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="810fa-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="810fa-150">CommonParameters</span></span>
<span data-ttu-id="810fa-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="810fa-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="810fa-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="810fa-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="810fa-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="810fa-153">INPUTS</span></span>

## <span data-ttu-id="810fa-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="810fa-154">OUTPUTS</span></span>

## <span data-ttu-id="810fa-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="810fa-155">NOTES</span></span>

## <span data-ttu-id="810fa-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="810fa-156">RELATED LINKS</span></span>

[<span data-ttu-id="810fa-157">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="810fa-157">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="810fa-158">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="810fa-158">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="810fa-159">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="810fa-159">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="810fa-160">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="810fa-160">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="810fa-161">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="810fa-161">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)
