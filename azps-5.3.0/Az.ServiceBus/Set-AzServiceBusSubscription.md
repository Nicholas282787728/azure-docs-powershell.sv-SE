---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
ms.openlocfilehash: 2bff80a8f04dada3625eaa5b0a16287bb37c6a13
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525466"
---
# <span data-ttu-id="24361-101">Set-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="24361-101">Set-AzServiceBusSubscription</span></span>

## <span data-ttu-id="24361-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24361-102">SYNOPSIS</span></span>
<span data-ttu-id="24361-103">Uppdaterar en prenumerations beskrivning för ett tjänst Bus ämne i angivet Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="24361-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="24361-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24361-104">SYNTAX</span></span>

```
Set-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <PSSubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24361-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24361-105">DESCRIPTION</span></span>
<span data-ttu-id="24361-106">Cmdleten **set-AzServiceBusSubscription** uppdaterar beskrivningen av prenumerationen för Service Bus-ämnet i angivet Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="24361-106">The **Set-AzServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="24361-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24361-107">EXAMPLES</span></span>

### <span data-ttu-id="24361-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="24361-108">Example 1</span></span>
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

<span data-ttu-id="24361-109">Uppdaterar beskrivningen för det angivna abonnemanget till det angivna avsnittet.</span><span class="sxs-lookup"><span data-stu-id="24361-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="24361-110">Det här exemplet uppdaterar egenskapen **DeadLetteringOnMessageExpiration** till **True** och **MaxDeliveryCount** till 9.</span><span class="sxs-lookup"><span data-stu-id="24361-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="24361-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24361-111">PARAMETERS</span></span>

### <span data-ttu-id="24361-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24361-112">-DefaultProfile</span></span>
<span data-ttu-id="24361-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="24361-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24361-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24361-114">-InputObject</span></span>
<span data-ttu-id="24361-115">ServiceBus abonnemangs definition.</span><span class="sxs-lookup"><span data-stu-id="24361-115">ServiceBus Subscription definition.</span></span>

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

### <span data-ttu-id="24361-116">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="24361-116">-Namespace</span></span>
<span data-ttu-id="24361-117">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="24361-117">Namespace Name.</span></span>

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

### <span data-ttu-id="24361-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24361-118">-ResourceGroupName</span></span>
<span data-ttu-id="24361-119">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="24361-119">The name of the resource group</span></span>

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

### <span data-ttu-id="24361-120">-Ämne</span><span class="sxs-lookup"><span data-stu-id="24361-120">-Topic</span></span>
<span data-ttu-id="24361-121">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="24361-121">Topic Name.</span></span>

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

### <span data-ttu-id="24361-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="24361-122">-Confirm</span></span>
<span data-ttu-id="24361-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="24361-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24361-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24361-124">-WhatIf</span></span>
<span data-ttu-id="24361-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="24361-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24361-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="24361-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24361-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24361-127">CommonParameters</span></span>
<span data-ttu-id="24361-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24361-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24361-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24361-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24361-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24361-130">INPUTS</span></span>

### <span data-ttu-id="24361-131">System. String</span><span class="sxs-lookup"><span data-stu-id="24361-131">System.String</span></span>

### <span data-ttu-id="24361-132">Microsoft. Azure. commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="24361-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="24361-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24361-133">OUTPUTS</span></span>

### <span data-ttu-id="24361-134">Microsoft. Azure. commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="24361-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="24361-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24361-135">NOTES</span></span>

## <span data-ttu-id="24361-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24361-136">RELATED LINKS</span></span>
