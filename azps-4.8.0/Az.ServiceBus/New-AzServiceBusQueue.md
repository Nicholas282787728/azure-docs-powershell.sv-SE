---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
ms.openlocfilehash: 16a7de817250170cf39a02200cee67c028249e1f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258588"
---
# <span data-ttu-id="b685f-101">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="b685f-101">New-AzServiceBusQueue</span></span>

## <span data-ttu-id="b685f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b685f-102">SYNOPSIS</span></span>
<span data-ttu-id="b685f-103">Skapar en Service Bus-kö i det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="b685f-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="b685f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b685f-104">SYNTAX</span></span>

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

## <span data-ttu-id="b685f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b685f-105">DESCRIPTION</span></span>
<span data-ttu-id="b685f-106">Cmdleten **New-AzServiceBusQueue** skapar en tjänst buss kö i det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="b685f-106">The **New-AzServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="b685f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b685f-107">EXAMPLES</span></span>

### <span data-ttu-id="b685f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b685f-108">Example 1</span></span>
```powershell
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

<span data-ttu-id="b685f-109">Skapar en ny Service Bus-kö `SB-Queue_example1` i det angivna Service Bus-namnområdet `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="b685f-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="b685f-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b685f-110">Example 2</span></span>

<span data-ttu-id="b685f-111">Skapar en Service Bus-kö i det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="b685f-111">Creates a Service Bus queue in the specified Service Bus namespace.</span></span> <span data-ttu-id="b685f-112">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="b685f-112">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzServiceBusQueue -EnablePartitioning $true -MaxSizeInMegabytes <Int64> -Name SB-Queue_example1 -Namespace SB-Example1 -ResourceGroupName Default-ServiceBus-WestUS
```

## <span data-ttu-id="b685f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b685f-113">PARAMETERS</span></span>

### <span data-ttu-id="b685f-114">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="b685f-114">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="b685f-115">Anger [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) Idle Interval efter vilket kön automatiskt tas bort.</span><span class="sxs-lookup"><span data-stu-id="b685f-115">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="b685f-116">Minsta varaktighet är 5 minuter.</span><span class="sxs-lookup"><span data-stu-id="b685f-116">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="b685f-117">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="b685f-117">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="b685f-118">Död Brevering för meddelande</span><span class="sxs-lookup"><span data-stu-id="b685f-118">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="b685f-119">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="b685f-119">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="b685f-120">TimeSpan to Live-värde.</span><span class="sxs-lookup"><span data-stu-id="b685f-120">Timespan to live value.</span></span>
<span data-ttu-id="b685f-121">Det här är den tid som meddelandet upphör att gälla, från och med när meddelandet skickas till Service Bus.</span><span class="sxs-lookup"><span data-stu-id="b685f-121">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="b685f-122">Det här är standardvärdet som används när TimeToLive inte är inställt på ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="b685f-122">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="b685f-123">Standard = TimeSpan. max och Basic = 14 dagar</span><span class="sxs-lookup"><span data-stu-id="b685f-123">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="b685f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b685f-124">-DefaultProfile</span></span>
<span data-ttu-id="b685f-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b685f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b685f-126">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="b685f-126">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="b685f-127">Anger tidsfönstret för historik för dubblettidentifiering, ett [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) -värde som definierar varaktigheten för dubblettidentifiering för dubbletter.</span><span class="sxs-lookup"><span data-stu-id="b685f-127">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) value that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="b685f-128">Standardvärdet är 10 minuter.</span><span class="sxs-lookup"><span data-stu-id="b685f-128">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="b685f-129">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="b685f-129">-EnableBatchedOperations</span></span>
<span data-ttu-id="b685f-130">Aktivera grupp operationer-värde som anger om grupp operationer på Server sidan är aktiverade</span><span class="sxs-lookup"><span data-stu-id="b685f-130">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="b685f-131">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="b685f-131">-EnableExpress</span></span>
<span data-ttu-id="b685f-132">EnableExpress – ett värde som anger om Express-enheter är aktiverade.</span><span class="sxs-lookup"><span data-stu-id="b685f-132">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="b685f-133">En Express-kö innehåller ett meddelande i minnet tillfälligt innan det skrivs till beständig lagring.</span><span class="sxs-lookup"><span data-stu-id="b685f-133">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="b685f-134">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="b685f-134">-EnablePartitioning</span></span>
<span data-ttu-id="b685f-135">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="b685f-135">EnablePartitioning</span></span>

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

### <span data-ttu-id="b685f-136">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="b685f-136">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="b685f-137">Namn på kö för att vidarekoppla meddelandet om obeställbara meddelanden</span><span class="sxs-lookup"><span data-stu-id="b685f-137">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="b685f-138">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="b685f-138">-ForwardTo</span></span>
<span data-ttu-id="b685f-139">Namn på kö/ämne för att vidarekoppla meddelanden</span><span class="sxs-lookup"><span data-stu-id="b685f-139">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="b685f-140">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="b685f-140">-LockDuration</span></span>
<span data-ttu-id="b685f-141">Lås varaktighet</span><span class="sxs-lookup"><span data-stu-id="b685f-141">Lock Duration</span></span>

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

### <span data-ttu-id="b685f-142">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="b685f-142">-MaxDeliveryCount</span></span>
<span data-ttu-id="b685f-143">MaxDeliveryCount-högsta antal leveranser.</span><span class="sxs-lookup"><span data-stu-id="b685f-143">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="b685f-144">Ett meddelande deadlettered automatiskt efter detta antal leveranser.</span><span class="sxs-lookup"><span data-stu-id="b685f-144">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="b685f-145">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="b685f-145">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="b685f-146">MaxSizeInMegabytes-köns maximala storlek i MB, vilket är storleken på det allokerade minnet för kön. Standardvärdet är 1024.</span><span class="sxs-lookup"><span data-stu-id="b685f-146">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.Default is 1024.</span></span> <span data-ttu-id="b685f-147">Max för standard-SKU är 5120 och för Premium SKU är 81920, tillåtna värden: 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span><span class="sxs-lookup"><span data-stu-id="b685f-147">Max for Standard SKU is 5120 and for Premium SKU is 81920, Allowed values : 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span></span>

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

### <span data-ttu-id="b685f-148">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="b685f-148">-MessageCount</span></span>
<span data-ttu-id="b685f-149">MessageCount-antalet meddelanden i kön</span><span class="sxs-lookup"><span data-stu-id="b685f-149">MessageCount - the number of messages in the queue</span></span>

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

### <span data-ttu-id="b685f-150">-Namn</span><span class="sxs-lookup"><span data-stu-id="b685f-150">-Name</span></span>
<span data-ttu-id="b685f-151">Könamn</span><span class="sxs-lookup"><span data-stu-id="b685f-151">Queue Name</span></span>

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

### <span data-ttu-id="b685f-152">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="b685f-152">-Namespace</span></span>
<span data-ttu-id="b685f-153">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="b685f-153">Namespace Name</span></span>

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

### <span data-ttu-id="b685f-154">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="b685f-154">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="b685f-155">RequiresDuplicateDetection – ett värde som anger om kön stöder konceptet session</span><span class="sxs-lookup"><span data-stu-id="b685f-155">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

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

### <span data-ttu-id="b685f-156">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="b685f-156">-RequiresSession</span></span>
<span data-ttu-id="b685f-157">RequiresSession-det värde som anger om kön använder sessioner</span><span class="sxs-lookup"><span data-stu-id="b685f-157">RequiresSession - the value indicating if this queue uses sessions</span></span>

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

### <span data-ttu-id="b685f-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b685f-158">-ResourceGroupName</span></span>
<span data-ttu-id="b685f-159">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="b685f-159">The name of the resource group</span></span>

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

### <span data-ttu-id="b685f-160">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="b685f-160">-SizeInBytes</span></span>
<span data-ttu-id="b685f-161">SizeInBytes-köns storlek i byte</span><span class="sxs-lookup"><span data-stu-id="b685f-161">SizeInBytes - the size of the queue in bytes</span></span>

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

### <span data-ttu-id="b685f-162">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b685f-162">-Confirm</span></span>
<span data-ttu-id="b685f-163">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b685f-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b685f-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b685f-164">-WhatIf</span></span>
<span data-ttu-id="b685f-165">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b685f-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b685f-166">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b685f-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b685f-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b685f-167">CommonParameters</span></span>
<span data-ttu-id="b685f-168">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b685f-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b685f-169">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b685f-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b685f-170">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b685f-170">INPUTS</span></span>

### <span data-ttu-id="b685f-171">System. String</span><span class="sxs-lookup"><span data-stu-id="b685f-171">System.String</span></span>

### <span data-ttu-id="b685f-172">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b685f-172">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b685f-173">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b685f-173">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b685f-174">System. Nullable ' 1 [[system. Int64, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b685f-174">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b685f-175">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b685f-175">OUTPUTS</span></span>

### <span data-ttu-id="b685f-176">Microsoft. Azure. commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="b685f-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="b685f-177">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b685f-177">NOTES</span></span>

## <span data-ttu-id="b685f-178">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b685f-178">RELATED LINKS</span></span>
