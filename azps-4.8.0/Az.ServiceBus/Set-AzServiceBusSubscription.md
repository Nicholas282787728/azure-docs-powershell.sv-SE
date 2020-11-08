---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
ms.openlocfilehash: 2bff80a8f04dada3625eaa5b0a16287bb37c6a13
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100831"
---
# <span data-ttu-id="5afb4-101">Set-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="5afb4-101">Set-AzServiceBusSubscription</span></span>

## <span data-ttu-id="5afb4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5afb4-102">SYNOPSIS</span></span>
<span data-ttu-id="5afb4-103">Uppdaterar en prenumerations beskrivning för ett tjänst Bus ämne i angivet Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="5afb4-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="5afb4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5afb4-104">SYNTAX</span></span>

```
Set-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <PSSubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5afb4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5afb4-105">DESCRIPTION</span></span>
<span data-ttu-id="5afb4-106">Cmdleten **set-AzServiceBusSubscription** uppdaterar beskrivningen av prenumerationen för Service Bus-ämnet i angivet Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="5afb4-106">The **Set-AzServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="5afb4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5afb4-107">EXAMPLES</span></span>

### <span data-ttu-id="5afb4-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5afb4-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

PS C:\> $subscriptionObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $subscriptionObj.MaxDeliveryCount = 9

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : 
CreatedAt                                 : 1/20/2017 9:59:15 PM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : True
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 9
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 9:59:15 PM
PS C:\> Set-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="5afb4-109">Uppdaterar beskrivningen för det angivna abonnemanget till det angivna avsnittet.</span><span class="sxs-lookup"><span data-stu-id="5afb4-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="5afb4-110">Det här exemplet uppdaterar egenskapen **DeadLetteringOnMessageExpiration** till **True** och **MaxDeliveryCount** till 9.</span><span class="sxs-lookup"><span data-stu-id="5afb4-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="5afb4-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5afb4-111">PARAMETERS</span></span>

### <span data-ttu-id="5afb4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5afb4-112">-DefaultProfile</span></span>
<span data-ttu-id="5afb4-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5afb4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5afb4-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5afb4-114">-InputObject</span></span>
<span data-ttu-id="5afb4-115">ServiceBus abonnemangs definition.</span><span class="sxs-lookup"><span data-stu-id="5afb4-115">ServiceBus Subscription definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5afb4-116">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="5afb4-116">-Namespace</span></span>
<span data-ttu-id="5afb4-117">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="5afb4-117">Namespace Name.</span></span>

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

### <span data-ttu-id="5afb4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5afb4-118">-ResourceGroupName</span></span>
<span data-ttu-id="5afb4-119">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="5afb4-119">The name of the resource group</span></span>

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

### <span data-ttu-id="5afb4-120">-Ämne</span><span class="sxs-lookup"><span data-stu-id="5afb4-120">-Topic</span></span>
<span data-ttu-id="5afb4-121">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="5afb4-121">Topic Name.</span></span>

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

### <span data-ttu-id="5afb4-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5afb4-122">-Confirm</span></span>
<span data-ttu-id="5afb4-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5afb4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5afb4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5afb4-124">-WhatIf</span></span>
<span data-ttu-id="5afb4-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5afb4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5afb4-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5afb4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5afb4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5afb4-127">CommonParameters</span></span>
<span data-ttu-id="5afb4-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5afb4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5afb4-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5afb4-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5afb4-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5afb4-130">INPUTS</span></span>

### <span data-ttu-id="5afb4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5afb4-131">System.String</span></span>

### <span data-ttu-id="5afb4-132">Microsoft. Azure. commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="5afb4-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="5afb4-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5afb4-133">OUTPUTS</span></span>

### <span data-ttu-id="5afb4-134">Microsoft. Azure. commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="5afb4-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="5afb4-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5afb4-135">NOTES</span></span>

## <span data-ttu-id="5afb4-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5afb4-136">RELATED LINKS</span></span>
