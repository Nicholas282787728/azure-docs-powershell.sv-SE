---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
ms.openlocfilehash: 099088bb560606990baa4f1774d8f46c5f68f04b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575853"
---
# <span data-ttu-id="e5688-101">New-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="e5688-101">New-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="e5688-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5688-102">SYNOPSIS</span></span>
<span data-ttu-id="e5688-103">Skapar ett nytt tjänst Bus-avsnitt i det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="e5688-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5688-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5688-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> -Name <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-EnableSubscriptionPartitioning <Boolean>]
 [-FilteringMessagesBeforePublishing <Boolean>] [-IsAnonymousAccessible <Boolean>] [-IsExpress <Boolean>]
 [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>] [-SupportOrdering <Boolean>]
 [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5688-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5688-105">DESCRIPTION</span></span>
<span data-ttu-id="e5688-106">Cmdleten **New-AzureRmServiceBusTopic** skapar ett nytt tjänst Bus-avsnitt i det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="e5688-106">The **New-AzureRmServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="e5688-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5688-107">EXAMPLES</span></span>

### <span data-ttu-id="e5688-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e5688-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True
```

<span data-ttu-id="e5688-109">Skapar ett nytt tjänst Bus-avsnitt `SB-Topic_exampl1` i det angivna Service Bus-namnområdet `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="e5688-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="e5688-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5688-110">PARAMETERS</span></span>

### <span data-ttu-id="e5688-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="e5688-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="e5688-112">Anger [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) Idle Interval efter vilket avsnittet automatiskt tas bort.</span><span class="sxs-lookup"><span data-stu-id="e5688-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="e5688-113">Minsta varaktighet är 5 minuter.</span><span class="sxs-lookup"><span data-stu-id="e5688-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="e5688-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="e5688-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="e5688-115">Anger hur länge meddelandet förfaller, räknat från när meddelandet skickas till Service Bus.</span><span class="sxs-lookup"><span data-stu-id="e5688-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

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

### <span data-ttu-id="e5688-116">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="e5688-116">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="e5688-117">Anger [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) -strukturen som definierar varaktigheten för dubblettidentifiering för dubbletter.</span><span class="sxs-lookup"><span data-stu-id="e5688-117">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="e5688-118">Standardvärdet är 10 minuter.</span><span class="sxs-lookup"><span data-stu-id="e5688-118">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="e5688-119">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="e5688-119">-EnableBatchedOperations</span></span>
<span data-ttu-id="e5688-120">Anger om grupp operationer på Server sidan är aktiverade.</span><span class="sxs-lookup"><span data-stu-id="e5688-120">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="e5688-121">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="e5688-121">-EnableExpress</span></span>
<span data-ttu-id="e5688-122">Anger om Express-enheter är aktiverade.</span><span class="sxs-lookup"><span data-stu-id="e5688-122">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="e5688-123">En Express-kö innehåller ett meddelande i minnet tillfälligt innan det skrivs till beständig lagring.</span><span class="sxs-lookup"><span data-stu-id="e5688-123">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="e5688-124">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="e5688-124">-EnablePartitioning</span></span>
<span data-ttu-id="e5688-125">Anger om ämnet ska aktive ras för att vara partitionerad i flera meddelande hanterare.</span><span class="sxs-lookup"><span data-stu-id="e5688-125">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

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

### <span data-ttu-id="e5688-126">-EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="e5688-126">-EnableSubscriptionPartitioning</span></span>
<span data-ttu-id="e5688-127">Anger om du vill aktivera abonnemangs partitionerings.</span><span class="sxs-lookup"><span data-stu-id="e5688-127">Specifies whether to enable subscription partitioning.</span></span>

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

### <span data-ttu-id="e5688-128">-FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="e5688-128">-FilteringMessagesBeforePublishing</span></span>
<span data-ttu-id="e5688-129">Anger om filtrering är aktiverat för meddelanden före publicering.</span><span class="sxs-lookup"><span data-stu-id="e5688-129">Indicates whether filtering is enabled for messages before publishing.</span></span>

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

### <span data-ttu-id="e5688-130">-IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="e5688-130">-IsAnonymousAccessible</span></span>
<span data-ttu-id="e5688-131">Anger om meddelandet tillåter anonym åtkomst.</span><span class="sxs-lookup"><span data-stu-id="e5688-131">Indicates whether the message allows anonymous access.</span></span>

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

### <span data-ttu-id="e5688-132">-IsExpress</span><span class="sxs-lookup"><span data-stu-id="e5688-132">-IsExpress</span></span>
<span data-ttu-id="e5688-133">Anger om avsnittet är Express aktiverat.</span><span class="sxs-lookup"><span data-stu-id="e5688-133">Indicates whether the topic is express enabled.</span></span>

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

### <span data-ttu-id="e5688-134">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="e5688-134">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="e5688-135">Den maximala storleken på ämnet i MB, vilket är storleken på det allokerade minnet.</span><span class="sxs-lookup"><span data-stu-id="e5688-135">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

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

### <span data-ttu-id="e5688-136">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="e5688-136">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="e5688-137">Anger om det krävs en dubblettidentifiering för avsnittet.</span><span class="sxs-lookup"><span data-stu-id="e5688-137">Indicates whether the topic requires duplication detection.</span></span>

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

### <span data-ttu-id="e5688-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="e5688-138">-SizeInBytes</span></span>
<span data-ttu-id="e5688-139">Anger storleken på ämnet i byte.</span><span class="sxs-lookup"><span data-stu-id="e5688-139">Specifies the size of the topic in bytes.</span></span>

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

### <span data-ttu-id="e5688-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="e5688-140">-SupportOrdering</span></span>
<span data-ttu-id="e5688-141">Anger om avsnittet har stöd för sortering.</span><span class="sxs-lookup"><span data-stu-id="e5688-141">Indicates whether the topic supports ordering.</span></span>

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

### <span data-ttu-id="e5688-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e5688-142">-Confirm</span></span>
<span data-ttu-id="e5688-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e5688-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5688-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5688-144">-WhatIf</span></span>
<span data-ttu-id="e5688-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e5688-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5688-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e5688-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5688-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5688-147">-DefaultProfile</span></span>
<span data-ttu-id="e5688-148">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e5688-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5688-149">-Namn</span><span class="sxs-lookup"><span data-stu-id="e5688-149">-Name</span></span>
<span data-ttu-id="e5688-150">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="e5688-150">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5688-151">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="e5688-151">-Namespace</span></span>
<span data-ttu-id="e5688-152">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="e5688-152">Namespace Name.</span></span>

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

### <span data-ttu-id="e5688-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5688-153">-ResourceGroupName</span></span>
<span data-ttu-id="e5688-154">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="e5688-154">The name of the resource group</span></span>

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

### <span data-ttu-id="e5688-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5688-155">CommonParameters</span></span>
<span data-ttu-id="e5688-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5688-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5688-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5688-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5688-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5688-158">INPUTS</span></span>

### <span data-ttu-id="e5688-159">System. String</span><span class="sxs-lookup"><span data-stu-id="e5688-159">System.String</span></span>
<span data-ttu-id="e5688-160">System. Nullable \` 1 \[ \[ system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = B77a5c561934e089 \] \] system. Nullable \` 1 \[ \[ system. Int64, mscorlib, version = 4.0.0.0, kultur = neutral, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="e5688-160">System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

### <span data-ttu-id="e5688-161">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e5688-161">-ResourceGroup</span></span>
 <span data-ttu-id="e5688-162">System. String</span><span class="sxs-lookup"><span data-stu-id="e5688-162">System.String</span></span>

### <span data-ttu-id="e5688-163">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="e5688-163">-NamespaceName</span></span>
 <span data-ttu-id="e5688-164">System. String</span><span class="sxs-lookup"><span data-stu-id="e5688-164">System.String</span></span>

### <span data-ttu-id="e5688-165">-TopicName</span><span class="sxs-lookup"><span data-stu-id="e5688-165">-TopicName</span></span>
 <span data-ttu-id="e5688-166">System. String</span><span class="sxs-lookup"><span data-stu-id="e5688-166">System.String</span></span>

### <span data-ttu-id="e5688-167">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="e5688-167">-EnablePartitioning</span></span>
 <span data-ttu-id="e5688-168">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="e5688-168">System.Boolean?</span></span>

## <span data-ttu-id="e5688-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5688-169">OUTPUTS</span></span>

### <span data-ttu-id="e5688-170">Microsoft. Azure. commands. ServiceBus. Models. TopicAttributes</span><span class="sxs-lookup"><span data-stu-id="e5688-170">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>
<span data-ttu-id="e5688-171">Namn: SB-Topic_exampl1 plats: West US ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1: Microsoft. ServiceBus/topic AccessedAt: AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 3:16:42 ' AM CountDetails: DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true EnableExpress: falskt EnablePartitioning: true EnableSubscriptionPartitioning: falskt FilteringMessagesBeforePublishing: falskt IsAnonymousAccessible: falskt IsExpress: falskt MaxSizeInMegabytes: 16384 RequiresDuplicateDetection: false SizeInBytes: 0 status: Active SubscriptionCount: SupportOrdering: false UpdatedAt: 1/20/2017 3:16:43 AM</span><span class="sxs-lookup"><span data-stu-id="e5688-171">Name                                : SB-Topic_exampl1 Location                            : West US Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 Type                                : Microsoft.ServiceBus/Topic AccessedAt                          : AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 3:16:42 AM CountDetails                        : DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True EnableExpress                       : False EnablePartitioning                  : True EnableSubscriptionPartitioning      : False FilteringMessagesBeforePublishing   : False IsAnonymousAccessible               : False IsExpress                           : False MaxSizeInMegabytes                  : 16384 RequiresDuplicateDetection          : False SizeInBytes                         : 0 Status                              : Active SubscriptionCount                   : SupportOrdering                     : False UpdatedAt                           : 1/20/2017 3:16:43 AM</span></span>

## <span data-ttu-id="e5688-172">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5688-172">NOTES</span></span>

## <span data-ttu-id="e5688-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5688-173">RELATED LINKS</span></span>

