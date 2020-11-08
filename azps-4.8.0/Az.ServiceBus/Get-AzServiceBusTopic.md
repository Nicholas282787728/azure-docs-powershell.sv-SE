---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
ms.openlocfilehash: 3d688362932f61bdea9d685b98f2cba757288da2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261050"
---
# <span data-ttu-id="5c792-101">Get-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="5c792-101">Get-AzServiceBusTopic</span></span>

## <span data-ttu-id="5c792-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5c792-102">SYNOPSIS</span></span>
<span data-ttu-id="5c792-103">Returnerar en beskrivning för den angivna tjänst Bus artikeln.</span><span class="sxs-lookup"><span data-stu-id="5c792-103">Returns a description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="5c792-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5c792-104">SYNTAX</span></span>

```
Get-AzServiceBusTopic [-ResourceGroupName <String>] [-Namespace <String>] [-Name <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c792-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5c792-105">DESCRIPTION</span></span>
<span data-ttu-id="5c792-106">Cmdleten **Get-AzServiceBusTopic** returnerar en beskrivning för det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="5c792-106">The **Get-AzServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="5c792-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5c792-107">EXAMPLES</span></span>

### <span data-ttu-id="5c792-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5c792-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 11:51:24 PM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : True
UpdatedAt                           : 10/11/2018 11:51:24 PM
```

<span data-ttu-id="5c792-109">Returnerar beskrivningen av angivet avsnitt för angivet Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="5c792-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

### <span data-ttu-id="5c792-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5c792-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="5c792-111">Returnerar en lista med ämnen för angivet Service Bus-namnrymd.</span><span class="sxs-lookup"><span data-stu-id="5c792-111">Returns list of topics for given Service Bus namespace.</span></span> <span data-ttu-id="5c792-112">Som standard returneras 100-avsnitt, om fler än 100 ämnen returneras, Använd-MaxCount-parameter.</span><span class="sxs-lookup"><span data-stu-id="5c792-112">By default 100 topics will be returned, if more than 100 topics to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="5c792-113">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="5c792-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="5c792-114">Returnerar en lista med de första 150-avsnitten för angivet Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="5c792-114">Returns list of first 150 topics for given Service Bus namespace.</span></span>

## <span data-ttu-id="5c792-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5c792-115">PARAMETERS</span></span>

### <span data-ttu-id="5c792-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c792-116">-DefaultProfile</span></span>
<span data-ttu-id="5c792-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5c792-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c792-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="5c792-118">-MaxCount</span></span>
<span data-ttu-id="5c792-119">Avgöra hur många avsnitt som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="5c792-119">Determine the maximum number of Topics to return.</span></span>

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

### <span data-ttu-id="5c792-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="5c792-120">-Name</span></span>
<span data-ttu-id="5c792-121">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="5c792-121">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c792-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="5c792-122">-Namespace</span></span>
<span data-ttu-id="5c792-123">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="5c792-123">Namespace Name</span></span>

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

### <span data-ttu-id="5c792-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c792-124">-ResourceGroupName</span></span>
<span data-ttu-id="5c792-125">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="5c792-125">The name of the resource group</span></span>

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

### <span data-ttu-id="5c792-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c792-126">CommonParameters</span></span>
<span data-ttu-id="5c792-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c792-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c792-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c792-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c792-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5c792-129">INPUTS</span></span>

### <span data-ttu-id="5c792-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5c792-130">System.String</span></span>

## <span data-ttu-id="5c792-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5c792-131">OUTPUTS</span></span>

### <span data-ttu-id="5c792-132">Microsoft. Azure. commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="5c792-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="5c792-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5c792-133">NOTES</span></span>

## <span data-ttu-id="5c792-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5c792-134">RELATED LINKS</span></span>
