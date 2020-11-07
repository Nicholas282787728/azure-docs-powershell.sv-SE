---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 63fd207c9d3348e17718f6d4ad8dbd53a09752af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757520"
---
# <span data-ttu-id="d8ce5-101">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d8ce5-101">Set-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="d8ce5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8ce5-102">SYNOPSIS</span></span>
<span data-ttu-id="d8ce5-103">Anger en lagrad åtkomst princip för en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-103">Sets a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8ce5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8ce5-104">SYNTAX</span></span>

```
Set-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8ce5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8ce5-105">DESCRIPTION</span></span>
<span data-ttu-id="d8ce5-106">Cmdleten **set-AzureStorageContainerStoredAccessPolicy** anger en lagrad åtkomst princip för en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-106">The **Set-AzureStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="d8ce5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8ce5-107">EXAMPLES</span></span>

### <span data-ttu-id="d8ce5-108">Exempel 1: Ange en lagrad åtkomst princip i en lagrings behållare med fullständig behörighet</span><span class="sxs-lookup"><span data-stu-id="d8ce5-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="d8ce5-109">Det här kommandot anger en åtkomst princip med namnet Policy06 för Storage container med namnet $.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="d8ce5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8ce5-110">PARAMETERS</span></span>

### <span data-ttu-id="d8ce5-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d8ce5-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d8ce5-112">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d8ce5-113">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d8ce5-114">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d8ce5-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d8ce5-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d8ce5-116">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d8ce5-117">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d8ce5-118">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d8ce5-119">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d8ce5-120">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-120">The default value is 10.</span></span>

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

### <span data-ttu-id="d8ce5-121">-Container</span><span class="sxs-lookup"><span data-stu-id="d8ce5-121">-Container</span></span>
<span data-ttu-id="d8ce5-122">Anger namnet på Azure-lagringsplatsen.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8ce5-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d8ce5-123">-Context</span></span>
<span data-ttu-id="d8ce5-124">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d8ce5-125">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d8ce5-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d8ce5-126">-ExpiryTime</span></span>
<span data-ttu-id="d8ce5-127">Anger den tid då den lagrade åtkomst policyn blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ce5-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d8ce5-128">-NoExpiryTime</span></span>
<span data-ttu-id="d8ce5-129">Visar att åtkomst policyn inte har något utgångs datum.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-129">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="d8ce5-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="d8ce5-130">-NoStartTime</span></span>
<span data-ttu-id="d8ce5-131">Anger start tiden som ska $Null.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-131">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="d8ce5-132">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="d8ce5-132">-Permission</span></span>
<span data-ttu-id="d8ce5-133">Anger behörigheter i den lagrade åtkomst principen för att komma åt lagrings behållaren.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-133">Specifies permissions in the stored access policy to access the storage container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ce5-134">-Princip</span><span class="sxs-lookup"><span data-stu-id="d8ce5-134">-Policy</span></span>
<span data-ttu-id="d8ce5-135">Anger namnet på den lagrade åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-135">Specifies the name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ce5-136">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d8ce5-136">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d8ce5-137">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-137">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d8ce5-138">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-138">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d8ce5-139">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-139">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d8ce5-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d8ce5-140">-StartTime</span></span>
<span data-ttu-id="d8ce5-141">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-141">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ce5-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d8ce5-142">-Confirm</span></span>
<span data-ttu-id="d8ce5-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ce5-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8ce5-144">-WhatIf</span></span>
<span data-ttu-id="d8ce5-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8ce5-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ce5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8ce5-147">CommonParameters</span></span>
<span data-ttu-id="d8ce5-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8ce5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8ce5-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8ce5-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8ce5-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8ce5-150">INPUTS</span></span>

### <span data-ttu-id="d8ce5-151">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="d8ce5-151">String</span></span>

<span data-ttu-id="d8ce5-152">Parametern "container" accepterar värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="d8ce5-152">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="d8ce5-153">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d8ce5-153">IStorageContext</span></span>

<span data-ttu-id="d8ce5-154">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d8ce5-154">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="d8ce5-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8ce5-155">OUTPUTS</span></span>

### <span data-ttu-id="d8ce5-156">System. String</span><span class="sxs-lookup"><span data-stu-id="d8ce5-156">System.String</span></span>

## <span data-ttu-id="d8ce5-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8ce5-157">NOTES</span></span>

## <span data-ttu-id="d8ce5-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8ce5-158">RELATED LINKS</span></span>

[<span data-ttu-id="d8ce5-159">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d8ce5-159">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="d8ce5-160">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d8ce5-160">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="d8ce5-161">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d8ce5-161">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="d8ce5-162">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d8ce5-162">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)
