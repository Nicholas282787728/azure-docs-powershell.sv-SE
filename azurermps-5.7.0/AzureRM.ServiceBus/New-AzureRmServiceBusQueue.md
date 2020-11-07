---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 8e1b1cd39e30bcbe2ccc9f46b5ab39511e4de58f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756448"
---
# <span data-ttu-id="e96ea-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="e96ea-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="e96ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e96ea-102">SYNOPSIS</span></span>
<span data-ttu-id="e96ea-103">Skapar en Service Bus-kö i det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="e96ea-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e96ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e96ea-104">SYNTAX</span></span>

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

## <span data-ttu-id="e96ea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e96ea-105">DESCRIPTION</span></span>
<span data-ttu-id="e96ea-106">Cmdleten **New-AzureRmServiceBusQueue** skapar en tjänst buss kö i det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="e96ea-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="e96ea-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e96ea-107">EXAMPLES</span></span>

### <span data-ttu-id="e96ea-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e96ea-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -EnablePartitioning $True

Name                                : SB-Queue_exampl1
LockDuration                        : 
AccessedAt                          : 
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:36 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : 
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 2:51:37 AM
```
<span data-ttu-id="e96ea-109">Skapar en ny Service Bus-kö `SB-Queue_exampl1` i det angivna Service Bus-namnområdet `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="e96ea-109">Creates a new Service Bus queue `SB-Queue_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="e96ea-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e96ea-110">PARAMETERS</span></span>

### <span data-ttu-id="e96ea-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="e96ea-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="e96ea-112">Anger [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) Idle Interval efter vilket kön automatiskt tas bort.</span><span class="sxs-lookup"><span data-stu-id="e96ea-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="e96ea-113">Minsta varaktighet är 5 minuter.</span><span class="sxs-lookup"><span data-stu-id="e96ea-113">The minimum duration is 5 minutes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e96ea-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e96ea-114">-Confirm</span></span>
<span data-ttu-id="e96ea-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e96ea-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e96ea-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="e96ea-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="e96ea-117">Död Brevering för meddelande</span><span class="sxs-lookup"><span data-stu-id="e96ea-117">Dead Lettering On Message Expiration</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e96ea-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="e96ea-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="e96ea-119">TimeSpan to Live-värde.</span><span class="sxs-lookup"><span data-stu-id="e96ea-119">Timespan to live value.</span></span>
<span data-ttu-id="e96ea-120">Det här är den tid som meddelandet upphör att gälla, från och med när meddelandet skickas till Service Bus.</span><span class="sxs-lookup"><span data-stu-id="e96ea-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="e96ea-121">Det här är standardvärdet som används när TimeToLive inte är inställt på ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="e96ea-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="e96ea-122">Standard = TimeSpan. max och Basic = 14 dyas</span><span class="sxs-lookup"><span data-stu-id="e96ea-122">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e96ea-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e96ea-123">-DefaultProfile</span></span>
<span data-ttu-id="e96ea-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e96ea-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e96ea-125">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="e96ea-125">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="e96ea-126">Visar fönstret historik tid för dubblettidentifiering, ett [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) -valuethat definierar varaktigheten för historiken för dubblettidentifiering.</span><span class="sxs-lookup"><span data-stu-id="e96ea-126">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="e96ea-127">Standardvärdet är 10 minuter.</span><span class="sxs-lookup"><span data-stu-id="e96ea-127">The default value is 10 minutes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e96ea-128">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="e96ea-128">-EnableBatchedOperations</span></span>
<span data-ttu-id="e96ea-129">Aktivera grupp operationer-värde som anger om grupp operationer på Server sidan är aktiverade</span><span class="sxs-lookup"><span data-stu-id="e96ea-129">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="e96ea-130">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="e96ea-130">-EnableExpress</span></span>
<span data-ttu-id="e96ea-131">EnableExpress – ett värde som anger om Express-enheter är aktiverade.</span><span class="sxs-lookup"><span data-stu-id="e96ea-131">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="e96ea-132">En Express-kö innehåller ett meddelande i minnet tillfälligt innan det skrivs till beständig lagring.</span><span class="sxs-lookup"><span data-stu-id="e96ea-132">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e96ea-133">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="e96ea-133">-EnablePartitioning</span></span>
<span data-ttu-id="e96ea-134">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="e96ea-134">EnablePartitioning</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e96ea-135">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="e96ea-135">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="e96ea-136">Namn på kö för att vidarekoppla meddelandet om obeställbara meddelanden</span><span class="sxs-lookup"><span data-stu-id="e96ea-136">Queue/Topic name to forward the Dead Letter message</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e96ea-137">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="e96ea-137">-ForwardTo</span></span>
<span data-ttu-id="e96ea-138">Namn på kö/ämne för att vidarekoppla meddelanden</span><span class="sxs-lookup"><span data-stu-id="e96ea-138">Queue/Topic name to forward the messages</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e96ea-139">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="e96ea-139">-LockDuration</span></span>
<span data-ttu-id="e96ea-140">Lås varaktighet</span><span class="sxs-lookup"><span data-stu-id="e96ea-140">Lock Duration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e96ea-141">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="e96ea-141">-MaxDeliveryCount</span></span>
<span data-ttu-id="e96ea-142">MaxDeliveryCount-högsta antal leveranser.</span><span class="sxs-lookup"><span data-stu-id="e96ea-142">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="e96ea-143">Ett meddelande deadlettered automatiskt efter detta antal leveranser.</span><span class="sxs-lookup"><span data-stu-id="e96ea-143">A message is automatically deadlettered after this number of deliveries.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e96ea-144">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="e96ea-144">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="e96ea-145">MaxSizeInMegabytes-köns maximala storlek i MB, vilket är storleken på det allokerade minnet för kön.</span><span class="sxs-lookup"><span data-stu-id="e96ea-145">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e96ea-146">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="e96ea-146">-MessageCount</span></span>
<span data-ttu-id="e96ea-147">MessageCount-antalet meddelanden i kön</span><span class="sxs-lookup"><span data-stu-id="e96ea-147">MessageCount - the number of messages in the queue</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e96ea-148">-Namn</span><span class="sxs-lookup"><span data-stu-id="e96ea-148">-Name</span></span>
<span data-ttu-id="e96ea-149">Könamn</span><span class="sxs-lookup"><span data-stu-id="e96ea-149">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e96ea-150">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="e96ea-150">-Namespace</span></span>
<span data-ttu-id="e96ea-151">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="e96ea-151">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e96ea-152">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="e96ea-152">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="e96ea-153">RequiresDuplicateDetection – ett värde som anger om kön stöder konceptet session</span><span class="sxs-lookup"><span data-stu-id="e96ea-153">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e96ea-154">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="e96ea-154">-RequiresSession</span></span>
<span data-ttu-id="e96ea-155">RequiresSession-det värde som anger om denna kö kräver dubblettidentifiering</span><span class="sxs-lookup"><span data-stu-id="e96ea-155">RequiresSession - the value indicating if this queue requires duplicate detection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e96ea-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e96ea-156">-ResourceGroupName</span></span>
<span data-ttu-id="e96ea-157">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="e96ea-157">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e96ea-158">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="e96ea-158">-SizeInBytes</span></span>
<span data-ttu-id="e96ea-159">SizeInBytes-köns storlek i byte</span><span class="sxs-lookup"><span data-stu-id="e96ea-159">SizeInBytes - the size of the queue in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e96ea-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e96ea-160">-WhatIf</span></span>
<span data-ttu-id="e96ea-161">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e96ea-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e96ea-162">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e96ea-162">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e96ea-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e96ea-163">CommonParameters</span></span>
<span data-ttu-id="e96ea-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e96ea-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e96ea-165">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e96ea-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e96ea-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e96ea-166">INPUTS</span></span>

### <span data-ttu-id="e96ea-167">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e96ea-167">-ResourceGroup</span></span>
 <span data-ttu-id="e96ea-168">System. String</span><span class="sxs-lookup"><span data-stu-id="e96ea-168">System.String</span></span>

### <span data-ttu-id="e96ea-169">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="e96ea-169">-NamespaceName</span></span>
 <span data-ttu-id="e96ea-170">System. String</span><span class="sxs-lookup"><span data-stu-id="e96ea-170">System.String</span></span>

### <span data-ttu-id="e96ea-171">-QueueName</span><span class="sxs-lookup"><span data-stu-id="e96ea-171">-QueueName</span></span>
 <span data-ttu-id="e96ea-172">System. String</span><span class="sxs-lookup"><span data-stu-id="e96ea-172">System.String</span></span>

### <span data-ttu-id="e96ea-173">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="e96ea-173">-EnablePartitioning</span></span>
 <span data-ttu-id="e96ea-174">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="e96ea-174">System.Boolean?</span></span>


## <span data-ttu-id="e96ea-175">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e96ea-175">OUTPUTS</span></span>

### <span data-ttu-id="e96ea-176">Microsoft. Azure. commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="e96ea-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>


## <span data-ttu-id="e96ea-177">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e96ea-177">NOTES</span></span>

## <span data-ttu-id="e96ea-178">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e96ea-178">RELATED LINKS</span></span>
