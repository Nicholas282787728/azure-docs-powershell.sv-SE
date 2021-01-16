---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 1b8667d08e02c9294a18f4cbf84cb27085cbc118
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522011"
---
# <span data-ttu-id="2a95b-101">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2a95b-101">Remove-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="2a95b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a95b-102">SYNOPSIS</span></span>
<span data-ttu-id="2a95b-103">Tar bort en lagrad åtkomst princip från en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="2a95b-103">Removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="2a95b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a95b-104">SYNTAX</span></span>

```
Remove-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a95b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a95b-105">DESCRIPTION</span></span>
<span data-ttu-id="2a95b-106">Cmdleten **Remove-AzStorageContainerStoredAccessPolicy** tar bort en lagrad åtkomst princip från en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="2a95b-106">The **Remove-AzStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="2a95b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a95b-107">EXAMPLES</span></span>

### <span data-ttu-id="2a95b-108">Exempel 1: ta bort en lagrad åtkomst princip från en lagrings behållare</span><span class="sxs-lookup"><span data-stu-id="2a95b-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="2a95b-109">Det här kommandot tar bort en åtkomst princip med namnet Policy03 från den lagrade behållaren med namnet $.</span><span class="sxs-lookup"><span data-stu-id="2a95b-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="2a95b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a95b-110">PARAMETERS</span></span>

### <span data-ttu-id="2a95b-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2a95b-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2a95b-112">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="2a95b-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2a95b-113">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="2a95b-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2a95b-114">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="2a95b-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2a95b-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2a95b-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2a95b-116">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="2a95b-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2a95b-117">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="2a95b-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2a95b-118">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="2a95b-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2a95b-119">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="2a95b-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2a95b-120">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="2a95b-120">The default value is 10.</span></span>

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

### <span data-ttu-id="2a95b-121">-Container</span><span class="sxs-lookup"><span data-stu-id="2a95b-121">-Container</span></span>
<span data-ttu-id="2a95b-122">Anger namnet på Azure-lagringsplatsen.</span><span class="sxs-lookup"><span data-stu-id="2a95b-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a95b-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2a95b-123">-Context</span></span>
<span data-ttu-id="2a95b-124">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="2a95b-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2a95b-125">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="2a95b-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2a95b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a95b-126">-DefaultProfile</span></span>
<span data-ttu-id="2a95b-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2a95b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a95b-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a95b-128">-PassThru</span></span>
<span data-ttu-id="2a95b-129">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="2a95b-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="2a95b-130">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="2a95b-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="2a95b-131">-Princip</span><span class="sxs-lookup"><span data-stu-id="2a95b-131">-Policy</span></span>
<span data-ttu-id="2a95b-132">Anger namnet på den lagrade åtkomst principen som tas bort av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2a95b-132">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a95b-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2a95b-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2a95b-134">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="2a95b-134">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2a95b-135">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="2a95b-135">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2a95b-136">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="2a95b-136">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2a95b-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2a95b-137">-Confirm</span></span>
<span data-ttu-id="2a95b-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2a95b-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a95b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a95b-139">-WhatIf</span></span>
<span data-ttu-id="2a95b-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2a95b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a95b-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2a95b-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a95b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a95b-142">CommonParameters</span></span>
<span data-ttu-id="2a95b-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a95b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a95b-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a95b-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a95b-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a95b-145">INPUTS</span></span>

### <span data-ttu-id="2a95b-146">System. String</span><span class="sxs-lookup"><span data-stu-id="2a95b-146">System.String</span></span>

### <span data-ttu-id="2a95b-147">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2a95b-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2a95b-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a95b-148">OUTPUTS</span></span>

### <span data-ttu-id="2a95b-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2a95b-149">System.Boolean</span></span>

## <span data-ttu-id="2a95b-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a95b-150">NOTES</span></span>

## <span data-ttu-id="2a95b-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a95b-151">RELATED LINKS</span></span>

[<span data-ttu-id="2a95b-152">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2a95b-152">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="2a95b-153">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2a95b-153">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="2a95b-154">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2a95b-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="2a95b-155">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2a95b-155">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)
