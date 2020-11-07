---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 54753001be0a754cf9416e1b2ec53fd81647d8d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756447"
---
# <span data-ttu-id="859b4-101">New-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="859b4-101">New-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="859b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="859b4-102">SYNOPSIS</span></span>
<span data-ttu-id="859b4-103">Skapar ett abonnemang för den angivna tjänst Bus artikeln.</span><span class="sxs-lookup"><span data-stu-id="859b4-103">Creates a subscription to the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="859b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="859b4-104">SYNTAX</span></span>

```
New-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="859b4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="859b4-105">DESCRIPTION</span></span>
<span data-ttu-id="859b4-106">Cmdleten **New-AzureRmServiceBusSubscription** skapar ett nytt abonnemang för den angivna tjänst Bus artikeln.</span><span class="sxs-lookup"><span data-stu-id="859b4-106">The **New-AzureRmServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="859b4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="859b4-107">EXAMPLES</span></span>

### <span data-ttu-id="859b4-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="859b4-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
CreatedAt                                 : 1/20/2017 3:18:52 AM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : False
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 10
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 3:18:54 AM
```
<span data-ttu-id="859b4-109">Skapar abonnemanget `SB-TopicSubscription-Example1` för den angivna tjänst Bus artikeln `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="859b4-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="859b4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="859b4-110">PARAMETERS</span></span>

### <span data-ttu-id="859b4-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="859b4-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="859b4-112">Anger [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) Idle Interval efter vilket prenumerationen automatiskt raderas.</span><span class="sxs-lookup"><span data-stu-id="859b4-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="859b4-113">Minsta varaktighet är 5 minuter.</span><span class="sxs-lookup"><span data-stu-id="859b4-113">The minimum duration is 5 minutes.</span></span>


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

### <span data-ttu-id="859b4-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="859b4-114">-Confirm</span></span>
<span data-ttu-id="859b4-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="859b4-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="859b4-116">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="859b4-116">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="859b4-117">Värde som anger om ett abonnemang har stöd för obeställbara meddelanden om undantag för filter utvärdering.</span><span class="sxs-lookup"><span data-stu-id="859b4-117">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="859b4-118">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="859b4-118">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="859b4-119">Död Brevering för meddelande</span><span class="sxs-lookup"><span data-stu-id="859b4-119">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="859b4-120">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="859b4-120">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="859b4-121">TimeSpan to Live-värde.</span><span class="sxs-lookup"><span data-stu-id="859b4-121">Timespan to live value.</span></span>
<span data-ttu-id="859b4-122">Det här är den tid som meddelandet upphör att gälla, från och med när meddelandet skickas till Service Bus.</span><span class="sxs-lookup"><span data-stu-id="859b4-122">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="859b4-123">Det här är standardvärdet som används när TimeToLive inte är inställt på ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="859b4-123">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="859b4-124">Standard = TimeSpan. max och Basic = 14 dyas</span><span class="sxs-lookup"><span data-stu-id="859b4-124">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="859b4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="859b4-125">-DefaultProfile</span></span>
<span data-ttu-id="859b4-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="859b4-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="859b4-127">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="859b4-127">-EnableBatchedOperations</span></span>
<span data-ttu-id="859b4-128">Aktivera grupp operationer-värde som anger om grupp operationer på Server sidan är aktiverade</span><span class="sxs-lookup"><span data-stu-id="859b4-128">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="859b4-129">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="859b4-129">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="859b4-130">Namn på kö för att vidarekoppla meddelandet om obeställbara meddelanden</span><span class="sxs-lookup"><span data-stu-id="859b4-130">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="859b4-131">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="859b4-131">-ForwardTo</span></span>
<span data-ttu-id="859b4-132">Namn på kö/ämne för att vidarekoppla meddelanden</span><span class="sxs-lookup"><span data-stu-id="859b4-132">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="859b4-133">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="859b4-133">-LockDuration</span></span>
<span data-ttu-id="859b4-134">Lås varaktighet</span><span class="sxs-lookup"><span data-stu-id="859b4-134">Lock Duration</span></span>

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

### <span data-ttu-id="859b4-135">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="859b4-135">-MaxDeliveryCount</span></span>
<span data-ttu-id="859b4-136">MaxDeliveryCount-högsta antal leveranser.</span><span class="sxs-lookup"><span data-stu-id="859b4-136">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="859b4-137">Ett meddelande deadlettered automatiskt efter detta antal leveranser.</span><span class="sxs-lookup"><span data-stu-id="859b4-137">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="859b4-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="859b4-138">-Name</span></span>
<span data-ttu-id="859b4-139">Prenumerationens namn</span><span class="sxs-lookup"><span data-stu-id="859b4-139">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859b4-140">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="859b4-140">-Namespace</span></span>
<span data-ttu-id="859b4-141">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="859b4-141">Namespace Name</span></span>

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

### <span data-ttu-id="859b4-142">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="859b4-142">-RequiresSession</span></span>
<span data-ttu-id="859b4-143">RequiresSession-det värde som anger om den här kön kräver dubblettidentifiering.</span><span class="sxs-lookup"><span data-stu-id="859b4-143">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="859b4-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="859b4-144">-ResourceGroupName</span></span>
<span data-ttu-id="859b4-145">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="859b4-145">The name of the resource group</span></span>

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

### <span data-ttu-id="859b4-146">-Ämne</span><span class="sxs-lookup"><span data-stu-id="859b4-146">-Topic</span></span>
<span data-ttu-id="859b4-147">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="859b4-147">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859b4-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="859b4-148">-WhatIf</span></span>
<span data-ttu-id="859b4-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="859b4-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="859b4-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="859b4-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="859b4-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="859b4-151">CommonParameters</span></span>
<span data-ttu-id="859b4-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="859b4-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="859b4-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="859b4-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="859b4-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="859b4-154">INPUTS</span></span>

### <span data-ttu-id="859b4-155">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="859b4-155">-ResourceGroup</span></span>
 <span data-ttu-id="859b4-156">System. String</span><span class="sxs-lookup"><span data-stu-id="859b4-156">System.String</span></span>
 

### <span data-ttu-id="859b4-157">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="859b4-157">-NamespaceName</span></span>
 <span data-ttu-id="859b4-158">System. String</span><span class="sxs-lookup"><span data-stu-id="859b4-158">System.String</span></span>
 

### <span data-ttu-id="859b4-159">-TopicName</span><span class="sxs-lookup"><span data-stu-id="859b4-159">-TopicName</span></span>
 <span data-ttu-id="859b4-160">System. String</span><span class="sxs-lookup"><span data-stu-id="859b4-160">System.String</span></span>
 

### <span data-ttu-id="859b4-161">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="859b4-161">-SubscriptionName</span></span>
 <span data-ttu-id="859b4-162">System. String</span><span class="sxs-lookup"><span data-stu-id="859b4-162">System.String</span></span>


## <span data-ttu-id="859b4-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="859b4-163">OUTPUTS</span></span>

### <span data-ttu-id="859b4-164">Microsoft. Azure. commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="859b4-164">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>


## <span data-ttu-id="859b4-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="859b4-165">NOTES</span></span>

## <span data-ttu-id="859b4-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="859b4-166">RELATED LINKS</span></span>
