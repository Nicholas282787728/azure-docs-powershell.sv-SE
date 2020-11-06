---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
ms.openlocfilehash: c929a7e3e685fd870c57ff942262a0c5ac4a9966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574458"
---
# <span data-ttu-id="72fd0-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="72fd0-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="72fd0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="72fd0-103">Tar bort en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="72fd0-103">Deletes a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72fd0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72fd0-104">SYNTAX</span></span>

### <span data-ttu-id="72fd0-105">Resurs namn (standard)</span><span class="sxs-lookup"><span data-stu-id="72fd0-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72fd0-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="72fd0-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72fd0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72fd0-107">DESCRIPTION</span></span>
<span data-ttu-id="72fd0-108">Cmdleten **Remove-AzureStorageShare** tar bort en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="72fd0-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="72fd0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72fd0-109">EXAMPLES</span></span>

### <span data-ttu-id="72fd0-110">Exempel 1: ta bort en fil resurs</span><span class="sxs-lookup"><span data-stu-id="72fd0-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="72fd0-111">Det här kommandot tar bort fil resursen som heter ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="72fd0-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="72fd0-112">Exempel 2: ta bort en fil resurs och alla dess stillbilder</span><span class="sxs-lookup"><span data-stu-id="72fd0-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="72fd0-113">Det här kommandot tar bort fil resursen med namnet ContosoShare06 och alla dess stillbilder.</span><span class="sxs-lookup"><span data-stu-id="72fd0-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="72fd0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72fd0-114">PARAMETERS</span></span>

### <span data-ttu-id="72fd0-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="72fd0-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="72fd0-116">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="72fd0-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="72fd0-117">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="72fd0-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="72fd0-118">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="72fd0-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="72fd0-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="72fd0-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="72fd0-120">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="72fd0-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="72fd0-121">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="72fd0-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="72fd0-122">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="72fd0-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="72fd0-123">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="72fd0-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="72fd0-124">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="72fd0-124">The default value is 10.</span></span>

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

### <span data-ttu-id="72fd0-125">-Kontext</span><span class="sxs-lookup"><span data-stu-id="72fd0-125">-Context</span></span>
<span data-ttu-id="72fd0-126">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="72fd0-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="72fd0-127">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="72fd0-127">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="72fd0-128">-Force</span><span class="sxs-lookup"><span data-stu-id="72fd0-128">-Force</span></span>
<span data-ttu-id="72fd0-129">Tvinga att ta bort resursen med alla dess stillbilder samt allt innehåll.</span><span class="sxs-lookup"><span data-stu-id="72fd0-129">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="72fd0-130">-IncludeAllSnapshot</span><span class="sxs-lookup"><span data-stu-id="72fd0-130">-IncludeAllSnapshot</span></span>
<span data-ttu-id="72fd0-131">Ta bort fil resursen med alla stillbilder</span><span class="sxs-lookup"><span data-stu-id="72fd0-131">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="72fd0-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="72fd0-132">-Name</span></span>
<span data-ttu-id="72fd0-133">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="72fd0-133">Specifies the name of the file share.</span></span>
<span data-ttu-id="72fd0-134">Denna cmdlet tar bort fil resursen som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="72fd0-134">This cmdlet deletes the file share that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72fd0-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72fd0-135">-PassThru</span></span>
<span data-ttu-id="72fd0-136">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="72fd0-136">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="72fd0-137">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="72fd0-137">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="72fd0-138">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="72fd0-138">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="72fd0-139">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="72fd0-139">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="72fd0-140">-Dela</span><span class="sxs-lookup"><span data-stu-id="72fd0-140">-Share</span></span>
<span data-ttu-id="72fd0-141">Anger ett **CloudFileShare** -objekt.</span><span class="sxs-lookup"><span data-stu-id="72fd0-141">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="72fd0-142">Denna cmdlet tar bort det objekt som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="72fd0-142">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="72fd0-143">För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="72fd0-143">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="72fd0-144">Det här objektet innehåller lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="72fd0-144">This object contains the storage context.</span></span>
<span data-ttu-id="72fd0-145">Om du anger den här parametern ska du inte ange en *kontext* parameter.</span><span class="sxs-lookup"><span data-stu-id="72fd0-145">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="72fd0-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="72fd0-146">-Confirm</span></span>
<span data-ttu-id="72fd0-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="72fd0-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72fd0-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72fd0-148">-WhatIf</span></span>
<span data-ttu-id="72fd0-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="72fd0-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72fd0-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="72fd0-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72fd0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72fd0-151">CommonParameters</span></span>
<span data-ttu-id="72fd0-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72fd0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72fd0-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72fd0-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72fd0-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72fd0-154">INPUTS</span></span>

### <span data-ttu-id="72fd0-155">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="72fd0-155">IStorageContext</span></span>

<span data-ttu-id="72fd0-156">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="72fd0-156">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="72fd0-157">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="72fd0-157">String</span></span>

<span data-ttu-id="72fd0-158">Parametern "name" accepterar värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="72fd0-158">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="72fd0-159">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="72fd0-159">CloudFileShare</span></span>

<span data-ttu-id="72fd0-160">Parametern ' Share ' godkänner värdet av typen ' CloudFileShare ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="72fd0-160">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="72fd0-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72fd0-161">OUTPUTS</span></span>

## <span data-ttu-id="72fd0-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72fd0-162">NOTES</span></span>

## <span data-ttu-id="72fd0-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72fd0-163">RELATED LINKS</span></span>

[<span data-ttu-id="72fd0-164">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="72fd0-164">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="72fd0-165">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="72fd0-165">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="72fd0-166">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="72fd0-166">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
