---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
ms.openlocfilehash: a79afdbba1293c3340e499387b5df745d8b76228
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756068"
---
# <span data-ttu-id="1a1ad-101">New-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="1a1ad-101">New-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="1a1ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1a1ad-102">SYNOPSIS</span></span>
<span data-ttu-id="1a1ad-103">Skapar ett nytt tjänst Bus-avsnitt i det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="1a1ad-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a1ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1a1ad-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>]
 [-SupportOrdering <Boolean>] [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a1ad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1a1ad-105">DESCRIPTION</span></span>
<span data-ttu-id="1a1ad-106">Cmdleten **New-AzureRmServiceBusTopic** skapar ett nytt tjänst Bus-avsnitt i det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="1a1ad-106">The **New-AzureRmServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="1a1ad-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1a1ad-107">EXAMPLES</span></span>

### <span data-ttu-id="1a1ad-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1a1ad-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True

Name                                : SB-Topic_exampl1
Id                                  : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S
                                      B-Topic_exampl1
Type                                : Microsoft.ServiceBus/Topic
AccessedAt                          : 
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 3:16:42 AM
CountDetails                        : 
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 16384
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 
SupportOrdering                     : False
UpdatedAt                           : 1/20/2017 3:16:43 AM

```
<span data-ttu-id="1a1ad-109">Skapar ett nytt tjänst Bus-avsnitt `SB-Topic_exampl1` i det angivna Service Bus-namnområdet `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="1a1ad-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="1a1ad-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1a1ad-110">PARAMETERS</span></span>

### <span data-ttu-id="1a1ad-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="1a1ad-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="1a1ad-112">Anger [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) Idle Interval efter vilket avsnittet automatiskt tas bort.</span><span class="sxs-lookup"><span data-stu-id="1a1ad-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="1a1ad-113">Minsta varaktighet är 5 minuter.</span><span class="sxs-lookup"><span data-stu-id="1a1ad-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="1a1ad-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="1a1ad-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="1a1ad-115">Anger hur länge meddelandet förfaller, räknat från när meddelandet skickas till Service Bus.</span><span class="sxs-lookup"><span data-stu-id="1a1ad-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

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

### <span data-ttu-id="1a1ad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a1ad-116">-DefaultProfile</span></span>
<span data-ttu-id="1a1ad-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1a1ad-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a1ad-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="1a1ad-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="1a1ad-119">Anger [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) -strukturen som definierar varaktigheten för dubblettidentifiering för dubbletter.</span><span class="sxs-lookup"><span data-stu-id="1a1ad-119">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="1a1ad-120">Standardvärdet är 10 minuter.</span><span class="sxs-lookup"><span data-stu-id="1a1ad-120">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="1a1ad-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="1a1ad-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="1a1ad-122">Anger om grupp operationer på Server sidan är aktiverade.</span><span class="sxs-lookup"><span data-stu-id="1a1ad-122">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="1a1ad-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="1a1ad-123">-EnableExpress</span></span>
<span data-ttu-id="1a1ad-124">Anger om Express-enheter är aktiverade.</span><span class="sxs-lookup"><span data-stu-id="1a1ad-124">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="1a1ad-125">En Express-kö innehåller ett meddelande i minnet tillfälligt innan det skrivs till beständig lagring.</span><span class="sxs-lookup"><span data-stu-id="1a1ad-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="1a1ad-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="1a1ad-126">-EnablePartitioning</span></span>
<span data-ttu-id="1a1ad-127">Anger om ämnet ska aktive ras för att vara partitionerad i flera meddelande hanterare.</span><span class="sxs-lookup"><span data-stu-id="1a1ad-127">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a1ad-128">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="1a1ad-128">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="1a1ad-129">Den maximala storleken på ämnet i MB, vilket är storleken på det allokerade minnet.</span><span class="sxs-lookup"><span data-stu-id="1a1ad-129">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

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

### <span data-ttu-id="1a1ad-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="1a1ad-130">-Name</span></span>
<span data-ttu-id="1a1ad-131">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="1a1ad-131">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a1ad-132">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="1a1ad-132">-Namespace</span></span>
<span data-ttu-id="1a1ad-133">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="1a1ad-133">Namespace Name.</span></span>

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

### <span data-ttu-id="1a1ad-134">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="1a1ad-134">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="1a1ad-135">Anger om det krävs en dubblettidentifiering för avsnittet.</span><span class="sxs-lookup"><span data-stu-id="1a1ad-135">Indicates whether the topic requires duplication detection.</span></span>

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

### <span data-ttu-id="1a1ad-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a1ad-136">-ResourceGroupName</span></span>
<span data-ttu-id="1a1ad-137">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="1a1ad-137">The name of the resource group</span></span>

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

### <span data-ttu-id="1a1ad-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="1a1ad-138">-SizeInBytes</span></span>
<span data-ttu-id="1a1ad-139">Anger storleken på ämnet i byte.</span><span class="sxs-lookup"><span data-stu-id="1a1ad-139">Specifies the size of the topic in bytes.</span></span>

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

### <span data-ttu-id="1a1ad-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="1a1ad-140">-SupportOrdering</span></span>
<span data-ttu-id="1a1ad-141">Anger om avsnittet har stöd för sortering.</span><span class="sxs-lookup"><span data-stu-id="1a1ad-141">Indicates whether the topic supports ordering.</span></span>

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

### <span data-ttu-id="1a1ad-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1a1ad-142">-Confirm</span></span>
<span data-ttu-id="1a1ad-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1a1ad-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a1ad-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a1ad-144">-WhatIf</span></span>
<span data-ttu-id="1a1ad-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1a1ad-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a1ad-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1a1ad-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a1ad-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a1ad-147">CommonParameters</span></span>
<span data-ttu-id="1a1ad-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a1ad-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a1ad-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a1ad-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a1ad-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1a1ad-150">INPUTS</span></span>

### <span data-ttu-id="1a1ad-151">System. String</span><span class="sxs-lookup"><span data-stu-id="1a1ad-151">System.String</span></span>
<span data-ttu-id="1a1ad-152">System. Nullable \` 1 \[ \[ system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = B77a5c561934e089 \] \] system. Nullable \` 1 \[ \[ system. Int64, mscorlib, version = 4.0.0.0, kultur = neutral, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="1a1ad-152">System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

### <span data-ttu-id="1a1ad-153">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1a1ad-153">-ResourceGroup</span></span>
 <span data-ttu-id="1a1ad-154">System. String</span><span class="sxs-lookup"><span data-stu-id="1a1ad-154">System.String</span></span>

### <span data-ttu-id="1a1ad-155">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="1a1ad-155">-NamespaceName</span></span>
 <span data-ttu-id="1a1ad-156">System. String</span><span class="sxs-lookup"><span data-stu-id="1a1ad-156">System.String</span></span>

### <span data-ttu-id="1a1ad-157">-TopicName</span><span class="sxs-lookup"><span data-stu-id="1a1ad-157">-TopicName</span></span>
 <span data-ttu-id="1a1ad-158">System. String</span><span class="sxs-lookup"><span data-stu-id="1a1ad-158">System.String</span></span>

### <span data-ttu-id="1a1ad-159">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="1a1ad-159">-EnablePartitioning</span></span>
 <span data-ttu-id="1a1ad-160">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="1a1ad-160">System.Boolean?</span></span>

## <span data-ttu-id="1a1ad-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1a1ad-161">OUTPUTS</span></span>

### <span data-ttu-id="1a1ad-162">Microsoft. Azure. commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="1a1ad-162">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="1a1ad-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1a1ad-163">NOTES</span></span>

## <span data-ttu-id="1a1ad-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1a1ad-164">RELATED LINKS</span></span>

