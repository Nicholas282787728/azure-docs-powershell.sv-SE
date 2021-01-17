---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 577dd6cb3ca12daee1cbc4c87d5d1f619c13eea0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403307"
---
# <span data-ttu-id="831a9-101">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="831a9-101">Set-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="831a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="831a9-102">SYNOPSIS</span></span>
<span data-ttu-id="831a9-103">Anger en lagrad åtkomst princip för en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="831a9-103">Sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="831a9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="831a9-104">SYNTAX</span></span>

```
Set-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="831a9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="831a9-105">DESCRIPTION</span></span>
<span data-ttu-id="831a9-106">Cmdleten **set-AzStorageContainerStoredAccessPolicy** anger en lagrad åtkomst princip för en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="831a9-106">The **Set-AzStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="831a9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="831a9-107">EXAMPLES</span></span>

### <span data-ttu-id="831a9-108">Exempel 1: Ange en lagrad åtkomst princip i en lagrings behållare med fullständig behörighet</span><span class="sxs-lookup"><span data-stu-id="831a9-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="831a9-109">Det här kommandot anger en åtkomst princip med namnet Policy06 för Storage container med namnet $.</span><span class="sxs-lookup"><span data-stu-id="831a9-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="831a9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="831a9-110">PARAMETERS</span></span>

### <span data-ttu-id="831a9-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="831a9-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="831a9-112">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="831a9-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="831a9-113">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="831a9-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="831a9-114">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="831a9-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="831a9-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="831a9-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="831a9-116">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="831a9-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="831a9-117">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="831a9-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="831a9-118">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="831a9-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="831a9-119">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="831a9-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="831a9-120">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="831a9-120">The default value is 10.</span></span>

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

### <span data-ttu-id="831a9-121">-Container</span><span class="sxs-lookup"><span data-stu-id="831a9-121">-Container</span></span>
<span data-ttu-id="831a9-122">Anger namnet på Azure-lagringsplatsen.</span><span class="sxs-lookup"><span data-stu-id="831a9-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="831a9-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="831a9-123">-Context</span></span>
<span data-ttu-id="831a9-124">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="831a9-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="831a9-125">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="831a9-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="831a9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="831a9-126">-DefaultProfile</span></span>
<span data-ttu-id="831a9-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="831a9-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="831a9-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="831a9-128">-ExpiryTime</span></span>
<span data-ttu-id="831a9-129">Anger den tid då den lagrade åtkomst policyn blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="831a9-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831a9-130">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="831a9-130">-NoExpiryTime</span></span>
<span data-ttu-id="831a9-131">Visar att åtkomst policyn inte har något utgångs datum.</span><span class="sxs-lookup"><span data-stu-id="831a9-131">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831a9-132">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="831a9-132">-NoStartTime</span></span>
<span data-ttu-id="831a9-133">Anger start tiden som ska $Null.</span><span class="sxs-lookup"><span data-stu-id="831a9-133">Sets the start time to be $Null.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831a9-134">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="831a9-134">-Permission</span></span>
<span data-ttu-id="831a9-135">Anger behörigheter i den lagrade åtkomst principen för att komma åt lagrings behållaren.</span><span class="sxs-lookup"><span data-stu-id="831a9-135">Specifies permissions in the stored access policy to access the storage container.</span></span>
<span data-ttu-id="831a9-136">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="831a9-136">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831a9-137">-Princip</span><span class="sxs-lookup"><span data-stu-id="831a9-137">-Policy</span></span>
<span data-ttu-id="831a9-138">Anger namnet på den lagrade åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="831a9-138">Specifies the name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831a9-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="831a9-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="831a9-140">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="831a9-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="831a9-141">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="831a9-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="831a9-142">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="831a9-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="831a9-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="831a9-143">-StartTime</span></span>
<span data-ttu-id="831a9-144">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="831a9-144">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831a9-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="831a9-145">-Confirm</span></span>
<span data-ttu-id="831a9-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="831a9-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831a9-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="831a9-147">-WhatIf</span></span>
<span data-ttu-id="831a9-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="831a9-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="831a9-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="831a9-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831a9-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="831a9-150">CommonParameters</span></span>
<span data-ttu-id="831a9-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="831a9-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="831a9-152">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="831a9-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="831a9-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="831a9-153">INPUTS</span></span>

### <span data-ttu-id="831a9-154">System. String</span><span class="sxs-lookup"><span data-stu-id="831a9-154">System.String</span></span>

### <span data-ttu-id="831a9-155">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="831a9-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="831a9-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="831a9-156">OUTPUTS</span></span>

### <span data-ttu-id="831a9-157">System. String</span><span class="sxs-lookup"><span data-stu-id="831a9-157">System.String</span></span>

## <span data-ttu-id="831a9-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="831a9-158">NOTES</span></span>

## <span data-ttu-id="831a9-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="831a9-159">RELATED LINKS</span></span>

[<span data-ttu-id="831a9-160">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="831a9-160">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="831a9-161">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="831a9-161">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="831a9-162">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="831a9-162">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="831a9-163">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="831a9-163">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)
