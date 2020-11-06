---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
ms.openlocfilehash: ea305b334e6efd4cb1c5af47db2a1b8817e7cab6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577435"
---
# <span data-ttu-id="ad340-101">New-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="ad340-101">New-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="ad340-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad340-102">SYNOPSIS</span></span>
<span data-ttu-id="ad340-103">Skapar ett abonnemang för den angivna tjänst Bus artikeln.</span><span class="sxs-lookup"><span data-stu-id="ad340-103">Creates a subscription to the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad340-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad340-104">SYNTAX</span></span>

```
New-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -Name <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnFilterEvaluationExceptions <Boolean>] [-DeadLetteringOnMessageExpiration <Boolean>]
 [-EnableBatchedOperations <Boolean>] [-IsReadOnly <Boolean>] [-LockDuration <String>]
 [-MaxDeliveryCount <Int32>] [-RequiresSession <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad340-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad340-105">DESCRIPTION</span></span>
<span data-ttu-id="ad340-106">Cmdleten **New-AzureRmServiceBusSubscription** skapar ett nytt abonnemang för den angivna tjänst Bus artikeln.</span><span class="sxs-lookup"><span data-stu-id="ad340-106">The **New-AzureRmServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="ad340-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad340-107">EXAMPLES</span></span>

### <span data-ttu-id="ad340-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ad340-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="ad340-109">Skapar abonnemanget `SB-TopicSubscription-Example1` för den angivna tjänst Bus artikeln `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="ad340-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="ad340-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad340-110">PARAMETERS</span></span>

### <span data-ttu-id="ad340-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="ad340-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="ad340-112">Anger [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) Idle Interval efter vilket prenumerationen automatiskt raderas.</span><span class="sxs-lookup"><span data-stu-id="ad340-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="ad340-113">Minsta varaktighet är 5 minuter.</span><span class="sxs-lookup"><span data-stu-id="ad340-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="ad340-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="ad340-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="ad340-115">Anger om en prenumeration har stöd för obeställbara meddelanden om undantag för filter utvärdering.</span><span class="sxs-lookup"><span data-stu-id="ad340-115">Indicates if a subscription has dead letter support on Filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="ad340-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="ad340-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="ad340-117">Anger om en prenumeration har deadletter-stöd när ett meddelande upphör.</span><span class="sxs-lookup"><span data-stu-id="ad340-117">Indicates if a subscription has deadletter support when a message expires.</span></span>

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

### <span data-ttu-id="ad340-118">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="ad340-118">-EnableBatchedOperations</span></span>
<span data-ttu-id="ad340-119">Anger om grupp operationer på Server sidan är aktiverade.</span><span class="sxs-lookup"><span data-stu-id="ad340-119">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="ad340-120">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="ad340-120">-IsReadOnly</span></span>
<span data-ttu-id="ad340-121">Anger om beskrivningen är skrivskyddad</span><span class="sxs-lookup"><span data-stu-id="ad340-121">Indicates whether the entity description is read-only</span></span>

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

### <span data-ttu-id="ad340-122">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="ad340-122">-LockDuration</span></span>
<span data-ttu-id="ad340-123">Anger tids rymden för låsning för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="ad340-123">Specifies the lock duration time span for the subscription.</span></span>

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

### <span data-ttu-id="ad340-124">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="ad340-124">-MaxDeliveryCount</span></span>
<span data-ttu-id="ad340-125">Anger antalet maximala leveranser.</span><span class="sxs-lookup"><span data-stu-id="ad340-125">Specifies the number of maximum deliveries.</span></span> <span data-ttu-id="ad340-126">Ett meddelande deadlettered automatiskt efter detta antal leveranser.</span><span class="sxs-lookup"><span data-stu-id="ad340-126">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="ad340-127">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="ad340-127">-RequiresSession</span></span>
<span data-ttu-id="ad340-128">Anger om ett abonnemang har stöd för konceptet med sessioner.</span><span class="sxs-lookup"><span data-stu-id="ad340-128">Specifies whether a subscription supports the concept of sessions.</span></span>

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

