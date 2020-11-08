---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
ms.openlocfilehash: a555e269fd02cb02d420426fed99888b19214f52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089038"
---
# <span data-ttu-id="a19f8-101">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="a19f8-101">New-AzServiceBusQueue</span></span>

## <span data-ttu-id="a19f8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a19f8-102">SYNOPSIS</span></span>
<span data-ttu-id="a19f8-103">Skapar en Service Bus-kö i det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="a19f8-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="a19f8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a19f8-104">SYNTAX</span></span>

```
New-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-EnablePartitioning <Boolean>] [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableBatchedOperations] [-EnableExpress <Boolean>]
 [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>] [-MessageCount <Int64>]
 [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>] [-SizeInBytes <Int64>]
 [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a19f8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a19f8-105">DESCRIPTION</span></span>
<span data-ttu-id="a19f8-106">Cmdleten **New-AzServiceBusQueue** skapar en tjänst buss kö i det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="a19f8-106">The **New-AzServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="a19f8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a19f8-107">EXAMPLES</span></span>

### <span data-ttu-id="a19f8-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a19f8-108">Example 1</span></span>
```
PS C:\> New-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -EnablePartitioning $True

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_example1
Name                                : SB-Queue_example1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 12:37:11 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : False
MaxDeliveryCount                    : 10
MaxSizeInMegabytes                  : 81920
MessageCount                        : 0
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 0
Status                              : Active
UpdatedAt                           : 10/11/2018 12:37:12 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="a19f8-109">Skapar en ny Service Bus-kö `SB-Queue_example1` i det angivna Service Bus-namnområdet `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="a19f8-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="a19f8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a19f8-110">PARAMETERS</span></span>

### <span data-ttu-id="a19f8-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="a19f8-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="a19f8-112">Anger [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) Idle Interval efter vilket kön automatiskt tas bort.</span><span class="sxs-lookup"><span data-stu-id="a19f8-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="a19f8-113">Minsta varaktighet är 5 minuter.</span><span class="sxs-lookup"><span data-stu-id="a19f8-113">The minimum duration is 5 minutes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19f8-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="a19f8-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="a19f8-115">Död Brevering för meddelande</span><span class="sxs-lookup"><span data-stu-id="a19f8-115">Dead Lettering On Message Expiration</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19f8-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="a19f8-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="a19f8-117">TimeSpan to Live-värde.</span><span class="sxs-lookup"><span data-stu-id="a19f8-117">Timespan to live value.</span></span>
<span data-ttu-id="a19f8-118">Det här är den tid som meddelandet upphör att gälla, från och med när meddelandet skickas till Service Bus.</span><span class="sxs-lookup"><span data-stu-id="a19f8-118">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="a19f8-119">Det här är standardvärdet som används när TimeToLive inte är inställt på ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="a19f8-119">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="a19f8-120">Standard = TimeSpan. max och Basic = 14 dagar</span><span class="sxs-lookup"><span data-stu-id="a19f8-120">For Standard = Timespan.Max and Basic = 14 days</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19f8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a19f8-121">-DefaultProfile</span></span>
<span data-ttu-id="a19f8-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a19f8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a19f8-123">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="a19f8-123">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="a19f8-124">Anger tidsfönstret för historik för dubblettidentifiering, ett [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) -värde som definierar varaktigheten för dubblettidentifiering för dubbletter.</span><span class="sxs-lookup"><span data-stu-id="a19f8-124">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) value that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="a19f8-125">Standardvärdet är 10 minuter.</span><span class="sxs-lookup"><span data-stu-id="a19f8-125">The default value is 10 minutes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19f8-126">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="a19f8-126">-EnableBatchedOperations</span></span>
<span data-ttu-id="a19f8-127">Aktivera grupp operationer-värde som anger om grupp operationer på Server sidan är aktiverade</span><span class="sxs-lookup"><span data-stu-id="a19f8-127">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="a19f8-128">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="a19f8-128">-EnableExpress</span></span>
<span data-ttu-id="a19f8-129">EnableExpress – ett värde som anger om Express-enheter är aktiverade.</span><span class="sxs-lookup"><span data-stu-id="a19f8-129">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="a19f8-130">En Express-kö innehåller ett meddelande i minnet tillfälligt innan det skrivs till beständig lagring.</span><span class="sxs-lookup"><span data-stu-id="a19f8-130">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19f8-131">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="a19f8-131">-EnablePartitioning</span></span>
<span data-ttu-id="a19f8-132">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="a19f8-132">EnablePartitioning</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19f8-133">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="a19f8-133">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="a19f8-134">Namn på kö för att vidarekoppla meddelandet om obeställbara meddelanden</span><span class="sxs-lookup"><span data-stu-id="a19f8-134">Queue/Topic name to forward the Dead Letter message</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19f8-135">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="a19f8-135">-ForwardTo</span></span>
<span data-ttu-id="a19f8-136">Namn på kö/ämne för att vidarekoppla meddelanden</span><span class="sxs-lookup"><span data-stu-id="a19f8-136">Queue/Topic name to forward the messages</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19f8-137">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="a19f8-137">-LockDuration</span></span>
<span data-ttu-id="a19f8-138">Lås varaktighet</span><span class="sxs-lookup"><span data-stu-id="a19f8-138">Lock Duration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19f8-139">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="a19f8-139">-MaxDeliveryCount</span></span>
<span data-ttu-id="a19f8-140">MaxDeliveryCount-högsta antal leveranser.</span><span class="sxs-lookup"><span data-stu-id="a19f8-140">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="a19f8-141">Ett meddelande deadlettered automatiskt efter detta antal leveranser.</span><span class="sxs-lookup"><span data-stu-id="a19f8-141">A message is automatically deadlettered after this number of deliveries.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19f8-142">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="a19f8-142">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="a19f8-143">MaxSizeInMegabytes-köns maximala storlek i MB, vilket är storleken på det allokerade minnet för kön. Standardvärdet är 1024.</span><span class="sxs-lookup"><span data-stu-id="a19f8-143">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.Default is 1024.</span></span> <span data-ttu-id="a19f8-144">Max för standard-SKU är 5120 och för Premium SKU är 81920, tillåtna värden: 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span><span class="sxs-lookup"><span data-stu-id="a19f8-144">Max for Standard SKU is 5120 and for Premium SKU is 81920, Allowed values : 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19f8-145">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="a19f8-145">-MessageCount</span></span>
<span data-ttu-id="a19f8-146">MessageCount-antalet meddelanden i kön</span><span class="sxs-lookup"><span data-stu-id="a19f8-146">MessageCount - the number of messages in the queue</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19f8-147">-Namn</span><span class="sxs-lookup"><span data-stu-id="a19f8-147">-Name</span></span>
<span data-ttu-id="a19f8-148">Könamn</span><span class="sxs-lookup"><span data-stu-id="a19f8-148">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19f8-149">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="a19f8-149">-Namespace</span></span>
<span data-ttu-id="a19f8-150">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="a19f8-150">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19f8-151">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="a19f8-151">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="a19f8-152">RequiresDuplicateDetection – ett värde som anger om kön stöder konceptet session</span><span class="sxs-lookup"><span data-stu-id="a19f8-152">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19f8-153">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="a19f8-153">-RequiresSession</span></span>
<span data-ttu-id="a19f8-154">RequiresSession-det värde som anger om kön använder sessioner</span><span class="sxs-lookup"><span data-stu-id="a19f8-154">RequiresSession - the value indicating if this queue uses sessions</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19f8-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a19f8-155">-ResourceGroupName</span></span>
<span data-ttu-id="a19f8-156">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="a19f8-156">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19f8-157">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="a19f8-157">-SizeInBytes</span></span>
<span data-ttu-id="a19f8-158">SizeInBytes-köns storlek i byte</span><span class="sxs-lookup"><span data-stu-id="a19f8-158">SizeInBytes - the size of the queue in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19f8-159">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a19f8-159">-Confirm</span></span>
<span data-ttu-id="a19f8-160">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a19f8-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a19f8-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a19f8-161">-WhatIf</span></span>
<span data-ttu-id="a19f8-162">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a19f8-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a19f8-163">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a19f8-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a19f8-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a19f8-164">CommonParameters</span></span>
<span data-ttu-id="a19f8-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a19f8-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a19f8-166">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a19f8-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a19f8-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a19f8-167">INPUTS</span></span>

### <span data-ttu-id="a19f8-168">System. String</span><span class="sxs-lookup"><span data-stu-id="a19f8-168">System.String</span></span>

### <span data-ttu-id="a19f8-169">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a19f8-169">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a19f8-170">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a19f8-170">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a19f8-171">System. Nullable ' 1 [[system. Int64, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a19f8-171">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a19f8-172">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a19f8-172">OUTPUTS</span></span>

### <span data-ttu-id="a19f8-173">Microsoft. Azure. commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="a19f8-173">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="a19f8-174">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a19f8-174">NOTES</span></span>

## <span data-ttu-id="a19f8-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a19f8-175">RELATED LINKS</span></span>
