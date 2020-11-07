---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
ms.openlocfilehash: b9ad7c729395115845349c1e39f8d90666a4fcb8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746908"
---
# <span data-ttu-id="c07fe-101">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="c07fe-101">New-AzServiceBusQueue</span></span>

## <span data-ttu-id="c07fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c07fe-102">SYNOPSIS</span></span>
<span data-ttu-id="c07fe-103">Skapar en Service Bus-kö i det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="c07fe-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="c07fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c07fe-104">SYNTAX</span></span>

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

## <span data-ttu-id="c07fe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c07fe-105">DESCRIPTION</span></span>
<span data-ttu-id="c07fe-106">Cmdleten **New-AzServiceBusQueue** skapar en tjänst buss kö i det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="c07fe-106">The **New-AzServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="c07fe-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c07fe-107">EXAMPLES</span></span>

### <span data-ttu-id="c07fe-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c07fe-108">Example 1</span></span>
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

<span data-ttu-id="c07fe-109">Skapar en ny Service Bus-kö `SB-Queue_example1` i det angivna Service Bus-namnområdet `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="c07fe-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="c07fe-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c07fe-110">PARAMETERS</span></span>

### <span data-ttu-id="c07fe-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="c07fe-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="c07fe-112">Anger [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) Idle Interval efter vilket kön automatiskt tas bort.</span><span class="sxs-lookup"><span data-stu-id="c07fe-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="c07fe-113">Minsta varaktighet är 5 minuter.</span><span class="sxs-lookup"><span data-stu-id="c07fe-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="c07fe-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="c07fe-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="c07fe-115">Död Brevering för meddelande</span><span class="sxs-lookup"><span data-stu-id="c07fe-115">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="c07fe-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="c07fe-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="c07fe-117">TimeSpan to Live-värde.</span><span class="sxs-lookup"><span data-stu-id="c07fe-117">Timespan to live value.</span></span>
<span data-ttu-id="c07fe-118">Det här är den tid som meddelandet upphör att gälla, från och med när meddelandet skickas till Service Bus.</span><span class="sxs-lookup"><span data-stu-id="c07fe-118">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="c07fe-119">Det här är standardvärdet som används när TimeToLive inte är inställt på ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="c07fe-119">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="c07fe-120">Standard = TimeSpan. max och Basic = 14 dyas</span><span class="sxs-lookup"><span data-stu-id="c07fe-120">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="c07fe-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c07fe-121">-DefaultProfile</span></span>
<span data-ttu-id="c07fe-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c07fe-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c07fe-123">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="c07fe-123">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="c07fe-124">Visar fönstret historik tid för dubblettidentifiering, ett [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) -valuethat definierar varaktigheten för historiken för dubblettidentifiering.</span><span class="sxs-lookup"><span data-stu-id="c07fe-124">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="c07fe-125">Standardvärdet är 10 minuter.</span><span class="sxs-lookup"><span data-stu-id="c07fe-125">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="c07fe-126">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="c07fe-126">-EnableBatchedOperations</span></span>
<span data-ttu-id="c07fe-127">Aktivera grupp operationer-värde som anger om grupp operationer på Server sidan är aktiverade</span><span class="sxs-lookup"><span data-stu-id="c07fe-127">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="c07fe-128">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="c07fe-128">-EnableExpress</span></span>
<span data-ttu-id="c07fe-129">EnableExpress – ett värde som anger om Express-enheter är aktiverade.</span><span class="sxs-lookup"><span data-stu-id="c07fe-129">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="c07fe-130">En Express-kö innehåller ett meddelande i minnet tillfälligt innan det skrivs till beständig lagring.</span><span class="sxs-lookup"><span data-stu-id="c07fe-130">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="c07fe-131">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="c07fe-131">-EnablePartitioning</span></span>
<span data-ttu-id="c07fe-132">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="c07fe-132">EnablePartitioning</span></span>

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

### <span data-ttu-id="c07fe-133">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="c07fe-133">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="c07fe-134">Namn på kö för att vidarekoppla meddelandet om obeställbara meddelanden</span><span class="sxs-lookup"><span data-stu-id="c07fe-134">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="c07fe-135">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="c07fe-135">-ForwardTo</span></span>
<span data-ttu-id="c07fe-136">Namn på kö/ämne för att vidarekoppla meddelanden</span><span class="sxs-lookup"><span data-stu-id="c07fe-136">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="c07fe-137">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="c07fe-137">-LockDuration</span></span>
<span data-ttu-id="c07fe-138">Lås varaktighet</span><span class="sxs-lookup"><span data-stu-id="c07fe-138">Lock Duration</span></span>

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

### <span data-ttu-id="c07fe-139">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="c07fe-139">-MaxDeliveryCount</span></span>
<span data-ttu-id="c07fe-140">MaxDeliveryCount-högsta antal leveranser.</span><span class="sxs-lookup"><span data-stu-id="c07fe-140">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="c07fe-141">Ett meddelande deadlettered automatiskt efter detta antal leveranser.</span><span class="sxs-lookup"><span data-stu-id="c07fe-141">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="c07fe-142">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="c07fe-142">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="c07fe-143">MaxSizeInMegabytes-köns maximala storlek i MB, vilket är storleken på det allokerade minnet för kön.</span><span class="sxs-lookup"><span data-stu-id="c07fe-143">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

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

### <span data-ttu-id="c07fe-144">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="c07fe-144">-MessageCount</span></span>
<span data-ttu-id="c07fe-145">MessageCount-antalet meddelanden i kön</span><span class="sxs-lookup"><span data-stu-id="c07fe-145">MessageCount - the number of messages in the queue</span></span>

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

### <span data-ttu-id="c07fe-146">-Namn</span><span class="sxs-lookup"><span data-stu-id="c07fe-146">-Name</span></span>
<span data-ttu-id="c07fe-147">Könamn</span><span class="sxs-lookup"><span data-stu-id="c07fe-147">Queue Name</span></span>

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

### <span data-ttu-id="c07fe-148">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="c07fe-148">-Namespace</span></span>
<span data-ttu-id="c07fe-149">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="c07fe-149">Namespace Name</span></span>

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

### <span data-ttu-id="c07fe-150">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="c07fe-150">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="c07fe-151">RequiresDuplicateDetection – ett värde som anger om kön stöder konceptet session</span><span class="sxs-lookup"><span data-stu-id="c07fe-151">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

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

### <span data-ttu-id="c07fe-152">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="c07fe-152">-RequiresSession</span></span>
<span data-ttu-id="c07fe-153">RequiresSession-det värde som anger om denna kö kräver dubblettidentifiering</span><span class="sxs-lookup"><span data-stu-id="c07fe-153">RequiresSession - the value indicating if this queue requires duplicate detection</span></span>

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

### <span data-ttu-id="c07fe-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c07fe-154">-ResourceGroupName</span></span>
<span data-ttu-id="c07fe-155">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="c07fe-155">The name of the resource group</span></span>

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

### <span data-ttu-id="c07fe-156">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="c07fe-156">-SizeInBytes</span></span>
<span data-ttu-id="c07fe-157">SizeInBytes-köns storlek i byte</span><span class="sxs-lookup"><span data-stu-id="c07fe-157">SizeInBytes - the size of the queue in bytes</span></span>

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

### <span data-ttu-id="c07fe-158">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c07fe-158">-Confirm</span></span>
<span data-ttu-id="c07fe-159">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c07fe-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c07fe-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c07fe-160">-WhatIf</span></span>
<span data-ttu-id="c07fe-161">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c07fe-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c07fe-162">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c07fe-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c07fe-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c07fe-163">CommonParameters</span></span>
<span data-ttu-id="c07fe-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c07fe-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c07fe-165">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c07fe-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c07fe-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c07fe-166">INPUTS</span></span>

### <span data-ttu-id="c07fe-167">System. String</span><span class="sxs-lookup"><span data-stu-id="c07fe-167">System.String</span></span>

### <span data-ttu-id="c07fe-168">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c07fe-168">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c07fe-169">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c07fe-169">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c07fe-170">System. Nullable ' 1 [[system. Int64, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c07fe-170">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c07fe-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c07fe-171">OUTPUTS</span></span>

### <span data-ttu-id="c07fe-172">Microsoft. Azure. commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="c07fe-172">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="c07fe-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c07fe-173">NOTES</span></span>

## <span data-ttu-id="c07fe-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c07fe-174">RELATED LINKS</span></span>
