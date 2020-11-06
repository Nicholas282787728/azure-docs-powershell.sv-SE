---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 29e2c0f04dff07e76907ee67c3e012c2b67c1582
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579976"
---
# <span data-ttu-id="e39ea-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="e39ea-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="e39ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e39ea-102">SYNOPSIS</span></span>
<span data-ttu-id="e39ea-103">Skapar en Service Bus-kö i det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="e39ea-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e39ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e39ea-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-EnablePartitioning <Boolean>] [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableBatchedOperations] [-EnableExpress <Boolean>]
 [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>] [-MessageCount <Int64>]
 [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>] [-SizeInBytes <Int64>]
 [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e39ea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e39ea-105">DESCRIPTION</span></span>
<span data-ttu-id="e39ea-106">Cmdleten **New-AzureRmServiceBusQueue** skapar en tjänst buss kö i det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="e39ea-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="e39ea-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e39ea-107">EXAMPLES</span></span>

### <span data-ttu-id="e39ea-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e39ea-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -EnablePartitioning $True

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

<span data-ttu-id="e39ea-109">Skapar en ny Service Bus-kö `SB-Queue_example1` i det angivna Service Bus-namnområdet `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="e39ea-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="e39ea-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e39ea-110">PARAMETERS</span></span>

### <span data-ttu-id="e39ea-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="e39ea-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="e39ea-112">Anger [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) Idle Interval efter vilket kön automatiskt tas bort.</span><span class="sxs-lookup"><span data-stu-id="e39ea-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="e39ea-113">Minsta varaktighet är 5 minuter.</span><span class="sxs-lookup"><span data-stu-id="e39ea-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="e39ea-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="e39ea-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="e39ea-115">Död Brevering för meddelande</span><span class="sxs-lookup"><span data-stu-id="e39ea-115">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="e39ea-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="e39ea-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="e39ea-117">TimeSpan to Live-värde.</span><span class="sxs-lookup"><span data-stu-id="e39ea-117">Timespan to live value.</span></span>
<span data-ttu-id="e39ea-118">Det här är den tid som meddelandet upphör att gälla, från och med när meddelandet skickas till Service Bus.</span><span class="sxs-lookup"><span data-stu-id="e39ea-118">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="e39ea-119">Det här är standardvärdet som används när TimeToLive inte är inställt på ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="e39ea-119">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="e39ea-120">Standard = TimeSpan. max och Basic = 14 dyas</span><span class="sxs-lookup"><span data-stu-id="e39ea-120">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="e39ea-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e39ea-121">-DefaultProfile</span></span>
<span data-ttu-id="e39ea-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e39ea-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ea-123">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="e39ea-123">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="e39ea-124">Visar fönstret historik tid för dubblettidentifiering, ett [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) -valuethat definierar varaktigheten för historiken för dubblettidentifiering.</span><span class="sxs-lookup"><span data-stu-id="e39ea-124">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="e39ea-125">Standardvärdet är 10 minuter.</span><span class="sxs-lookup"><span data-stu-id="e39ea-125">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="e39ea-126">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="e39ea-126">-EnableBatchedOperations</span></span>
<span data-ttu-id="e39ea-127">Aktivera grupp operationer-värde som anger om grupp operationer på Server sidan är aktiverade</span><span class="sxs-lookup"><span data-stu-id="e39ea-127">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="e39ea-128">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="e39ea-128">-EnableExpress</span></span>
<span data-ttu-id="e39ea-129">EnableExpress – ett värde som anger om Express-enheter är aktiverade.</span><span class="sxs-lookup"><span data-stu-id="e39ea-129">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="e39ea-130">En Express-kö innehåller ett meddelande i minnet tillfälligt innan det skrivs till beständig lagring.</span><span class="sxs-lookup"><span data-stu-id="e39ea-130">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="e39ea-131">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="e39ea-131">-EnablePartitioning</span></span>
<span data-ttu-id="e39ea-132">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="e39ea-132">EnablePartitioning</span></span>

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

### <span data-ttu-id="e39ea-133">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="e39ea-133">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="e39ea-134">Namn på kö för att vidarekoppla meddelandet om obeställbara meddelanden</span><span class="sxs-lookup"><span data-stu-id="e39ea-134">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="e39ea-135">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="e39ea-135">-ForwardTo</span></span>
<span data-ttu-id="e39ea-136">Namn på kö/ämne för att vidarekoppla meddelanden</span><span class="sxs-lookup"><span data-stu-id="e39ea-136">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="e39ea-137">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="e39ea-137">-LockDuration</span></span>
<span data-ttu-id="e39ea-138">Lås varaktighet</span><span class="sxs-lookup"><span data-stu-id="e39ea-138">Lock Duration</span></span>

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

### <span data-ttu-id="e39ea-139">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="e39ea-139">-MaxDeliveryCount</span></span>
<span data-ttu-id="e39ea-140">MaxDeliveryCount-högsta antal leveranser.</span><span class="sxs-lookup"><span data-stu-id="e39ea-140">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="e39ea-141">Ett meddelande deadlettered automatiskt efter detta antal leveranser.</span><span class="sxs-lookup"><span data-stu-id="e39ea-141">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="e39ea-142">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="e39ea-142">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="e39ea-143">MaxSizeInMegabytes-köns maximala storlek i MB, vilket är storleken på det allokerade minnet för kön.</span><span class="sxs-lookup"><span data-stu-id="e39ea-143">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

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

### <span data-ttu-id="e39ea-144">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="e39ea-144">-MessageCount</span></span>
<span data-ttu-id="e39ea-145">MessageCount-antalet meddelanden i kön</span><span class="sxs-lookup"><span data-stu-id="e39ea-145">MessageCount - the number of messages in the queue</span></span>

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

### <span data-ttu-id="e39ea-146">-Namn</span><span class="sxs-lookup"><span data-stu-id="e39ea-146">-Name</span></span>
<span data-ttu-id="e39ea-147">Könamn</span><span class="sxs-lookup"><span data-stu-id="e39ea-147">Queue Name</span></span>

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

### <span data-ttu-id="e39ea-148">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="e39ea-148">-Namespace</span></span>
<span data-ttu-id="e39ea-149">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="e39ea-149">Namespace Name</span></span>

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

### <span data-ttu-id="e39ea-150">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="e39ea-150">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="e39ea-151">RequiresDuplicateDetection – ett värde som anger om kön stöder konceptet session</span><span class="sxs-lookup"><span data-stu-id="e39ea-151">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

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

### <span data-ttu-id="e39ea-152">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="e39ea-152">-RequiresSession</span></span>
<span data-ttu-id="e39ea-153">RequiresSession-det värde som anger om denna kö kräver dubblettidentifiering</span><span class="sxs-lookup"><span data-stu-id="e39ea-153">RequiresSession - the value indicating if this queue requires duplicate detection</span></span>

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

### <span data-ttu-id="e39ea-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e39ea-154">-ResourceGroupName</span></span>
<span data-ttu-id="e39ea-155">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="e39ea-155">The name of the resource group</span></span>

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

### <span data-ttu-id="e39ea-156">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="e39ea-156">-SizeInBytes</span></span>
<span data-ttu-id="e39ea-157">SizeInBytes-köns storlek i byte</span><span class="sxs-lookup"><span data-stu-id="e39ea-157">SizeInBytes - the size of the queue in bytes</span></span>

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

### <span data-ttu-id="e39ea-158">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e39ea-158">-Confirm</span></span>
<span data-ttu-id="e39ea-159">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e39ea-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e39ea-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e39ea-160">-WhatIf</span></span>
<span data-ttu-id="e39ea-161">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e39ea-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e39ea-162">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e39ea-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e39ea-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e39ea-163">CommonParameters</span></span>
<span data-ttu-id="e39ea-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e39ea-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e39ea-165">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e39ea-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e39ea-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e39ea-166">INPUTS</span></span>

### <span data-ttu-id="e39ea-167">System. String</span><span class="sxs-lookup"><span data-stu-id="e39ea-167">System.String</span></span>

### <span data-ttu-id="e39ea-168">System. Nullable ' 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e39ea-168">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e39ea-169">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e39ea-169">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e39ea-170">System. Nullable ' 1 [[system. Int64, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e39ea-170">System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e39ea-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e39ea-171">OUTPUTS</span></span>

### <span data-ttu-id="e39ea-172">Microsoft. Azure. commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="e39ea-172">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="e39ea-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e39ea-173">NOTES</span></span>

## <span data-ttu-id="e39ea-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e39ea-174">RELATED LINKS</span></span>
