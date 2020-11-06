---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
ms.openlocfilehash: 92c26b2b92257de7cdd3bbbb0d602d45d8ea1d1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575495"
---
# <span data-ttu-id="fa868-101">Set-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="fa868-101">Set-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="fa868-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fa868-102">SYNOPSIS</span></span>
<span data-ttu-id="fa868-103">Uppdaterar beskrivningen av ett tjänst Bus-avsnitt i angivet Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="fa868-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa868-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fa868-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <TopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa868-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fa868-105">DESCRIPTION</span></span>
<span data-ttu-id="fa868-106">Cmdleten **set-AzureRmServiceBusTopic** uppdaterar ett Description-objekt för ett tjänst Bus ämne i det angivna tjänst buss namn området.</span><span class="sxs-lookup"><span data-stu-id="fa868-106">The **Set-AzureRmServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="fa868-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fa868-107">EXAMPLES</span></span>

### <span data-ttu-id="fa868-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fa868-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -TopicObj $topicObj

Name                                : SB-Topic_exampl1
Id                                  : /subscriptions/{subscription id}d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-
                                      Topic_exampl1
Type                                : Microsoft.ServiceBus/Topic
AccessedAt                          : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 3:16:41 AM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
EnableBatchedOperations             : True
EnableExpress                       : True
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 16384
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 1
SupportOrdering                     : False
UpdatedAt                           : 1/20/2017 7:12:16 PM
```
<span data-ttu-id="fa868-109">Uppdaterar angivet avsnitt med en ny beskrivning i det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="fa868-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="fa868-110">Det här exemplet uppdaterar egenskapen **EnableExpress** till **True**.</span><span class="sxs-lookup"><span data-stu-id="fa868-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="fa868-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fa868-111">PARAMETERS</span></span>

### <span data-ttu-id="fa868-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa868-112">-DefaultProfile</span></span>
<span data-ttu-id="fa868-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fa868-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa868-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa868-114">-InputObject</span></span>
<span data-ttu-id="fa868-115">Avsnitts definitionen ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="fa868-115">ServiceBus Topic definition.</span></span>

```yaml
Type: PSTopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa868-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="fa868-116">-Name</span></span>
<span data-ttu-id="fa868-117">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="fa868-117">Topic Name.</span></span>

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

### <span data-ttu-id="fa868-118">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="fa868-118">-Namespace</span></span>
<span data-ttu-id="fa868-119">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="fa868-119">Namespace Name.</span></span>

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

### <span data-ttu-id="fa868-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa868-120">-ResourceGroupName</span></span>
<span data-ttu-id="fa868-121">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="fa868-121">The name of the resource group</span></span>

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

### <span data-ttu-id="fa868-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fa868-122">-Confirm</span></span>
<span data-ttu-id="fa868-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fa868-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa868-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa868-124">-WhatIf</span></span>
<span data-ttu-id="fa868-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fa868-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa868-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fa868-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa868-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa868-127">CommonParameters</span></span>
<span data-ttu-id="fa868-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa868-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa868-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa868-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa868-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fa868-130">INPUTS</span></span>

### <span data-ttu-id="fa868-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fa868-131">-ResourceGroup</span></span>
 <span data-ttu-id="fa868-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fa868-132">System.String</span></span>

### <span data-ttu-id="fa868-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="fa868-133">-NamespaceName</span></span>
 <span data-ttu-id="fa868-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fa868-134">System.String</span></span>

### <span data-ttu-id="fa868-135">-TopicName</span><span class="sxs-lookup"><span data-stu-id="fa868-135">-TopicName</span></span>
 <span data-ttu-id="fa868-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fa868-136">System.String</span></span>

### <span data-ttu-id="fa868-137">-TopicObj</span><span class="sxs-lookup"><span data-stu-id="fa868-137">-TopicObj</span></span>
 <span data-ttu-id="fa868-138">Microsoft. Azure. commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="fa868-138">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="fa868-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fa868-139">OUTPUTS</span></span>

### <span data-ttu-id="fa868-140">Microsoft. Azure. commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="fa868-140">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="fa868-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fa868-141">NOTES</span></span>

## <span data-ttu-id="fa868-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fa868-142">RELATED LINKS</span></span>

