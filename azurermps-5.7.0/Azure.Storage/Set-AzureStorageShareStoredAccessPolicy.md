---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 0c77d2dedadd205a659bf296e02c09b98342dcc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758240"
---
# <span data-ttu-id="585b0-101">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="585b0-101">Set-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="585b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="585b0-102">SYNOPSIS</span></span>
<span data-ttu-id="585b0-103">Uppdaterar en lagrad åtkomst princip på en lagrings plats.</span><span class="sxs-lookup"><span data-stu-id="585b0-103">Updates a stored access policy on a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="585b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="585b0-104">SYNTAX</span></span>

```
Set-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="585b0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="585b0-105">DESCRIPTION</span></span>
<span data-ttu-id="585b0-106">Cmdleten **set-AzureStorageShareStoredAccessPolicy har** en lagrad åtkomst princip på en Azure lagrings plats.</span><span class="sxs-lookup"><span data-stu-id="585b0-106">The **Set-AzureStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="585b0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="585b0-107">EXAMPLES</span></span>

### <span data-ttu-id="585b0-108">Exempel 1: uppdatera en lagrad åtkomst princip i lagrings resursen</span><span class="sxs-lookup"><span data-stu-id="585b0-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="585b0-109">Det här kommandot uppdaterar en sparad åtkomst princip med fullständig behörighet i en resurs.</span><span class="sxs-lookup"><span data-stu-id="585b0-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="585b0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="585b0-110">PARAMETERS</span></span>

### <span data-ttu-id="585b0-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="585b0-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="585b0-112">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="585b0-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="585b0-113">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="585b0-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="585b0-114">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="585b0-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="585b0-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="585b0-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="585b0-116">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="585b0-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="585b0-117">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="585b0-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="585b0-118">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="585b0-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="585b0-119">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="585b0-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="585b0-120">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="585b0-120">The default value is 10.</span></span>

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

### <span data-ttu-id="585b0-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="585b0-121">-Context</span></span>
<span data-ttu-id="585b0-122">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="585b0-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="585b0-123">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="585b0-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="585b0-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="585b0-124">-ExpiryTime</span></span>
<span data-ttu-id="585b0-125">Anger den tid då den lagrade åtkomst policyn blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="585b0-125">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="585b0-126">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="585b0-126">-NoExpiryTime</span></span>
<span data-ttu-id="585b0-127">Anger att den här cmdleten rensar egenskapen **ExpiryTime** i den lagrade åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="585b0-127">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="585b0-128">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="585b0-128">-NoStartTime</span></span>
<span data-ttu-id="585b0-129">Anger att denna cmdlet rensar egenskapen **StartTime** i den lagrade åtkomst policyn.</span><span class="sxs-lookup"><span data-stu-id="585b0-129">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="585b0-130">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="585b0-130">-Permission</span></span>
<span data-ttu-id="585b0-131">Anger behörigheter i den lagrade åtkomst principen för att komma åt den delade resursen eller filerna under den.</span><span class="sxs-lookup"><span data-stu-id="585b0-131">Specifies permissions in the stored access policy to access the share or files under it.</span></span>

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

### <span data-ttu-id="585b0-132">-Princip</span><span class="sxs-lookup"><span data-stu-id="585b0-132">-Policy</span></span>
<span data-ttu-id="585b0-133">Anger ett namn för den lagrade åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="585b0-133">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="585b0-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="585b0-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="585b0-135">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="585b0-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="585b0-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="585b0-136">-ShareName</span></span>
<span data-ttu-id="585b0-137">Anger namnet på lagrings resursen.</span><span class="sxs-lookup"><span data-stu-id="585b0-137">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="585b0-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="585b0-138">-StartTime</span></span>
<span data-ttu-id="585b0-139">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="585b0-139">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="585b0-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="585b0-140">-Confirm</span></span>
<span data-ttu-id="585b0-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="585b0-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="585b0-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="585b0-142">-WhatIf</span></span>
<span data-ttu-id="585b0-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="585b0-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="585b0-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="585b0-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="585b0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="585b0-145">CommonParameters</span></span>
<span data-ttu-id="585b0-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="585b0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="585b0-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="585b0-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="585b0-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="585b0-148">INPUTS</span></span>

### <span data-ttu-id="585b0-149">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="585b0-149">IStorageContext</span></span>

<span data-ttu-id="585b0-150">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="585b0-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="585b0-151">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="585b0-151">String</span></span>

<span data-ttu-id="585b0-152">Parametern ' ShareName ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="585b0-152">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="585b0-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="585b0-153">OUTPUTS</span></span>

### <span data-ttu-id="585b0-154">System. String</span><span class="sxs-lookup"><span data-stu-id="585b0-154">System.String</span></span>

## <span data-ttu-id="585b0-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="585b0-155">NOTES</span></span>

## <span data-ttu-id="585b0-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="585b0-156">RELATED LINKS</span></span>

[<span data-ttu-id="585b0-157">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="585b0-157">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="585b0-158">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="585b0-158">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="585b0-159">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="585b0-159">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="585b0-160">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="585b0-160">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)
