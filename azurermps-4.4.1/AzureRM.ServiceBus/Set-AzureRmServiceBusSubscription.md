---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 13e221c0205f07be81d01fd5011fa2d937b020a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757744"
---
# <span data-ttu-id="ac56e-101">Set-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="ac56e-101">Set-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="ac56e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac56e-102">SYNOPSIS</span></span>
<span data-ttu-id="ac56e-103">Uppdaterar en prenumerations beskrivning för ett tjänst Bus ämne i angivet Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="ac56e-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac56e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac56e-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -InputObject <SubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ac56e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac56e-105">DESCRIPTION</span></span>
<span data-ttu-id="ac56e-106">Cmdleten **set-AzureRmServiceBusSubscription** uppdaterar beskrivningen av prenumerationen för Service Bus-ämnet i angivet Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="ac56e-106">The **Set-AzureRmServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ac56e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac56e-107">EXAMPLES</span></span>

### <span data-ttu-id="ac56e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ac56e-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

PS C:\> $subscriptionObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $subscriptionObj.MaxDeliveryCount = 9

PS C:\> Set-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="ac56e-109">Uppdaterar beskrivningen för det angivna abonnemanget till det angivna avsnittet.</span><span class="sxs-lookup"><span data-stu-id="ac56e-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="ac56e-110">Det här exemplet uppdaterar egenskapen **DeadLetteringOnMessageExpiration** till **True** och **MaxDeliveryCount** till 9.</span><span class="sxs-lookup"><span data-stu-id="ac56e-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="ac56e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac56e-111">PARAMETERS</span></span>

### <span data-ttu-id="ac56e-112">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ac56e-112">-Confirm</span></span>
<span data-ttu-id="ac56e-113">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ac56e-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac56e-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac56e-114">-WhatIf</span></span>
<span data-ttu-id="ac56e-115">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ac56e-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac56e-116">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ac56e-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac56e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac56e-117">-DefaultProfile</span></span>
<span data-ttu-id="ac56e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ac56e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac56e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac56e-119">-InputObject</span></span>
<span data-ttu-id="ac56e-120">ServiceBus abonnemangs definition.</span><span class="sxs-lookup"><span data-stu-id="ac56e-120">ServiceBus Subscription definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac56e-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="ac56e-121">-Namespace</span></span>
<span data-ttu-id="ac56e-122">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="ac56e-122">Namespace Name.</span></span>

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

### <span data-ttu-id="ac56e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac56e-123">-ResourceGroupName</span></span>
<span data-ttu-id="ac56e-124">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="ac56e-124">The name of the resource group</span></span>

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

### <span data-ttu-id="ac56e-125">-Ämne</span><span class="sxs-lookup"><span data-stu-id="ac56e-125">-Topic</span></span>
<span data-ttu-id="ac56e-126">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="ac56e-126">Topic Name.</span></span>

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

### <span data-ttu-id="ac56e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac56e-127">CommonParameters</span></span>
<span data-ttu-id="ac56e-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac56e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac56e-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac56e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac56e-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac56e-130">INPUTS</span></span>

### <span data-ttu-id="ac56e-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ac56e-131">-ResourceGroup</span></span>
 <span data-ttu-id="ac56e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ac56e-132">System.String</span></span>

### <span data-ttu-id="ac56e-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="ac56e-133">-NamespaceName</span></span>
 <span data-ttu-id="ac56e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ac56e-134">System.String</span></span>

### <span data-ttu-id="ac56e-135">-TopicName</span><span class="sxs-lookup"><span data-stu-id="ac56e-135">-TopicName</span></span>
 <span data-ttu-id="ac56e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ac56e-136">System.String</span></span>

### <span data-ttu-id="ac56e-137">-SubscriptionObj</span><span class="sxs-lookup"><span data-stu-id="ac56e-137">-SubscriptionObj</span></span>
 <span data-ttu-id="ac56e-138">Microsoft. Azure. commands. ServiceBus. Models. SubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="ac56e-138">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>

## <span data-ttu-id="ac56e-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac56e-139">OUTPUTS</span></span>

### <span data-ttu-id="ac56e-140">Microsoft. Azure. commands. ServiceBus. Models. SubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="ac56e-140">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="ac56e-141">Namn: SB-TopicSubscription-Example1 Location: West US AccessedAt: 1/1/0001 12:00:00 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 CountDetails: CreatedAt: 1/20/2017 9:59:15 PM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions: true DeadLetteringOnMessageExpiration: EnableBatchedOperations: true EntityAvailabilityStatus: tillgänglig IsReadOnly: LockDuration: 00:01:00 MaxDeliveryCount: 9 MessageCount: 0 RequiresSession: falsk status: aktiv UpdatedAt: 1/20/2017 9:59:15 PM</span><span class="sxs-lookup"><span data-stu-id="ac56e-141">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/1/0001 12:00:00 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : CreatedAt                                 : 1/20/2017 9:59:15 PM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : True EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 9 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 9:59:15 PM</span></span>

## <span data-ttu-id="ac56e-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac56e-142">NOTES</span></span>

## <span data-ttu-id="ac56e-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac56e-143">RELATED LINKS</span></span>

