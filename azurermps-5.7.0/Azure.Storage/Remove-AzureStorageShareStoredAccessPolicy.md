---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShareStoredAccessPolicy.md
ms.openlocfilehash: cb39d9800271d68f8ac78ebffc9ed3345209177c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574457"
---
# <span data-ttu-id="3f8e7-101">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3f8e7-101">Remove-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="3f8e7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f8e7-102">SYNOPSIS</span></span>
<span data-ttu-id="3f8e7-103">Tar bort en lagrad åtkomst princip från en lagrings plats.</span><span class="sxs-lookup"><span data-stu-id="3f8e7-103">Removes a stored access policy from a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f8e7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f8e7-104">SYNTAX</span></span>

```
Remove-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f8e7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f8e7-105">DESCRIPTION</span></span>
<span data-ttu-id="3f8e7-106">Cmdleten **Remove-AzureStorageShareStoredAccessPolicy** tar bort en lagrad åtkomst princip från en Azure Storage-resurs.</span><span class="sxs-lookup"><span data-stu-id="3f8e7-106">The **Remove-AzureStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="3f8e7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f8e7-107">EXAMPLES</span></span>

### <span data-ttu-id="3f8e7-108">Exempel 1: ta bort en lagrad åtkomst princip från en Azure-lagringsenhet</span><span class="sxs-lookup"><span data-stu-id="3f8e7-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="3f8e7-109">Det här kommandot tar bort en lagrad åtkomst princip med namnet GeneralPolicy från ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="3f8e7-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="3f8e7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f8e7-110">PARAMETERS</span></span>

### <span data-ttu-id="3f8e7-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3f8e7-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3f8e7-112">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="3f8e7-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3f8e7-113">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="3f8e7-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3f8e7-114">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="3f8e7-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3f8e7-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3f8e7-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3f8e7-116">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="3f8e7-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3f8e7-117">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="3f8e7-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3f8e7-118">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="3f8e7-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3f8e7-119">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="3f8e7-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3f8e7-120">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="3f8e7-120">The default value is 10.</span></span>

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

### <span data-ttu-id="3f8e7-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="3f8e7-121">-Context</span></span>
<span data-ttu-id="3f8e7-122">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="3f8e7-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3f8e7-123">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="3f8e7-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="3f8e7-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f8e7-124">-PassThru</span></span>
<span data-ttu-id="3f8e7-125">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="3f8e7-125">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="3f8e7-126">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="3f8e7-126">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="3f8e7-127">-Princip</span><span class="sxs-lookup"><span data-stu-id="3f8e7-127">-Policy</span></span>
<span data-ttu-id="3f8e7-128">Anger namnet på den lagrade åtkomst principen som tas bort av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3f8e7-128">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3f8e7-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3f8e7-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3f8e7-130">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="3f8e7-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="3f8e7-131">-ShareName</span><span class="sxs-lookup"><span data-stu-id="3f8e7-131">-ShareName</span></span>
<span data-ttu-id="3f8e7-132">Anger namnet på den lagrings resurs som den här cmdleten tar bort en princip för.</span><span class="sxs-lookup"><span data-stu-id="3f8e7-132">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

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

### <span data-ttu-id="3f8e7-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3f8e7-133">-Confirm</span></span>
<span data-ttu-id="3f8e7-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3f8e7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f8e7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f8e7-135">-WhatIf</span></span>
<span data-ttu-id="3f8e7-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3f8e7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f8e7-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3f8e7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f8e7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f8e7-138">CommonParameters</span></span>
<span data-ttu-id="3f8e7-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f8e7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f8e7-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f8e7-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f8e7-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f8e7-141">INPUTS</span></span>

### <span data-ttu-id="3f8e7-142">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3f8e7-142">IStorageContext</span></span>

<span data-ttu-id="3f8e7-143">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="3f8e7-143">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="3f8e7-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f8e7-144">OUTPUTS</span></span>

### <span data-ttu-id="3f8e7-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3f8e7-145">System.Boolean</span></span>

## <span data-ttu-id="3f8e7-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f8e7-146">NOTES</span></span>

## <span data-ttu-id="3f8e7-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f8e7-147">RELATED LINKS</span></span>

[<span data-ttu-id="3f8e7-148">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3f8e7-148">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="3f8e7-149">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3f8e7-149">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="3f8e7-150">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3f8e7-150">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="3f8e7-151">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3f8e7-151">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
