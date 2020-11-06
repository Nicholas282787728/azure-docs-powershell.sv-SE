---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24a61f071e806588976f601df69aa66dbbafc164
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572260"
---
# <span data-ttu-id="69c1b-101">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="69c1b-101">Remove-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="69c1b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69c1b-102">SYNOPSIS</span></span>
<span data-ttu-id="69c1b-103">Tar bort en lagrad åtkomst princip från en lagrings plats.</span><span class="sxs-lookup"><span data-stu-id="69c1b-103">Removes a stored access policy from a Storage share.</span></span>

## <span data-ttu-id="69c1b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69c1b-104">SYNTAX</span></span>

```
Remove-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69c1b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69c1b-105">DESCRIPTION</span></span>
<span data-ttu-id="69c1b-106">Cmdleten **Remove-AzureStorageShareStoredAccessPolicy** tar bort en lagrad åtkomst princip från en Azure Storage-resurs.</span><span class="sxs-lookup"><span data-stu-id="69c1b-106">The **Remove-AzureStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="69c1b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69c1b-107">EXAMPLES</span></span>

### <span data-ttu-id="69c1b-108">Exempel 1: ta bort en lagrad åtkomst princip från en Azure-lagringsenhet</span><span class="sxs-lookup"><span data-stu-id="69c1b-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="69c1b-109">Det här kommandot tar bort en lagrad åtkomst princip med namnet GeneralPolicy från ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="69c1b-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="69c1b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69c1b-110">PARAMETERS</span></span>

### <span data-ttu-id="69c1b-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="69c1b-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="69c1b-112">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="69c1b-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="69c1b-113">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="69c1b-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="69c1b-114">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="69c1b-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="69c1b-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="69c1b-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="69c1b-116">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="69c1b-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="69c1b-117">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="69c1b-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="69c1b-118">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="69c1b-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="69c1b-119">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="69c1b-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="69c1b-120">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="69c1b-120">The default value is 10.</span></span>

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

### <span data-ttu-id="69c1b-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="69c1b-121">-Context</span></span>
<span data-ttu-id="69c1b-122">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="69c1b-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="69c1b-123">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="69c1b-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="69c1b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69c1b-124">-PassThru</span></span>
<span data-ttu-id="69c1b-125">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="69c1b-125">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="69c1b-126">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="69c1b-126">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="69c1b-127">-Princip</span><span class="sxs-lookup"><span data-stu-id="69c1b-127">-Policy</span></span>
<span data-ttu-id="69c1b-128">Anger namnet på den lagrade åtkomst principen som tas bort av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="69c1b-128">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="69c1b-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="69c1b-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="69c1b-130">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="69c1b-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="69c1b-131">-ShareName</span><span class="sxs-lookup"><span data-stu-id="69c1b-131">-ShareName</span></span>
<span data-ttu-id="69c1b-132">Anger namnet på den lagrings resurs som den här cmdleten tar bort en princip för.</span><span class="sxs-lookup"><span data-stu-id="69c1b-132">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

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

### <span data-ttu-id="69c1b-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="69c1b-133">-Confirm</span></span>
<span data-ttu-id="69c1b-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="69c1b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69c1b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69c1b-135">-WhatIf</span></span>
<span data-ttu-id="69c1b-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="69c1b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69c1b-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="69c1b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69c1b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69c1b-138">CommonParameters</span></span>
<span data-ttu-id="69c1b-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69c1b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69c1b-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69c1b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69c1b-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69c1b-141">INPUTS</span></span>

## <span data-ttu-id="69c1b-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69c1b-142">OUTPUTS</span></span>

## <span data-ttu-id="69c1b-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69c1b-143">NOTES</span></span>

## <span data-ttu-id="69c1b-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69c1b-144">RELATED LINKS</span></span>

[<span data-ttu-id="69c1b-145">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="69c1b-145">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="69c1b-146">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="69c1b-146">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="69c1b-147">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="69c1b-147">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="69c1b-148">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="69c1b-148">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
