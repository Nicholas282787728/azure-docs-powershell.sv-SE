---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: cdd52b1e1bab28956605d70e1089d7804b8ccff7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756118"
---
# <span data-ttu-id="34932-101">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="34932-101">Remove-AzureStorageDirectory</span></span>

## <span data-ttu-id="34932-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="34932-102">SYNOPSIS</span></span>
<span data-ttu-id="34932-103">Tar bort en katalog.</span><span class="sxs-lookup"><span data-stu-id="34932-103">Deletes a directory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34932-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="34932-104">SYNTAX</span></span>

### <span data-ttu-id="34932-105">Resurs namn (standard)</span><span class="sxs-lookup"><span data-stu-id="34932-105">ShareName (Default)</span></span>
```
Remove-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34932-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="34932-106">Share</span></span>
```
Remove-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34932-107">Katalogen</span><span class="sxs-lookup"><span data-stu-id="34932-107">Directory</span></span>
```
Remove-AzureStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34932-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="34932-108">DESCRIPTION</span></span>
<span data-ttu-id="34932-109">Cmdleten **Remove-AzureStorageDirectory** tar bort en katalog.</span><span class="sxs-lookup"><span data-stu-id="34932-109">The **Remove-AzureStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="34932-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="34932-110">EXAMPLES</span></span>

### <span data-ttu-id="34932-111">Exempel 1: ta bort en mapp</span><span class="sxs-lookup"><span data-stu-id="34932-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="34932-112">Det här kommandot tar bort mappen som heter ContosoWorkingFolder från fil resursen med namnet ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="34932-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="34932-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="34932-113">PARAMETERS</span></span>

### <span data-ttu-id="34932-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="34932-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="34932-115">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="34932-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="34932-116">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="34932-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="34932-117">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="34932-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="34932-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="34932-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="34932-119">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="34932-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="34932-120">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="34932-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="34932-121">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="34932-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="34932-122">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="34932-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="34932-123">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="34932-123">The default value is 10.</span></span>

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

### <span data-ttu-id="34932-124">-Kontext</span><span class="sxs-lookup"><span data-stu-id="34932-124">-Context</span></span>
<span data-ttu-id="34932-125">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="34932-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="34932-126">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="34932-126">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="34932-127">-Katalog</span><span class="sxs-lookup"><span data-stu-id="34932-127">-Directory</span></span>
<span data-ttu-id="34932-128">Anger en mapp som ett **CloudFileDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="34932-128">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="34932-129">Denna cmdlet tar bort den mapp som anges i den här parametern.</span><span class="sxs-lookup"><span data-stu-id="34932-129">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="34932-130">Använd New-AzureStorageDirectory cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="34932-130">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="34932-131">Du kan också använda cmdleten **Get-AzureStorageFile** för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="34932-131">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="34932-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34932-132">-PassThru</span></span>
<span data-ttu-id="34932-133">Anger att om denna cmdlet lyckas returneras ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="34932-133">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="34932-134">Om du anger den här parametern och om cmdleten Miss lyckas på grund av ett olämpligt värde för parametern _Path_ returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="34932-134">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="34932-135">Om du inte anger den här parametern returnerar denna cmdlet inte ett värde.</span><span class="sxs-lookup"><span data-stu-id="34932-135">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="34932-136">-Path</span><span class="sxs-lookup"><span data-stu-id="34932-136">-Path</span></span>
<span data-ttu-id="34932-137">Anger sökvägen till en mapp.</span><span class="sxs-lookup"><span data-stu-id="34932-137">Specifies the path of a folder.</span></span>
<span data-ttu-id="34932-138">Om mappen som den här parametern anger är tom tar denna cmdlet bort den mappen.</span><span class="sxs-lookup"><span data-stu-id="34932-138">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="34932-139">Om mappen inte är tom gör denna cmdlet ingen ändring och returnerar ett fel.</span><span class="sxs-lookup"><span data-stu-id="34932-139">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Directory
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34932-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="34932-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="34932-141">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="34932-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="34932-142">-Dela</span><span class="sxs-lookup"><span data-stu-id="34932-142">-Share</span></span>
<span data-ttu-id="34932-143">Anger ett **CloudFileShare** -objekt.</span><span class="sxs-lookup"><span data-stu-id="34932-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="34932-144">Denna cmdlet tar bort en mapp under fil resursen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="34932-144">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="34932-145">För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="34932-145">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="34932-146">Det här objektet innehåller lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="34932-146">This object contains the storage context.</span></span>
<span data-ttu-id="34932-147">Om du anger den här parametern ska du inte ange en *kontext* parameter.</span><span class="sxs-lookup"><span data-stu-id="34932-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="34932-148">-ShareName</span><span class="sxs-lookup"><span data-stu-id="34932-148">-ShareName</span></span>
<span data-ttu-id="34932-149">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="34932-149">Specifies the name of the file share.</span></span>
<span data-ttu-id="34932-150">Denna cmdlet tar bort en mapp under fil resursen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="34932-150">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="34932-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="34932-151">-Confirm</span></span>
<span data-ttu-id="34932-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="34932-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34932-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34932-153">-WhatIf</span></span>
<span data-ttu-id="34932-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="34932-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34932-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="34932-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34932-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34932-156">CommonParameters</span></span>
<span data-ttu-id="34932-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34932-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34932-158">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34932-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34932-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="34932-159">INPUTS</span></span>

### <span data-ttu-id="34932-160">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="34932-160">IStorageContext</span></span>

<span data-ttu-id="34932-161">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="34932-161">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="34932-162">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="34932-162">CloudFileDirectory</span></span>

<span data-ttu-id="34932-163">Parametern ' Directory ' godkänner värdet av typen ' CloudFileDirectory ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="34932-163">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="34932-164">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="34932-164">CloudFileShare</span></span>

<span data-ttu-id="34932-165">Parametern ' Share ' godkänner värdet av typen ' CloudFileShare ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="34932-165">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="34932-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="34932-166">OUTPUTS</span></span>

## <span data-ttu-id="34932-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="34932-167">NOTES</span></span>

## <span data-ttu-id="34932-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="34932-168">RELATED LINKS</span></span>

[<span data-ttu-id="34932-169">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="34932-169">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="34932-170">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="34932-170">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="34932-171">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="34932-171">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)
