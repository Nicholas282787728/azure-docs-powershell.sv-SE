---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
ms.openlocfilehash: e2ca0b6902ecc13c9dfe4f418ea5d321b6e36dbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576075"
---
# <span data-ttu-id="38d60-101">New-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="38d60-101">New-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="38d60-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="38d60-102">SYNOPSIS</span></span>
<span data-ttu-id="38d60-103">Skapar ett nytt tjänst Bus-avsnitt i det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="38d60-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38d60-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="38d60-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>]
 [-SupportOrdering <Boolean>] [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38d60-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="38d60-105">DESCRIPTION</span></span>
<span data-ttu-id="38d60-106">Cmdleten **New-AzureRmServiceBusTopic** skapar ett nytt tjänst Bus-avsnitt i det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="38d60-106">The **New-AzureRmServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="38d60-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="38d60-107">EXAMPLES</span></span>

### <span data-ttu-id="38d60-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="38d60-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 11:51:24 PM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : True
UpdatedAt                           : 10/11/2018 11:51:24 PM
```

<span data-ttu-id="38d60-109">Skapar ett nytt tjänst Bus-avsnitt `SB-Topic_exampl1` i det angivna Service Bus-namnområdet `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="38d60-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="38d60-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="38d60-110">PARAMETERS</span></span>

### <span data-ttu-id="38d60-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="38d60-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="38d60-112">Anger [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) Idle Interval efter vilket avsnittet automatiskt tas bort.</span><span class="sxs-lookup"><span data-stu-id="38d60-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="38d60-113">Minsta varaktighet är 5 minuter.</span><span class="sxs-lookup"><span data-stu-id="38d60-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="38d60-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="38d60-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="38d60-115">Anger hur länge meddelandet förfaller, räknat från när meddelandet skickas till Service Bus.</span><span class="sxs-lookup"><span data-stu-id="38d60-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

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

### <span data-ttu-id="38d60-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d60-116">-DefaultProfile</span></span>
<span data-ttu-id="38d60-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="38d60-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38d60-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="38d60-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="38d60-119">Anger [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) -strukturen som definierar varaktigheten för dubblettidentifiering för dubbletter.</span><span class="sxs-lookup"><span data-stu-id="38d60-119">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="38d60-120">Standardvärdet är 10 minuter.</span><span class="sxs-lookup"><span data-stu-id="38d60-120">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="38d60-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="38d60-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="38d60-122">Anger om grupp operationer på Server sidan är aktiverade.</span><span class="sxs-lookup"><span data-stu-id="38d60-122">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="38d60-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="38d60-123">-EnableExpress</span></span>
<span data-ttu-id="38d60-124">Anger om Express-enheter är aktiverade.</span><span class="sxs-lookup"><span data-stu-id="38d60-124">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="38d60-125">En Express-kö innehåller ett meddelande i minnet tillfälligt innan det skrivs till beständig lagring.</span><span class="sxs-lookup"><span data-stu-id="38d60-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="38d60-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="38d60-126">-EnablePartitioning</span></span>
<span data-ttu-id="38d60-127">Anger om ämnet ska aktive ras för att vara partitionerad i flera meddelande hanterare.</span><span class="sxs-lookup"><span data-stu-id="38d60-127">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

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

### <span data-ttu-id="38d60-128">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="38d60-128">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="38d60-129">Den maximala storleken på ämnet i MB, vilket är storleken på det allokerade minnet.</span><span class="sxs-lookup"><span data-stu-id="38d60-129">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

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

### <span data-ttu-id="38d60-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="38d60-130">-Name</span></span>
<span data-ttu-id="38d60-131">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="38d60-131">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38d60-132">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="38d60-132">-Namespace</span></span>
<span data-ttu-id="38d60-133">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="38d60-133">Namespace Name.</span></span>

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

### <span data-ttu-id="38d60-134">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="38d60-134">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="38d60-135">Anger om det krävs en dubblettidentifiering för avsnittet.</span><span class="sxs-lookup"><span data-stu-id="38d60-135">Indicates whether the topic requires duplication detection.</span></span>

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

### <span data-ttu-id="38d60-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38d60-136">-ResourceGroupName</span></span>
<span data-ttu-id="38d60-137">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="38d60-137">The name of the resource group</span></span>

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

### <span data-ttu-id="38d60-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="38d60-138">-SizeInBytes</span></span>
<span data-ttu-id="38d60-139">Anger storleken på ämnet i byte.</span><span class="sxs-lookup"><span data-stu-id="38d60-139">Specifies the size of the topic in bytes.</span></span>

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

### <span data-ttu-id="38d60-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="38d60-140">-SupportOrdering</span></span>
<span data-ttu-id="38d60-141">Anger om avsnittet har stöd för sortering.</span><span class="sxs-lookup"><span data-stu-id="38d60-141">Indicates whether the topic supports ordering.</span></span>

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

### <span data-ttu-id="38d60-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="38d60-142">-Confirm</span></span>
<span data-ttu-id="38d60-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="38d60-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38d60-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38d60-144">-WhatIf</span></span>
<span data-ttu-id="38d60-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="38d60-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38d60-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="38d60-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38d60-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d60-147">CommonParameters</span></span>
<span data-ttu-id="38d60-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38d60-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d60-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38d60-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d60-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="38d60-150">INPUTS</span></span>

### <span data-ttu-id="38d60-151">System. String</span><span class="sxs-lookup"><span data-stu-id="38d60-151">System.String</span></span>

### <span data-ttu-id="38d60-152">System. Nullable ' 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="38d60-152">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="38d60-153">System. Nullable ' 1 [[system. Int64, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="38d60-153">System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="38d60-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="38d60-154">OUTPUTS</span></span>

### <span data-ttu-id="38d60-155">Microsoft. Azure. commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="38d60-155">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="38d60-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="38d60-156">NOTES</span></span>

## <span data-ttu-id="38d60-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="38d60-157">RELATED LINKS</span></span>
