---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
ms.openlocfilehash: 099e86e8ed085169823c40d51de376085f768753
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919216"
---
# <span data-ttu-id="63313-101">Get-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="63313-101">Get-AzServiceBusQueue</span></span>

## <span data-ttu-id="63313-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63313-102">SYNOPSIS</span></span>
<span data-ttu-id="63313-103">Returnerar en beskrivning för den angivna tjänst buss kön.</span><span class="sxs-lookup"><span data-stu-id="63313-103">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="63313-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63313-104">SYNTAX</span></span>

```
Get-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63313-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63313-105">DESCRIPTION</span></span>
<span data-ttu-id="63313-106">Returnerar en beskrivning för den angivna tjänst buss kön.</span><span class="sxs-lookup"><span data-stu-id="63313-106">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="63313-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63313-107">EXAMPLES</span></span>

### <span data-ttu-id="63313-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="63313-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_example1
Name                                : SB-Queue_example1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 12:37:11 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : False
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
UpdatedAt                           : 10/11/2018 12:37:11 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="63313-109">Returnerar beskrivningen av kön.</span><span class="sxs-lookup"><span data-stu-id="63313-109">Returns the description of the queue.</span></span>

### <span data-ttu-id="63313-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="63313-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="63313-111">Returnerar en lista med köer för det angivna namn området, som standard kommer 100-köer att returneras, om fler än 100 köer ska returneras, Använd-MaxCount-parametern.</span><span class="sxs-lookup"><span data-stu-id="63313-111">Returns list of queues for given namespace, By default 100 queues will be returned, if more than 100 queues to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="63313-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="63313-112">Example 3</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="63313-113">Returnerar en lista med de första 150-köerna för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="63313-113">Returns list of first 150 queues for given namespace</span></span>

## <span data-ttu-id="63313-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63313-114">PARAMETERS</span></span>

### <span data-ttu-id="63313-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63313-115">-DefaultProfile</span></span>
<span data-ttu-id="63313-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="63313-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63313-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="63313-117">-MaxCount</span></span>
<span data-ttu-id="63313-118">Bestämma det maximala antalet köer som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="63313-118">Determine the maximum number of Queues to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63313-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="63313-119">-Name</span></span>
<span data-ttu-id="63313-120">Könamn</span><span class="sxs-lookup"><span data-stu-id="63313-120">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63313-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="63313-121">-Namespace</span></span>
<span data-ttu-id="63313-122">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="63313-122">Namespace Name</span></span>

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

### <span data-ttu-id="63313-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63313-123">-ResourceGroupName</span></span>
<span data-ttu-id="63313-124">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="63313-124">The name of the resource group</span></span>

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

### <span data-ttu-id="63313-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63313-125">CommonParameters</span></span>
<span data-ttu-id="63313-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63313-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63313-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63313-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63313-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63313-128">INPUTS</span></span>

### <span data-ttu-id="63313-129">System. String</span><span class="sxs-lookup"><span data-stu-id="63313-129">System.String</span></span>

## <span data-ttu-id="63313-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63313-130">OUTPUTS</span></span>

### <span data-ttu-id="63313-131">Microsoft. Azure. commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="63313-131">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="63313-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63313-132">NOTES</span></span>

## <span data-ttu-id="63313-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63313-133">RELATED LINKS</span></span>