### <span data-ttu-id="ad340-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ad340-129">-Confirm</span></span>
<span data-ttu-id="ad340-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ad340-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad340-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad340-131">-WhatIf</span></span>
<span data-ttu-id="ad340-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ad340-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad340-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ad340-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad340-134">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="ad340-134">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="ad340-135">TimeSpan to Live-värde.</span><span class="sxs-lookup"><span data-stu-id="ad340-135">Timespan to live value.</span></span> <span data-ttu-id="ad340-136">Det här är den tid som meddelandet upphör att gälla, från och med när meddelandet skickas till Service Bus.</span><span class="sxs-lookup"><span data-stu-id="ad340-136">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span> <span data-ttu-id="ad340-137">Det här är standardvärdet som används när TimeToLive inte är inställt på ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="ad340-137">This is the default value used when TimeToLive is not set on a message itself.</span></span> <span data-ttu-id="ad340-138">Standard = TimeSpan. max och Basic = 14 dyas</span><span class="sxs-lookup"><span data-stu-id="ad340-138">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="ad340-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad340-139">-DefaultProfile</span></span>
<span data-ttu-id="ad340-140">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ad340-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad340-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="ad340-141">-Name</span></span>
<span data-ttu-id="ad340-142">Prenumerationens namn</span><span class="sxs-lookup"><span data-stu-id="ad340-142">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad340-143">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="ad340-143">-Namespace</span></span>
<span data-ttu-id="ad340-144">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="ad340-144">Namespace Name.</span></span>

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

### <span data-ttu-id="ad340-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad340-145">-ResourceGroupName</span></span>
<span data-ttu-id="ad340-146">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="ad340-146">The name of the resource group</span></span>

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

### <span data-ttu-id="ad340-147">-Ämne</span><span class="sxs-lookup"><span data-stu-id="ad340-147">-Topic</span></span>
<span data-ttu-id="ad340-148">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="ad340-148">Topic Name.</span></span>

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

### <span data-ttu-id="ad340-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad340-149">CommonParameters</span></span>
<span data-ttu-id="ad340-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad340-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad340-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad340-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad340-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad340-152">INPUTS</span></span>

### <span data-ttu-id="ad340-153">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ad340-153">-ResourceGroup</span></span>
 <span data-ttu-id="ad340-154">System. String</span><span class="sxs-lookup"><span data-stu-id="ad340-154">System.String</span></span>
 

### <span data-ttu-id="ad340-155">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="ad340-155">-NamespaceName</span></span>
 <span data-ttu-id="ad340-156">System. String</span><span class="sxs-lookup"><span data-stu-id="ad340-156">System.String</span></span>
 

### <span data-ttu-id="ad340-157">-TopicName</span><span class="sxs-lookup"><span data-stu-id="ad340-157">-TopicName</span></span>
 <span data-ttu-id="ad340-158">System. String</span><span class="sxs-lookup"><span data-stu-id="ad340-158">System.String</span></span>
 

### <span data-ttu-id="ad340-159">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ad340-159">-SubscriptionName</span></span>
 <span data-ttu-id="ad340-160">System. String</span><span class="sxs-lookup"><span data-stu-id="ad340-160">System.String</span></span>

## <span data-ttu-id="ad340-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad340-161">OUTPUTS</span></span>

### <span data-ttu-id="ad340-162">Microsoft. Azure. commands. ServiceBus. Models. SubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="ad340-162">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="ad340-163">Namn: SB-TopicSubscription-Example1-plats: 1/20/2017 3:18:54 am AutoDeleteOnIdle: 10675199.02:48:05.4775807 CountDetails: Microsoft. Azure. Management. ServiceBus. MODELES. MessageCountDetails CreatedAt: 1/20/2017 3:18:52 AM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions: true DeadLetteringOnMessageExpiration: false EnableBatchedOperations: true EntityAvailabilityStatus: tillgänglig IsReadOnly: LockDuration: 00:01:00 MaxDeliveryCount: 10 MessageCount: 0 RequiresSession: false status: Active UpdatedAt: 1/20/2017 3:18:54 AM</span><span class="sxs-lookup"><span data-stu-id="ad340-163">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails CreatedAt                                 : 1/20/2017 3:18:52 AM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : False EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 10 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 3:18:54 AM</span></span>

## <span data-ttu-id="ad340-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad340-164">NOTES</span></span>

## <span data-ttu-id="ad340-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad340-165">RELATED LINKS</span></span>

