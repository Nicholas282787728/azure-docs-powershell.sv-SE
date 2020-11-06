---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07ca74b29dad61c1cf909f13aefbf35b2048d4aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571896"
---
# <span data-ttu-id="e2dc9-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="e2dc9-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="e2dc9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2dc9-102">SYNOPSIS</span></span>
<span data-ttu-id="e2dc9-103">Tar bort en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-103">Deletes a file share.</span></span>

## <span data-ttu-id="e2dc9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2dc9-104">SYNTAX</span></span>

### <span data-ttu-id="e2dc9-105">Resurs namn (standard)</span><span class="sxs-lookup"><span data-stu-id="e2dc9-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2dc9-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="e2dc9-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-Force] [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2dc9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2dc9-107">DESCRIPTION</span></span>
<span data-ttu-id="e2dc9-108">Cmdleten **Remove-AzureStorageShare** tar bort en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="e2dc9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2dc9-109">EXAMPLES</span></span>

### <span data-ttu-id="e2dc9-110">Exempel 1: ta bort en fil resurs</span><span class="sxs-lookup"><span data-stu-id="e2dc9-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="e2dc9-111">Det här kommandot tar bort fil resursen som heter ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-111">This command removes the file share named ContosoShare06.</span></span>

## <span data-ttu-id="e2dc9-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2dc9-112">PARAMETERS</span></span>

### <span data-ttu-id="e2dc9-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e2dc9-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e2dc9-114">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e2dc9-115">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e2dc9-116">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e2dc9-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e2dc9-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e2dc9-118">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e2dc9-119">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e2dc9-120">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e2dc9-121">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e2dc9-122">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-122">The default value is 10.</span></span>

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

### <span data-ttu-id="e2dc9-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="e2dc9-123">-Context</span></span>
<span data-ttu-id="e2dc9-124">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e2dc9-125">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="e2dc9-126">-Force</span><span class="sxs-lookup"><span data-stu-id="e2dc9-126">-Force</span></span>
<span data-ttu-id="e2dc9-127">Tvinga att ta bort delningen och allt innehåll i den</span><span class="sxs-lookup"><span data-stu-id="e2dc9-127">Force to remove the share and all content in it</span></span>

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

### <span data-ttu-id="e2dc9-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="e2dc9-128">-Name</span></span>
<span data-ttu-id="e2dc9-129">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-129">Specifies the name of the file share.</span></span>
<span data-ttu-id="e2dc9-130">Denna cmdlet tar bort fil resursen som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-130">This cmdlet deletes the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="e2dc9-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2dc9-131">-PassThru</span></span>
<span data-ttu-id="e2dc9-132">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-132">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="e2dc9-133">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-133">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="e2dc9-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e2dc9-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e2dc9-135">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="e2dc9-136">-Dela</span><span class="sxs-lookup"><span data-stu-id="e2dc9-136">-Share</span></span>
<span data-ttu-id="e2dc9-137">Anger ett **CloudFileShare** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-137">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="e2dc9-138">Denna cmdlet tar bort det objekt som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-138">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="e2dc9-139">För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-139">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="e2dc9-140">Det här objektet innehåller lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-140">This object contains the storage context.</span></span>
<span data-ttu-id="e2dc9-141">Om du anger den här parametern ska du inte ange en *kontext* parameter.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-141">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="e2dc9-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e2dc9-142">-Confirm</span></span>
<span data-ttu-id="e2dc9-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2dc9-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2dc9-144">-WhatIf</span></span>
<span data-ttu-id="e2dc9-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2dc9-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2dc9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2dc9-147">CommonParameters</span></span>
<span data-ttu-id="e2dc9-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2dc9-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2dc9-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2dc9-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2dc9-150">INPUTS</span></span>

## <span data-ttu-id="e2dc9-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2dc9-151">OUTPUTS</span></span>

## <span data-ttu-id="e2dc9-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2dc9-152">NOTES</span></span>

## <span data-ttu-id="e2dc9-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2dc9-153">RELATED LINKS</span></span>

[<span data-ttu-id="e2dc9-154">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="e2dc9-154">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="e2dc9-155">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e2dc9-155">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e2dc9-156">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="e2dc9-156">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
