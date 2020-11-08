---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
ms.openlocfilehash: 8e8fe04476e66db6b45372879ac3176f9d492acc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092030"
---
# <span data-ttu-id="2e062-101">Set-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="2e062-101">Set-AzServiceBusTopic</span></span>

## <span data-ttu-id="2e062-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2e062-102">SYNOPSIS</span></span>
<span data-ttu-id="2e062-103">Uppdaterar beskrivningen av ett tjänst Bus-avsnitt i angivet Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="2e062-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="2e062-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2e062-104">SYNTAX</span></span>

```
Set-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSTopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e062-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2e062-105">DESCRIPTION</span></span>
<span data-ttu-id="2e062-106">Cmdleten **set-AzServiceBusTopic** uppdaterar ett Description-objekt för ett tjänst Bus ämne i det angivna tjänst buss namn området.</span><span class="sxs-lookup"><span data-stu-id="2e062-106">The **Set-AzServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="2e062-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2e062-107">EXAMPLES</span></span>

### <span data-ttu-id="2e062-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2e062-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1 -TopicObj $topicObj

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-ExampleStandard/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/12/2018 12:01:28 AM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : False
UpdatedAt                           : 10/12/2018 12:01:29 AM
```

<span data-ttu-id="2e062-109">Uppdaterar angivet avsnitt med en ny beskrivning i det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="2e062-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="2e062-110">Det här exemplet uppdaterar egenskapen **EnableExpress** till **True**.</span><span class="sxs-lookup"><span data-stu-id="2e062-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="2e062-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2e062-111">PARAMETERS</span></span>

### <span data-ttu-id="2e062-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e062-112">-DefaultProfile</span></span>
<span data-ttu-id="2e062-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2e062-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e062-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e062-114">-InputObject</span></span>
<span data-ttu-id="2e062-115">Avsnitts definitionen ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="2e062-115">ServiceBus Topic definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e062-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="2e062-116">-Name</span></span>
<span data-ttu-id="2e062-117">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="2e062-117">Topic Name.</span></span>

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

### <span data-ttu-id="2e062-118">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="2e062-118">-Namespace</span></span>
<span data-ttu-id="2e062-119">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="2e062-119">Namespace Name.</span></span>

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

### <span data-ttu-id="2e062-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e062-120">-ResourceGroupName</span></span>
<span data-ttu-id="2e062-121">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="2e062-121">The name of the resource group</span></span>

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

### <span data-ttu-id="2e062-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2e062-122">-Confirm</span></span>
<span data-ttu-id="2e062-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2e062-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e062-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e062-124">-WhatIf</span></span>
<span data-ttu-id="2e062-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2e062-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e062-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2e062-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e062-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e062-127">CommonParameters</span></span>
<span data-ttu-id="2e062-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e062-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e062-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e062-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e062-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2e062-130">INPUTS</span></span>

### <span data-ttu-id="2e062-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2e062-131">System.String</span></span>

### <span data-ttu-id="2e062-132">Microsoft. Azure. commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="2e062-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="2e062-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2e062-133">OUTPUTS</span></span>

### <span data-ttu-id="2e062-134">Microsoft. Azure. commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="2e062-134">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="2e062-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2e062-135">NOTES</span></span>

## <span data-ttu-id="2e062-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2e062-136">RELATED LINKS</span></span>
