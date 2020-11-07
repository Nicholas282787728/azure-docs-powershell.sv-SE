---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 58fc0ef20300f57407d7df35f1732830dbc4c5d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746253"
---
# <span data-ttu-id="7f1ae-101">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7f1ae-101">Set-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="7f1ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f1ae-102">SYNOPSIS</span></span>
<span data-ttu-id="7f1ae-103">Uppdaterar en lagrad åtkomst princip på en lagrings plats.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-103">Updates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="7f1ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f1ae-104">SYNTAX</span></span>

```
Set-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f1ae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f1ae-105">DESCRIPTION</span></span>
<span data-ttu-id="7f1ae-106">Cmdleten **set-AzStorageShareStoredAccessPolicy har** en lagrad åtkomst princip på en Azure lagrings plats.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-106">The **Set-AzStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="7f1ae-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f1ae-107">EXAMPLES</span></span>

### <span data-ttu-id="7f1ae-108">Exempel 1: uppdatera en lagrad åtkomst princip i lagrings resursen</span><span class="sxs-lookup"><span data-stu-id="7f1ae-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="7f1ae-109">Det här kommandot uppdaterar en sparad åtkomst princip med fullständig behörighet i en resurs.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="7f1ae-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f1ae-110">PARAMETERS</span></span>

### <span data-ttu-id="7f1ae-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7f1ae-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7f1ae-112">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7f1ae-113">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7f1ae-114">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7f1ae-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7f1ae-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7f1ae-116">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7f1ae-117">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7f1ae-118">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7f1ae-119">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7f1ae-120">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-120">The default value is 10.</span></span>

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

### <span data-ttu-id="7f1ae-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="7f1ae-121">-Context</span></span>
<span data-ttu-id="7f1ae-122">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7f1ae-123">Använd cmdleten [New-AzStorageContext](./New-AzStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="7f1ae-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f1ae-124">-DefaultProfile</span></span>
<span data-ttu-id="7f1ae-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f1ae-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7f1ae-126">-ExpiryTime</span></span>
<span data-ttu-id="7f1ae-127">Anger den tid då den lagrade åtkomst policyn blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="7f1ae-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7f1ae-128">-NoExpiryTime</span></span>
<span data-ttu-id="7f1ae-129">Anger att den här cmdleten rensar egenskapen **ExpiryTime** i den lagrade åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-129">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="7f1ae-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="7f1ae-130">-NoStartTime</span></span>
<span data-ttu-id="7f1ae-131">Anger att denna cmdlet rensar egenskapen **StartTime** i den lagrade åtkomst policyn.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-131">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="7f1ae-132">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="7f1ae-132">-Permission</span></span>
<span data-ttu-id="7f1ae-133">Anger behörigheter i den lagrade åtkomst principen för att komma åt den delade resursen eller filerna under den.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-133">Specifies permissions in the stored access policy to access the share or files under it.</span></span>
<span data-ttu-id="7f1ae-134">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="7f1ae-134">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="7f1ae-135">-Princip</span><span class="sxs-lookup"><span data-stu-id="7f1ae-135">-Policy</span></span>
<span data-ttu-id="7f1ae-136">Anger ett namn för den lagrade åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-136">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="7f1ae-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7f1ae-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7f1ae-138">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="7f1ae-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="7f1ae-139">-ShareName</span></span>
<span data-ttu-id="7f1ae-140">Anger namnet på lagrings resursen.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-140">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="7f1ae-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7f1ae-141">-StartTime</span></span>
<span data-ttu-id="7f1ae-142">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-142">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="7f1ae-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7f1ae-143">-Confirm</span></span>
<span data-ttu-id="7f1ae-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f1ae-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f1ae-145">-WhatIf</span></span>
<span data-ttu-id="7f1ae-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f1ae-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f1ae-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f1ae-148">CommonParameters</span></span>
<span data-ttu-id="7f1ae-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f1ae-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f1ae-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f1ae-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f1ae-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f1ae-151">INPUTS</span></span>

### <span data-ttu-id="7f1ae-152">System. String</span><span class="sxs-lookup"><span data-stu-id="7f1ae-152">System.String</span></span>

### <span data-ttu-id="7f1ae-153">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7f1ae-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7f1ae-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f1ae-154">OUTPUTS</span></span>

### <span data-ttu-id="7f1ae-155">System. String</span><span class="sxs-lookup"><span data-stu-id="7f1ae-155">System.String</span></span>

## <span data-ttu-id="7f1ae-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f1ae-156">NOTES</span></span>

## <span data-ttu-id="7f1ae-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f1ae-157">RELATED LINKS</span></span>

[<span data-ttu-id="7f1ae-158">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7f1ae-158">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="7f1ae-159">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7f1ae-159">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="7f1ae-160">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7f1ae-160">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="7f1ae-161">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7f1ae-161">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)