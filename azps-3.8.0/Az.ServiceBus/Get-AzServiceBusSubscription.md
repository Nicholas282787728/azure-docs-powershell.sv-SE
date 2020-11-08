---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
ms.openlocfilehash: a2a535dd9607b3018b7fe215f152bbeeb01b8858
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091462"
---
# <span data-ttu-id="e0d83-101">Get-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="e0d83-101">Get-AzServiceBusSubscription</span></span>

## <span data-ttu-id="e0d83-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0d83-102">SYNOPSIS</span></span>
<span data-ttu-id="e0d83-103">Returnerar en prenumerations beskrivning för det angivna ämnet.</span><span class="sxs-lookup"><span data-stu-id="e0d83-103">Returns a subscription description for the specified topic.</span></span>

## <span data-ttu-id="e0d83-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0d83-104">SYNTAX</span></span>

```
Get-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0d83-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0d83-105">DESCRIPTION</span></span>
<span data-ttu-id="e0d83-106">Cmdleten **Get-AzServiceBusSubscription** returnerar en prenumerations beskrivning för den angivna tjänst Bus artikeln.</span><span class="sxs-lookup"><span data-stu-id="e0d83-106">The **Get-AzServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="e0d83-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0d83-107">EXAMPLES</span></span>

### <span data-ttu-id="e0d83-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e0d83-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
CreatedAt                                 : 1/20/2017 3:18:52 AM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : False
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 10
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 3:18:54 AM
```

<span data-ttu-id="e0d83-109">Returnerar en prenumerations beskrivning för den angivna tjänst Bus artikeln.</span><span class="sxs-lookup"><span data-stu-id="e0d83-109">Returns a subscription description for the specified Service Bus topic.</span></span>

### <span data-ttu-id="e0d83-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="e0d83-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="e0d83-111">Returnerar en lista med abonnemang för angiven Service Bus-ämne.</span><span class="sxs-lookup"><span data-stu-id="e0d83-111">Returns list of subscriptions for specified Service Bus topic.</span></span> <span data-ttu-id="e0d83-112">Som standard returnerar 100 abonnemang, för antal prenumerationer: Använd-MaxCount parameter</span><span class="sxs-lookup"><span data-stu-id="e0d83-112">By default 100 subscriptions will be returned, for number of subscriptions please use -MaxCount Parameter</span></span>

### <span data-ttu-id="e0d83-113">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="e0d83-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -MaxCount 150
```

<span data-ttu-id="e0d83-114">Returnerar en lista med de första 150-prenumerationerna för angivet Service Bus-ämne.</span><span class="sxs-lookup"><span data-stu-id="e0d83-114">Returns list of first 150 subscriptions for specified Service Bus topic.</span></span>

## <span data-ttu-id="e0d83-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0d83-115">PARAMETERS</span></span>

### <span data-ttu-id="e0d83-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0d83-116">-DefaultProfile</span></span>
<span data-ttu-id="e0d83-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e0d83-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0d83-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e0d83-118">-MaxCount</span></span>
<span data-ttu-id="e0d83-119">Fastställ det maximala antalet prenumerationer som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="e0d83-119">Determine the maximum number of Subscriptions to return.</span></span>

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

### <span data-ttu-id="e0d83-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="e0d83-120">-Name</span></span>
<span data-ttu-id="e0d83-121">Prenumerationens namn</span><span class="sxs-lookup"><span data-stu-id="e0d83-121">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d83-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="e0d83-122">-Namespace</span></span>
<span data-ttu-id="e0d83-123">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="e0d83-123">Namespace Name</span></span>

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

### <span data-ttu-id="e0d83-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0d83-124">-ResourceGroupName</span></span>
<span data-ttu-id="e0d83-125">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="e0d83-125">The name of the resource group</span></span>

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

### <span data-ttu-id="e0d83-126">-Ämne</span><span class="sxs-lookup"><span data-stu-id="e0d83-126">-Topic</span></span>
<span data-ttu-id="e0d83-127">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="e0d83-127">Topic Name</span></span>

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

### <span data-ttu-id="e0d83-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0d83-128">CommonParameters</span></span>
<span data-ttu-id="e0d83-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0d83-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0d83-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0d83-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0d83-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0d83-131">INPUTS</span></span>

### <span data-ttu-id="e0d83-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e0d83-132">System.String</span></span>

## <span data-ttu-id="e0d83-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0d83-133">OUTPUTS</span></span>

### <span data-ttu-id="e0d83-134">Microsoft. Azure. commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="e0d83-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="e0d83-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0d83-135">NOTES</span></span>

## <span data-ttu-id="e0d83-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0d83-136">RELATED LINKS</span></span>
