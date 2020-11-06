---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
ms.openlocfilehash: 273a8ec4bcbf5ffcc7619d3fe663d6256e4851d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574523"
---
# <span data-ttu-id="59ad6-101">Get-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="59ad6-101">Get-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="59ad6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59ad6-102">SYNOPSIS</span></span>
<span data-ttu-id="59ad6-103">Returnerar en beskrivning för den angivna tjänst Bus artikeln.</span><span class="sxs-lookup"><span data-stu-id="59ad6-103">Returns a description for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59ad6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59ad6-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59ad6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59ad6-105">DESCRIPTION</span></span>
<span data-ttu-id="59ad6-106">Cmdleten **Get-AzureRmServiceBusTopic** returnerar en beskrivning för det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="59ad6-106">The **Get-AzureRmServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="59ad6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59ad6-107">EXAMPLES</span></span>

### <span data-ttu-id="59ad6-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="59ad6-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="59ad6-109">Returnerar beskrivningen av angivet avsnitt för angivet Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="59ad6-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

## <span data-ttu-id="59ad6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59ad6-110">PARAMETERS</span></span>

### <span data-ttu-id="59ad6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59ad6-111">-DefaultProfile</span></span>
<span data-ttu-id="59ad6-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="59ad6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59ad6-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="59ad6-113">-Name</span></span>
<span data-ttu-id="59ad6-114">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="59ad6-114">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59ad6-115">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="59ad6-115">-Namespace</span></span>
<span data-ttu-id="59ad6-116">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="59ad6-116">Namespace Name.</span></span>

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

### <span data-ttu-id="59ad6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59ad6-117">-ResourceGroupName</span></span>
<span data-ttu-id="59ad6-118">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="59ad6-118">The name of the resource group</span></span>

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

### <span data-ttu-id="59ad6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59ad6-119">CommonParameters</span></span>
<span data-ttu-id="59ad6-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59ad6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59ad6-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59ad6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59ad6-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59ad6-122">INPUTS</span></span>

### <span data-ttu-id="59ad6-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="59ad6-123">-ResourceGroup</span></span>
 <span data-ttu-id="59ad6-124">System. String</span><span class="sxs-lookup"><span data-stu-id="59ad6-124">System.String</span></span>
 

### <span data-ttu-id="59ad6-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="59ad6-125">-NamespaceName</span></span>
 <span data-ttu-id="59ad6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="59ad6-126">System.String</span></span>
 

### <span data-ttu-id="59ad6-127">-TopicName</span><span class="sxs-lookup"><span data-stu-id="59ad6-127">-TopicName</span></span>
 <span data-ttu-id="59ad6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="59ad6-128">System.String</span></span>

## <span data-ttu-id="59ad6-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59ad6-129">OUTPUTS</span></span>

### <span data-ttu-id="59ad6-130">Microsoft. Azure. commands. ServiceBus. Models. TopicAttributes</span><span class="sxs-lookup"><span data-stu-id="59ad6-130">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>
<span data-ttu-id="59ad6-131">Namn: SB-Topic_exampl1 plats: West US ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 typ: Microsoft. ServiceBus/topic AccessedAt: 1/20/2017 3:18:54 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 3:16:41 AM CountDetails: Microsoft. Azure. Management. ServiceBus. Models. MessageCountDetails DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true EnableExpress: falskt EnablePartitioning: true EnableSubscriptionPartitioning: falskt FilteringMessagesBeforePublishing: false IsAnonymousAccessible: falskt IsExpress: falskt MaxSizeInMegabytes: 16384 RequiresDuplicateDetection: falskt SizeInBytes: 0 status: aktiv SubscriptionCount: 1 SupportOrdering: false UpdatedAt: 1/20/2017 3:16:43 AM</span><span class="sxs-lookup"><span data-stu-id="59ad6-131">Name                                : SB-Topic_exampl1 Location                            : West US Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 Type                                : Microsoft.ServiceBus/Topic AccessedAt                          : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 3:16:41 AM CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True EnableExpress                       : False EnablePartitioning                  : True EnableSubscriptionPartitioning      : False FilteringMessagesBeforePublishing   : False IsAnonymousAccessible               : False IsExpress                           : False MaxSizeInMegabytes                  : 16384 RequiresDuplicateDetection          : False SizeInBytes                         : 0 Status                              : Active SubscriptionCount                   : 1 SupportOrdering                     : False UpdatedAt                           : 1/20/2017 3:16:43 AM</span></span>

## <span data-ttu-id="59ad6-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59ad6-132">NOTES</span></span>

## <span data-ttu-id="59ad6-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59ad6-133">RELATED LINKS</span></span>

