---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1bdded3834806e33f4605f626b78fe06bc370bf6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572483"
---
# <span data-ttu-id="de416-101">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="de416-101">Set-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="de416-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de416-102">SYNOPSIS</span></span>
<span data-ttu-id="de416-103">Anger en lagrad åtkomst princip för en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="de416-103">Sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="de416-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de416-104">SYNTAX</span></span>

```
Set-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de416-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de416-105">DESCRIPTION</span></span>
<span data-ttu-id="de416-106">Cmdleten **set-AzureStorageContainerStoredAccessPolicy** anger en lagrad åtkomst princip för en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="de416-106">The **Set-AzureStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="de416-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de416-107">EXAMPLES</span></span>

### <span data-ttu-id="de416-108">Exempel 1: Ange en lagrad åtkomst princip i en lagrings behållare</span><span class="sxs-lookup"><span data-stu-id="de416-108">Example 1: Set a stored access policy in a storage container</span></span>
```
PS C:\>Set-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06"
```

<span data-ttu-id="de416-109">Det här kommandot anger en åtkomst princip med namnet Policy06 för Storage container med namnet $.</span><span class="sxs-lookup"><span data-stu-id="de416-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="de416-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de416-110">PARAMETERS</span></span>

### <span data-ttu-id="de416-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="de416-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="de416-112">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="de416-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="de416-113">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="de416-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="de416-114">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="de416-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="de416-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="de416-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="de416-116">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="de416-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="de416-117">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="de416-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="de416-118">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="de416-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="de416-119">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="de416-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="de416-120">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="de416-120">The default value is 10.</span></span>

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

### <span data-ttu-id="de416-121">-Container</span><span class="sxs-lookup"><span data-stu-id="de416-121">-Container</span></span>
<span data-ttu-id="de416-122">Anger namnet på Azure-lagringsplatsen.</span><span class="sxs-lookup"><span data-stu-id="de416-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="de416-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="de416-123">-Context</span></span>
<span data-ttu-id="de416-124">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="de416-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="de416-125">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="de416-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="de416-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="de416-126">-ExpiryTime</span></span>
<span data-ttu-id="de416-127">Anger den tid då den lagrade åtkomst policyn blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="de416-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="de416-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="de416-128">-NoExpiryTime</span></span>
<span data-ttu-id="de416-129">Visar att åtkomst policyn inte har något utgångs datum.</span><span class="sxs-lookup"><span data-stu-id="de416-129">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="de416-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="de416-130">-NoStartTime</span></span>
<span data-ttu-id="de416-131">Anger start tiden som ska $Null.</span><span class="sxs-lookup"><span data-stu-id="de416-131">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="de416-132">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="de416-132">-Permission</span></span>
<span data-ttu-id="de416-133">Anger nivån för offentlig åtkomst till den här behållaren.</span><span class="sxs-lookup"><span data-stu-id="de416-133">Specifies the level of public access to this container.</span></span>

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

### <span data-ttu-id="de416-134">-Princip</span><span class="sxs-lookup"><span data-stu-id="de416-134">-Policy</span></span>
<span data-ttu-id="de416-135">Anger en lagrad åtkomst princip som innehåller behörigheter för denna delade Access-signatur (SAS).</span><span class="sxs-lookup"><span data-stu-id="de416-135">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="de416-136">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="de416-136">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="de416-137">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="de416-137">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="de416-138">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="de416-138">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="de416-139">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="de416-139">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="de416-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="de416-140">-StartTime</span></span>
<span data-ttu-id="de416-141">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="de416-141">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="de416-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="de416-142">-Confirm</span></span>
<span data-ttu-id="de416-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="de416-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de416-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de416-144">-WhatIf</span></span>
<span data-ttu-id="de416-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="de416-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de416-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="de416-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de416-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de416-147">CommonParameters</span></span>
<span data-ttu-id="de416-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de416-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de416-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de416-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de416-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de416-150">INPUTS</span></span>

## <span data-ttu-id="de416-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de416-151">OUTPUTS</span></span>

## <span data-ttu-id="de416-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de416-152">NOTES</span></span>

## <span data-ttu-id="de416-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de416-153">RELATED LINKS</span></span>

[<span data-ttu-id="de416-154">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="de416-154">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="de416-155">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="de416-155">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="de416-156">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="de416-156">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="de416-157">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="de416-157">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)
