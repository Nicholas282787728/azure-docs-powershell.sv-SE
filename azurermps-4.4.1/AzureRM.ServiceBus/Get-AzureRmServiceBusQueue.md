---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
ms.openlocfilehash: d90d93548e46f3586319b0acf96319fe24e298af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584539"
---
# <span data-ttu-id="fa05a-101">Get-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="fa05a-101">Get-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="fa05a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fa05a-102">SYNOPSIS</span></span>
<span data-ttu-id="fa05a-103">Returnerar en beskrivning för den angivna tjänst buss kön.</span><span class="sxs-lookup"><span data-stu-id="fa05a-103">Returns a description for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa05a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fa05a-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa05a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fa05a-105">DESCRIPTION</span></span>
<span data-ttu-id="fa05a-106">Cmdleten **Get-AzureRmServiceBusQueue** returnerar en beskrivning av den angivna tjänst buss kön.</span><span class="sxs-lookup"><span data-stu-id="fa05a-106">The **Get-AzureRmServiceBusQueue** cmdlet returns a description of the specified Service Bus queue.</span></span>

## <span data-ttu-id="fa05a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fa05a-107">EXAMPLES</span></span>

### <span data-ttu-id="fa05a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fa05a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1
```

<span data-ttu-id="fa05a-109">Returnerar beskrivningen av kön.</span><span class="sxs-lookup"><span data-stu-id="fa05a-109">Returns the description of the queue.</span></span> 

## <span data-ttu-id="fa05a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fa05a-110">PARAMETERS</span></span>

### <span data-ttu-id="fa05a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa05a-111">-DefaultProfile</span></span>
<span data-ttu-id="fa05a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fa05a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa05a-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="fa05a-113">-Name</span></span>
<span data-ttu-id="fa05a-114">Könamn.</span><span class="sxs-lookup"><span data-stu-id="fa05a-114">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa05a-115">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="fa05a-115">-Namespace</span></span>
<span data-ttu-id="fa05a-116">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="fa05a-116">Namespace Name.</span></span>

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

### <span data-ttu-id="fa05a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa05a-117">-ResourceGroupName</span></span>
<span data-ttu-id="fa05a-118">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="fa05a-118">The name of the resource group</span></span>

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

### <span data-ttu-id="fa05a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa05a-119">CommonParameters</span></span>
<span data-ttu-id="fa05a-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa05a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa05a-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa05a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa05a-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fa05a-122">INPUTS</span></span>

### <span data-ttu-id="fa05a-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fa05a-123">-ResourceGroup</span></span>
 <span data-ttu-id="fa05a-124">System. String</span><span class="sxs-lookup"><span data-stu-id="fa05a-124">System.String</span></span>
 

### <span data-ttu-id="fa05a-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="fa05a-125">-NamespaceName</span></span>
 <span data-ttu-id="fa05a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fa05a-126">System.String</span></span>
 

### <span data-ttu-id="fa05a-127">-QueueName</span><span class="sxs-lookup"><span data-stu-id="fa05a-127">-QueueName</span></span>
 <span data-ttu-id="fa05a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fa05a-128">System.String</span></span> 

## <span data-ttu-id="fa05a-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fa05a-129">OUTPUTS</span></span>

### <span data-ttu-id="fa05a-130">Microsoft. Azure. commands. ServiceBus. Models. QueueAttributes</span><span class="sxs-lookup"><span data-stu-id="fa05a-130">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>
<span data-ttu-id="fa05a-131">LockDuration: AccessedAt: 1/1/0001 12:00:00 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 2:51:35 AM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true DeadLetteringOnMessageExpiration: false EnableExpress: false EnablePartitioning: true IsAnonymousAccessible: false MaxDeliveryCount: MaxSizeInMegabytes: 16384 MessageCount: CountDetails: Microsoft. Azure. Management. ServiceBus. Models. MessageCountDetails RequiresDuplicateDetection: false RequiresSession: false SizeInBytes: status: Active SupportOrdering: false UpdatedAt: 1/20/2017 2:51:37 AM-ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/S B-Queue_example1 namn: SB-Queue_example1 typ: Microsoft. ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fa05a-131">LockDuration                        : AccessedAt                          : 1/1/0001 12:00:00 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 2:51:35 AM DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True DeadLetteringOnMessageExpiration    : False EnableExpress                       : False EnablePartitioning                  : True IsAnonymousAccessible               : False MaxDeliveryCount                    : MaxSizeInMegabytes                  : 16384 MessageCount                        : CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails RequiresDuplicateDetection          : False RequiresSession                     : False SizeInBytes                         : Status                              : Active SupportOrdering                     : False UpdatedAt                           : 1/20/2017 2:51:37 AM Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/S B-Queue_example1 Name                                : SB-Queue_example1 Type                                : Microsoft.ServiceBus/Queues Location                            : West US</span></span>

## <span data-ttu-id="fa05a-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fa05a-132">NOTES</span></span>

## <span data-ttu-id="fa05a-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fa05a-133">RELATED LINKS</span></span>

