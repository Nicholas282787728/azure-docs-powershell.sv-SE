---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 08b3ec17476e959aa7190cfb914468eb8ab73775
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755893"
---
# <span data-ttu-id="01905-101">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="01905-101">Remove-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="01905-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="01905-102">SYNOPSIS</span></span>
<span data-ttu-id="01905-103">Tar bort en lagrad åtkomst princip från en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="01905-103">Removes a stored access policy from an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01905-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="01905-104">SYNTAX</span></span>

```
Remove-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01905-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="01905-105">DESCRIPTION</span></span>
<span data-ttu-id="01905-106">Cmdleten **Remove-AzureStorageContainerStoredAccessPolicy** tar bort en lagrad åtkomst princip från en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="01905-106">The **Remove-AzureStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="01905-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="01905-107">EXAMPLES</span></span>

### <span data-ttu-id="01905-108">Exempel 1: ta bort en lagrad åtkomst princip från en lagrings behållare</span><span class="sxs-lookup"><span data-stu-id="01905-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="01905-109">Det här kommandot tar bort en åtkomst princip med namnet Policy03 från den lagrade behållaren med namnet $.</span><span class="sxs-lookup"><span data-stu-id="01905-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="01905-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="01905-110">PARAMETERS</span></span>

### <span data-ttu-id="01905-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="01905-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="01905-112">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="01905-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="01905-113">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="01905-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="01905-114">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="01905-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="01905-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="01905-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="01905-116">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="01905-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="01905-117">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="01905-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="01905-118">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="01905-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="01905-119">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="01905-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="01905-120">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="01905-120">The default value is 10.</span></span>

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

### <span data-ttu-id="01905-121">-Container</span><span class="sxs-lookup"><span data-stu-id="01905-121">-Container</span></span>
<span data-ttu-id="01905-122">Anger namnet på Azure-lagringsplatsen.</span><span class="sxs-lookup"><span data-stu-id="01905-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01905-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="01905-123">-Context</span></span>
<span data-ttu-id="01905-124">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="01905-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="01905-125">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="01905-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="01905-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01905-126">-PassThru</span></span>
<span data-ttu-id="01905-127">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="01905-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="01905-128">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="01905-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="01905-129">-Princip</span><span class="sxs-lookup"><span data-stu-id="01905-129">-Policy</span></span>
<span data-ttu-id="01905-130">Anger namnet på den lagrade åtkomst principen som tas bort av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="01905-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01905-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="01905-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="01905-132">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="01905-132">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="01905-133">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="01905-133">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="01905-134">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="01905-134">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="01905-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="01905-135">-Confirm</span></span>
<span data-ttu-id="01905-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="01905-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01905-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01905-137">-WhatIf</span></span>
<span data-ttu-id="01905-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="01905-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01905-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="01905-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01905-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01905-140">CommonParameters</span></span>
<span data-ttu-id="01905-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01905-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01905-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01905-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01905-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="01905-143">INPUTS</span></span>

### <span data-ttu-id="01905-144">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="01905-144">IStorageContext</span></span>

<span data-ttu-id="01905-145">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="01905-145">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="01905-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="01905-146">OUTPUTS</span></span>

### <span data-ttu-id="01905-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="01905-147">System.Boolean</span></span>

## <span data-ttu-id="01905-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="01905-148">NOTES</span></span>

## <span data-ttu-id="01905-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="01905-149">RELATED LINKS</span></span>

[<span data-ttu-id="01905-150">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="01905-150">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="01905-151">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="01905-151">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="01905-152">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="01905-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="01905-153">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="01905-153">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)