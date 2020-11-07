---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainer.md
ms.openlocfilehash: 23ea79879b7b194b9f761c585087a931f9373886
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575738"
---
# <span data-ttu-id="beb27-101">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="beb27-101">Remove-AzureStorageContainer</span></span>

## <span data-ttu-id="beb27-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="beb27-102">SYNOPSIS</span></span>
<span data-ttu-id="beb27-103">Tar bort den angivna lagrings behållaren.</span><span class="sxs-lookup"><span data-stu-id="beb27-103">Removes the specified storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="beb27-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="beb27-104">SYNTAX</span></span>

```
Remove-AzureStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="beb27-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="beb27-105">DESCRIPTION</span></span>
<span data-ttu-id="beb27-106">Cmdleten **Remove-AzureStorageContainer** tar bort den angivna lagrings behållaren i Azure.</span><span class="sxs-lookup"><span data-stu-id="beb27-106">The **Remove-AzureStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="beb27-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="beb27-107">EXAMPLES</span></span>

### <span data-ttu-id="beb27-108">Exempel 1: ta bort en behållare</span><span class="sxs-lookup"><span data-stu-id="beb27-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzureStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="beb27-109">I det här exemplet tas en container bort med namnet MyTestContainer.</span><span class="sxs-lookup"><span data-stu-id="beb27-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="beb27-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="beb27-110">PARAMETERS</span></span>

### <span data-ttu-id="beb27-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="beb27-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="beb27-112">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="beb27-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="beb27-113">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="beb27-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="beb27-114">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="beb27-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="beb27-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="beb27-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="beb27-116">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="beb27-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="beb27-117">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="beb27-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="beb27-118">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="beb27-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="beb27-119">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="beb27-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="beb27-120">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="beb27-120">The default value is 10.</span></span>

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

### <span data-ttu-id="beb27-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="beb27-121">-Context</span></span>
<span data-ttu-id="beb27-122">Anger en kontext för den behållare som du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="beb27-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="beb27-123">Du kan använda New-AzureStorageContext cmdlet för att skapa den.</span><span class="sxs-lookup"><span data-stu-id="beb27-123">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="beb27-124">-Force</span><span class="sxs-lookup"><span data-stu-id="beb27-124">-Force</span></span>
<span data-ttu-id="beb27-125">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="beb27-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="beb27-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="beb27-126">-Name</span></span>
<span data-ttu-id="beb27-127">Anger namnet på den behållare som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="beb27-127">Specifies the name of the container to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="beb27-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="beb27-128">-PassThru</span></span>
<span data-ttu-id="beb27-129">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="beb27-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="beb27-130">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="beb27-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="beb27-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="beb27-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="beb27-132">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="beb27-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="beb27-133">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="beb27-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="beb27-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="beb27-134">-Confirm</span></span>
<span data-ttu-id="beb27-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="beb27-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="beb27-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beb27-136">-WhatIf</span></span>
<span data-ttu-id="beb27-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="beb27-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="beb27-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="beb27-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="beb27-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beb27-139">CommonParameters</span></span>
<span data-ttu-id="beb27-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beb27-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beb27-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beb27-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beb27-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="beb27-142">INPUTS</span></span>

### <span data-ttu-id="beb27-143">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="beb27-143">IStorageContext</span></span>

<span data-ttu-id="beb27-144">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="beb27-144">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="beb27-145">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="beb27-145">String</span></span>

<span data-ttu-id="beb27-146">Parametern "name" accepterar värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="beb27-146">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="beb27-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="beb27-147">OUTPUTS</span></span>

### <span data-ttu-id="beb27-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="beb27-148">System.Boolean</span></span>

## <span data-ttu-id="beb27-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="beb27-149">NOTES</span></span>

## <span data-ttu-id="beb27-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="beb27-150">RELATED LINKS</span></span>

[<span data-ttu-id="beb27-151">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="beb27-151">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="beb27-152">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="beb27-152">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)