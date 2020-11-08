---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
ms.openlocfilehash: 2ed5d3345730e631b3f7668ca4b05f3decc04f06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919966"
---
# <span data-ttu-id="e45c4-101">New-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="e45c4-101">New-AzServiceBusSubscription</span></span>

## <span data-ttu-id="e45c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e45c4-102">SYNOPSIS</span></span>
<span data-ttu-id="e45c4-103">Skapar ett abonnemang för den angivna tjänst Bus artikeln.</span><span class="sxs-lookup"><span data-stu-id="e45c4-103">Creates a subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="e45c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e45c4-104">SYNTAX</span></span>

```
New-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e45c4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e45c4-105">DESCRIPTION</span></span>
<span data-ttu-id="e45c4-106">Cmdleten **New-AzServiceBusSubscription** skapar ett nytt abonnemang för den angivna tjänst Bus artikeln.</span><span class="sxs-lookup"><span data-stu-id="e45c4-106">The **New-AzServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="e45c4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e45c4-107">EXAMPLES</span></span>

### <span data-ttu-id="e45c4-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e45c4-108">Example 1</span></span>
```
PS C:\> New-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

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

<span data-ttu-id="e45c4-109">Skapar abonnemanget `SB-TopicSubscription-Example1` för den angivna tjänst Bus artikeln `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="e45c4-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="e45c4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e45c4-110">PARAMETERS</span></span>

### <span data-ttu-id="e45c4-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="e45c4-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="e45c4-112">Anger [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) Idle Interval efter vilket prenumerationen automatiskt raderas.</span><span class="sxs-lookup"><span data-stu-id="e45c4-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="e45c4-113">Minsta varaktighet är 5 minuter.</span><span class="sxs-lookup"><span data-stu-id="e45c4-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="e45c4-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="e45c4-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="e45c4-115">Värde som anger om ett abonnemang har stöd för obeställbara meddelanden om undantag för filter utvärdering.</span><span class="sxs-lookup"><span data-stu-id="e45c4-115">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="e45c4-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="e45c4-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="e45c4-117">Död Brevering för meddelande</span><span class="sxs-lookup"><span data-stu-id="e45c4-117">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="e45c4-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="e45c4-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="e45c4-119">TimeSpan to Live-värde.</span><span class="sxs-lookup"><span data-stu-id="e45c4-119">Timespan to live value.</span></span>
<span data-ttu-id="e45c4-120">Det här är den tid som meddelandet upphör att gälla, från och med när meddelandet skickas till Service Bus.</span><span class="sxs-lookup"><span data-stu-id="e45c4-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="e45c4-121">Det här är standardvärdet som används när TimeToLive inte är inställt på ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="e45c4-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="e45c4-122">Standard = TimeSpan. max och Basic = 14 dagar</span><span class="sxs-lookup"><span data-stu-id="e45c4-122">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="e45c4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e45c4-123">-DefaultProfile</span></span>
<span data-ttu-id="e45c4-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e45c4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e45c4-125">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="e45c4-125">-EnableBatchedOperations</span></span>
<span data-ttu-id="e45c4-126">Aktivera grupp operationer-värde som anger om grupp operationer på Server sidan är aktiverade</span><span class="sxs-lookup"><span data-stu-id="e45c4-126">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="e45c4-127">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="e45c4-127">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="e45c4-128">Namn på kö för att vidarekoppla meddelandet om obeställbara meddelanden</span><span class="sxs-lookup"><span data-stu-id="e45c4-128">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="e45c4-129">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="e45c4-129">-ForwardTo</span></span>
<span data-ttu-id="e45c4-130">Namn på kö/ämne för att vidarekoppla meddelanden</span><span class="sxs-lookup"><span data-stu-id="e45c4-130">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="e45c4-131">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="e45c4-131">-LockDuration</span></span>
<span data-ttu-id="e45c4-132">Lås varaktighet</span><span class="sxs-lookup"><span data-stu-id="e45c4-132">Lock Duration</span></span>

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

### <span data-ttu-id="e45c4-133">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="e45c4-133">-MaxDeliveryCount</span></span>
<span data-ttu-id="e45c4-134">MaxDeliveryCount-högsta antal leveranser.</span><span class="sxs-lookup"><span data-stu-id="e45c4-134">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="e45c4-135">Ett meddelande deadlettered automatiskt efter detta antal leveranser.</span><span class="sxs-lookup"><span data-stu-id="e45c4-135">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="e45c4-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="e45c4-136">-Name</span></span>
<span data-ttu-id="e45c4-137">Prenumerationens namn</span><span class="sxs-lookup"><span data-stu-id="e45c4-137">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e45c4-138">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="e45c4-138">-Namespace</span></span>
<span data-ttu-id="e45c4-139">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="e45c4-139">Namespace Name</span></span>

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

### <span data-ttu-id="e45c4-140">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="e45c4-140">-RequiresSession</span></span>
<span data-ttu-id="e45c4-141">RequiresSession-det värde som anger om den här kön kräver dubblettidentifiering.</span><span class="sxs-lookup"><span data-stu-id="e45c4-141">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="e45c4-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e45c4-142">-ResourceGroupName</span></span>
<span data-ttu-id="e45c4-143">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="e45c4-143">The name of the resource group</span></span>

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

### <span data-ttu-id="e45c4-144">-Ämne</span><span class="sxs-lookup"><span data-stu-id="e45c4-144">-Topic</span></span>
<span data-ttu-id="e45c4-145">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="e45c4-145">Topic Name</span></span>

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

### <span data-ttu-id="e45c4-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e45c4-146">-Confirm</span></span>
<span data-ttu-id="e45c4-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e45c4-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e45c4-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e45c4-148">-WhatIf</span></span>
<span data-ttu-id="e45c4-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e45c4-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e45c4-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e45c4-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e45c4-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e45c4-151">CommonParameters</span></span>
<span data-ttu-id="e45c4-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e45c4-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e45c4-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e45c4-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e45c4-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e45c4-154">INPUTS</span></span>

### <span data-ttu-id="e45c4-155">System. String</span><span class="sxs-lookup"><span data-stu-id="e45c4-155">System.String</span></span>

### <span data-ttu-id="e45c4-156">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e45c4-156">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e45c4-157">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e45c4-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e45c4-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e45c4-158">OUTPUTS</span></span>

### <span data-ttu-id="e45c4-159">Microsoft. Azure. commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="e45c4-159">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="e45c4-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e45c4-160">NOTES</span></span>

## <span data-ttu-id="e45c4-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e45c4-161">RELATED LINKS</span></span>