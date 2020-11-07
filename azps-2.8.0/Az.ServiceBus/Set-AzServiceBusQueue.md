---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
ms.openlocfilehash: 4206e29ad56e1d7b48b9d87a66b8a85960c4707e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919182"
---
# <span data-ttu-id="c4431-101">Set-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="c4431-101">Set-AzServiceBusQueue</span></span>

## <span data-ttu-id="c4431-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4431-102">SYNOPSIS</span></span>
<span data-ttu-id="c4431-103">Uppdaterar beskrivningen av en Service Bus-kö i angivet Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="c4431-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="c4431-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4431-104">SYNTAX</span></span>

```
Set-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSQueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4431-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4431-105">DESCRIPTION</span></span>
<span data-ttu-id="c4431-106">Cmdleten **set-AzServiceBusQueue** uppdaterar beskrivningen för Service Bus-kön i angivet Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="c4431-106">The **Set-AzServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="c4431-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4431-107">EXAMPLES</span></span>

### <span data-ttu-id="c4431-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c4431-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -QueueObj $QueueObj

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1
Name                                : SB-Queue_exampl1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 1/1/0001 12:00:00 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxDeliveryCount                    : 10
MaxSizeInMegabytes                  : 81920
MessageCount                        : 0
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 0
Status                              : Active
UpdatedAt                           : 1/1/0001 12:00:00 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="c4431-109">Uppdaterar den angivna kön med en ny beskrivning i det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="c4431-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="c4431-110">Det här exemplet uppdaterar egenskapen **DeadLetteringOnMessageExpiration** till **True** och **SupportOrdering** till **True**.</span><span class="sxs-lookup"><span data-stu-id="c4431-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="c4431-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4431-111">PARAMETERS</span></span>

### <span data-ttu-id="c4431-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4431-112">-DefaultProfile</span></span>
<span data-ttu-id="c4431-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c4431-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4431-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4431-114">-InputObject</span></span>
<span data-ttu-id="c4431-115">ServiceBus-definitionen.</span><span class="sxs-lookup"><span data-stu-id="c4431-115">ServiceBus definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes
Parameter Sets: (All)
Aliases: QueueObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4431-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="c4431-116">-Name</span></span>
<span data-ttu-id="c4431-117">Könamn.</span><span class="sxs-lookup"><span data-stu-id="c4431-117">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4431-118">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="c4431-118">-Namespace</span></span>
<span data-ttu-id="c4431-119">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="c4431-119">Namespace Name.</span></span>

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

### <span data-ttu-id="c4431-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4431-120">-ResourceGroupName</span></span>
<span data-ttu-id="c4431-121">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="c4431-121">The name of the resource group</span></span>

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

### <span data-ttu-id="c4431-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c4431-122">-Confirm</span></span>
<span data-ttu-id="c4431-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c4431-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4431-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4431-124">-WhatIf</span></span>
<span data-ttu-id="c4431-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c4431-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4431-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c4431-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4431-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4431-127">CommonParameters</span></span>
<span data-ttu-id="c4431-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4431-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4431-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4431-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4431-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4431-130">INPUTS</span></span>

### <span data-ttu-id="c4431-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c4431-131">System.String</span></span>

### <span data-ttu-id="c4431-132">Microsoft. Azure. commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="c4431-132">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="c4431-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4431-133">OUTPUTS</span></span>

### <span data-ttu-id="c4431-134">Microsoft. Azure. commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="c4431-134">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="c4431-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4431-135">NOTES</span></span>

## <span data-ttu-id="c4431-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4431-136">RELATED LINKS</span></span>
