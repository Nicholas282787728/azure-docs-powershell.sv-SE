---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
ms.openlocfilehash: 8c02c596b1b1eecb8654b07a2392d2336c0b0215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755676"
---
# <span data-ttu-id="ea517-101">Set-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="ea517-101">Set-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="ea517-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea517-102">SYNOPSIS</span></span>
<span data-ttu-id="ea517-103">Uppdaterar beskrivningen av en Service Bus-kö i angivet Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="ea517-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea517-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea517-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSQueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea517-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea517-105">DESCRIPTION</span></span>
<span data-ttu-id="ea517-106">Cmdleten **set-AzureRmServiceBusQueue** uppdaterar beskrivningen för Service Bus-kön i angivet Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="ea517-106">The **Set-AzureRmServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ea517-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea517-107">EXAMPLES</span></span>

### <span data-ttu-id="ea517-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ea517-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -QueueObj $QueueObj

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

<span data-ttu-id="ea517-109">Uppdaterar den angivna kön med en ny beskrivning i det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="ea517-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="ea517-110">Det här exemplet uppdaterar egenskapen **DeadLetteringOnMessageExpiration** till **True** och **SupportOrdering** till **True**.</span><span class="sxs-lookup"><span data-stu-id="ea517-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="ea517-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea517-111">PARAMETERS</span></span>

### <span data-ttu-id="ea517-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea517-112">-DefaultProfile</span></span>
<span data-ttu-id="ea517-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ea517-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea517-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea517-114">-InputObject</span></span>
<span data-ttu-id="ea517-115">ServiceBus-definitionen.</span><span class="sxs-lookup"><span data-stu-id="ea517-115">ServiceBus definition.</span></span>

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

### <span data-ttu-id="ea517-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="ea517-116">-Name</span></span>
<span data-ttu-id="ea517-117">Könamn.</span><span class="sxs-lookup"><span data-stu-id="ea517-117">Queue Name.</span></span>

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

### <span data-ttu-id="ea517-118">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="ea517-118">-Namespace</span></span>
<span data-ttu-id="ea517-119">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="ea517-119">Namespace Name.</span></span>

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

### <span data-ttu-id="ea517-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea517-120">-ResourceGroupName</span></span>
<span data-ttu-id="ea517-121">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="ea517-121">The name of the resource group</span></span>

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

### <span data-ttu-id="ea517-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ea517-122">-Confirm</span></span>
<span data-ttu-id="ea517-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ea517-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea517-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea517-124">-WhatIf</span></span>
<span data-ttu-id="ea517-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ea517-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea517-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ea517-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea517-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea517-127">CommonParameters</span></span>
<span data-ttu-id="ea517-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea517-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea517-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea517-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea517-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea517-130">INPUTS</span></span>

### <span data-ttu-id="ea517-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ea517-131">System.String</span></span>

### <span data-ttu-id="ea517-132">Microsoft. Azure. commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="ea517-132">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="ea517-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea517-133">OUTPUTS</span></span>

### <span data-ttu-id="ea517-134">Microsoft. Azure. commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="ea517-134">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="ea517-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea517-135">NOTES</span></span>

## <span data-ttu-id="ea517-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea517-136">RELATED LINKS</span></span>
