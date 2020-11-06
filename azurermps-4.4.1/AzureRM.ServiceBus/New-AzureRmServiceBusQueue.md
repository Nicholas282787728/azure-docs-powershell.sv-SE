---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 4538bb39c085a2e7152a146d5e93e08a0c09f5de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574520"
---
# <span data-ttu-id="d69d0-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="d69d0-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="d69d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d69d0-102">SYNOPSIS</span></span>
<span data-ttu-id="d69d0-103">Skapar en Service Bus-kö i det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="d69d0-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d69d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d69d0-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> -Name <String>
 -EnablePartitioning <Boolean> [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-EnableBatchedOperations <Boolean>] [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableExpress <Boolean>]
 [-IsAnonymousAccessible <Boolean>] [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>]
 [-MessageCount <Int64>] [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>]
 [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d69d0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d69d0-105">DESCRIPTION</span></span>
<span data-ttu-id="d69d0-106">Cmdleten **New-AzureRmServiceBusQueue** skapar en tjänst buss kö i det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="d69d0-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="d69d0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d69d0-107">EXAMPLES</span></span>

### <span data-ttu-id="d69d0-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d69d0-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -EnablePartitioning $True
```

<span data-ttu-id="d69d0-109">Skapar en ny Service Bus-kö `SB-Queue_exampl1` i det angivna Service Bus-namnområdet `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="d69d0-109">Creates a new Service Bus queue `SB-Queue_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="d69d0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d69d0-110">PARAMETERS</span></span>

### <span data-ttu-id="d69d0-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="d69d0-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="d69d0-112">Anger [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) Idle Interval efter vilket kön automatiskt tas bort.</span><span class="sxs-lookup"><span data-stu-id="d69d0-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="d69d0-113">Minsta varaktighet är 5 minuter.</span><span class="sxs-lookup"><span data-stu-id="d69d0-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="d69d0-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="d69d0-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="d69d0-115">Anger om meddelanden är deadlettered vid utgångs datum.</span><span class="sxs-lookup"><span data-stu-id="d69d0-115">Specifies whether messages are deadlettered on expiration.</span></span>

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

### <span data-ttu-id="d69d0-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="d69d0-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="d69d0-117">Anger standardvärdet för TTL (Time to Live) för meddelanden.</span><span class="sxs-lookup"><span data-stu-id="d69d0-117">Specifies the default message time-to-live (TTL).</span></span>

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

### <span data-ttu-id="d69d0-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="d69d0-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="d69d0-119">Visar fönstret historik tid för dubblettidentifiering, ett [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) -valuethat definierar varaktigheten för historiken för dubblettidentifiering.</span><span class="sxs-lookup"><span data-stu-id="d69d0-119">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="d69d0-120">Standardvärdet är 10 minuter.</span><span class="sxs-lookup"><span data-stu-id="d69d0-120">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="d69d0-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="d69d0-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="d69d0-122">Anger om grupp operationer på Server sidan är aktiverade.</span><span class="sxs-lookup"><span data-stu-id="d69d0-122">Specifies whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="d69d0-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="d69d0-123">-EnableExpress</span></span>
<span data-ttu-id="d69d0-124">Anger om Express-enheter är aktiverade.</span><span class="sxs-lookup"><span data-stu-id="d69d0-124">Specifies whether Express Entities are enabled.</span></span> <span data-ttu-id="d69d0-125">En Express-kö innehåller ett meddelande i minnet tillfälligt innan det skrivs till beständig lagring.</span><span class="sxs-lookup"><span data-stu-id="d69d0-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="d69d0-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="d69d0-126">-EnablePartitioning</span></span>
<span data-ttu-id="d69d0-127">Anger om EnablePartitioning är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="d69d0-127">Specifies whether EnablePartitioning is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d69d0-128">-IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="d69d0-128">-IsAnonymousAccessible</span></span>
<span data-ttu-id="d69d0-129">Anger om meddelandet är anonymt tillgängligt.</span><span class="sxs-lookup"><span data-stu-id="d69d0-129">Specifies whether the message is anonymously accessible.</span></span>

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

### <span data-ttu-id="d69d0-130">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="d69d0-130">-LockDuration</span></span>
<span data-ttu-id="d69d0-131">Anger lås varaktigheten.</span><span class="sxs-lookup"><span data-stu-id="d69d0-131">Specifies the lock duration.</span></span>

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

### <span data-ttu-id="d69d0-132">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="d69d0-132">-MaxDeliveryCount</span></span>
<span data-ttu-id="d69d0-133">Anger maximalt antal leveranser.</span><span class="sxs-lookup"><span data-stu-id="d69d0-133">Specifies the maximum delivery count.</span></span> <span data-ttu-id="d69d0-134">Ett meddelande deadlettered automatiskt efter detta antal leveranser.</span><span class="sxs-lookup"><span data-stu-id="d69d0-134">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="d69d0-135">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="d69d0-135">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="d69d0-136">Anger den maximala storleken på kön i MB, vilket är storleken på det allokerade minnet för kön.</span><span class="sxs-lookup"><span data-stu-id="d69d0-136">Specifies the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

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

### <span data-ttu-id="d69d0-137">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="d69d0-137">-MessageCount</span></span>
<span data-ttu-id="d69d0-138">Anger antalet meddelanden i kön.</span><span class="sxs-lookup"><span data-stu-id="d69d0-138">Specifies the number of messages in the queue.</span></span>

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

### <span data-ttu-id="d69d0-139">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="d69d0-139">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="d69d0-140">Anger om kön kräver dubblettidentifiering.</span><span class="sxs-lookup"><span data-stu-id="d69d0-140">Specifies whether the queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="d69d0-141">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="d69d0-141">-RequiresSession</span></span>
<span data-ttu-id="d69d0-142">Anger om kön har stöd för sessioner.</span><span class="sxs-lookup"><span data-stu-id="d69d0-142">Specifies whether this queue supports sessions.</span></span>

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

### <span data-ttu-id="d69d0-143">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="d69d0-143">-SizeInBytes</span></span>
<span data-ttu-id="d69d0-144">Storleken på kön i byte.</span><span class="sxs-lookup"><span data-stu-id="d69d0-144">The size of the queue in bytes.</span></span>

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

### <span data-ttu-id="d69d0-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d69d0-145">-Confirm</span></span>
<span data-ttu-id="d69d0-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d69d0-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d69d0-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d69d0-147">-WhatIf</span></span>
<span data-ttu-id="d69d0-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d69d0-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d69d0-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d69d0-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d69d0-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d69d0-150">-DefaultProfile</span></span>
<span data-ttu-id="d69d0-151">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d69d0-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d69d0-152">-Namn</span><span class="sxs-lookup"><span data-stu-id="d69d0-152">-Name</span></span>
<span data-ttu-id="d69d0-153">Könamn.</span><span class="sxs-lookup"><span data-stu-id="d69d0-153">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d69d0-154">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="d69d0-154">-Namespace</span></span>
<span data-ttu-id="d69d0-155">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="d69d0-155">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d69d0-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d69d0-156">-ResourceGroupName</span></span>
<span data-ttu-id="d69d0-157">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="d69d0-157">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d69d0-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d69d0-158">CommonParameters</span></span>
<span data-ttu-id="d69d0-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d69d0-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d69d0-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d69d0-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d69d0-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d69d0-161">INPUTS</span></span>

### <span data-ttu-id="d69d0-162">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d69d0-162">-ResourceGroup</span></span>
 <span data-ttu-id="d69d0-163">System. String</span><span class="sxs-lookup"><span data-stu-id="d69d0-163">System.String</span></span>

### <span data-ttu-id="d69d0-164">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="d69d0-164">-NamespaceName</span></span>
 <span data-ttu-id="d69d0-165">System. String</span><span class="sxs-lookup"><span data-stu-id="d69d0-165">System.String</span></span>

### <span data-ttu-id="d69d0-166">-QueueName</span><span class="sxs-lookup"><span data-stu-id="d69d0-166">-QueueName</span></span>
 <span data-ttu-id="d69d0-167">System. String</span><span class="sxs-lookup"><span data-stu-id="d69d0-167">System.String</span></span>

### <span data-ttu-id="d69d0-168">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="d69d0-168">-EnablePartitioning</span></span>
 <span data-ttu-id="d69d0-169">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="d69d0-169">System.Boolean?</span></span>

## <span data-ttu-id="d69d0-170">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d69d0-170">OUTPUTS</span></span>

### <span data-ttu-id="d69d0-171">Microsoft. Azure. commands. ServiceBus. Models. QueueAttributes</span><span class="sxs-lookup"><span data-stu-id="d69d0-171">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>
<span data-ttu-id="d69d0-172">Namn: SB-Queue_exampl1 plats: West US LockDuration: AccessedAt: AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 2:51:36 AM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true DeadLetteringOnMessageExpiration: falskt EnableExpress: falskt EnablePartitioning: true IsAnonymousAccessible: false MaxDeliveryCount: MaxSizeInMegabytes: 16384 MessageCount: CountDetails: RequiresDuplicateDetection: false RequiresSession: falskt SizeInBytes: status: Active SupportOrdering: false UpdatedAt: 1/20/2017 2:51:37 AM</span><span class="sxs-lookup"><span data-stu-id="d69d0-172">Name                                : SB-Queue_exampl1 Location                            : West US LockDuration                        : AccessedAt                          : AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 2:51:36 AM DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True DeadLetteringOnMessageExpiration    : False EnableExpress                       : False EnablePartitioning                  : True IsAnonymousAccessible               : False MaxDeliveryCount                    : MaxSizeInMegabytes                  : 16384 MessageCount                        : CountDetails                        : RequiresDuplicateDetection          : False RequiresSession                     : False SizeInBytes                         : Status                              : Active SupportOrdering                     : False UpdatedAt                           : 1/20/2017 2:51:37 AM</span></span>

## <span data-ttu-id="d69d0-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d69d0-173">NOTES</span></span>

## <span data-ttu-id="d69d0-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d69d0-174">RELATED LINKS</span></span>

