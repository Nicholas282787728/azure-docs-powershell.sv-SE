---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 0e0f6a824571ab529daa576e5f3f9a4cbff08264
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574527"
---
# <span data-ttu-id="96723-101">Get-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="96723-101">Get-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="96723-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96723-102">SYNOPSIS</span></span>
<span data-ttu-id="96723-103">Returnerar en prenumerations beskrivning för det angivna ämnet.</span><span class="sxs-lookup"><span data-stu-id="96723-103">Returns a subscription description for the specified topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96723-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96723-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96723-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96723-105">DESCRIPTION</span></span>
<span data-ttu-id="96723-106">Cmdleten **Get-AzureRmServiceBusSubscription** returnerar en prenumerations beskrivning för den angivna tjänst Bus artikeln.</span><span class="sxs-lookup"><span data-stu-id="96723-106">The **Get-AzureRmServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="96723-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96723-107">EXAMPLES</span></span>

### <span data-ttu-id="96723-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="96723-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="96723-109">Returnerar en prenumerations beskrivning för den angivna tjänst Bus artikeln.</span><span class="sxs-lookup"><span data-stu-id="96723-109">Returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="96723-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96723-110">PARAMETERS</span></span>

### <span data-ttu-id="96723-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96723-111">-DefaultProfile</span></span>
<span data-ttu-id="96723-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="96723-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96723-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="96723-113">-Name</span></span>
<span data-ttu-id="96723-114">Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="96723-114">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96723-115">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="96723-115">-Namespace</span></span>
<span data-ttu-id="96723-116">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="96723-116">Namespace Name.</span></span>

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

### <span data-ttu-id="96723-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96723-117">-ResourceGroupName</span></span>
<span data-ttu-id="96723-118">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="96723-118">The name of the resource group</span></span>

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

### <span data-ttu-id="96723-119">-Ämne</span><span class="sxs-lookup"><span data-stu-id="96723-119">-Topic</span></span>
<span data-ttu-id="96723-120">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="96723-120">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96723-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96723-121">CommonParameters</span></span>
<span data-ttu-id="96723-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96723-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96723-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96723-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96723-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96723-124">INPUTS</span></span>

### <span data-ttu-id="96723-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="96723-125">-ResourceGroup</span></span>
 <span data-ttu-id="96723-126">System. String</span><span class="sxs-lookup"><span data-stu-id="96723-126">System.String</span></span>
 

### <span data-ttu-id="96723-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="96723-127">-NamespaceName</span></span>
 <span data-ttu-id="96723-128">System. String</span><span class="sxs-lookup"><span data-stu-id="96723-128">System.String</span></span>
 

### <span data-ttu-id="96723-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="96723-129">-TopicName</span></span>
 <span data-ttu-id="96723-130">System. String</span><span class="sxs-lookup"><span data-stu-id="96723-130">System.String</span></span>
 

### <span data-ttu-id="96723-131">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="96723-131">-SubscriptionName</span></span>
 <span data-ttu-id="96723-132">System. String</span><span class="sxs-lookup"><span data-stu-id="96723-132">System.String</span></span>
 

## <span data-ttu-id="96723-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96723-133">OUTPUTS</span></span>

### <span data-ttu-id="96723-134">Microsoft. Azure. commands. ServiceBus. Models. SubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="96723-134">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="96723-135">Namn: SB-TopicSubscription-Example1-plats: 1/20/2017 3:18:54 am AutoDeleteOnIdle: 10675199.02:48:05.4775807 CountDetails: Microsoft. Azure. Management. ServiceBus. MODELES. MessageCountDetails CreatedAt: 1/20/2017 3:18:52 AM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions: true DeadLetteringOnMessageExpiration: false EnableBatchedOperations: true EntityAvailabilityStatus: tillgänglig IsReadOnly: LockDuration: 00:01:00 MaxDeliveryCount: 10 MessageCount: 0 RequiresSession: false status: Active UpdatedAt: 1/20/2017 3:18:54 AM</span><span class="sxs-lookup"><span data-stu-id="96723-135">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails CreatedAt                                 : 1/20/2017 3:18:52 AM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : False EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 10 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 3:18:54 AM</span></span>

## <span data-ttu-id="96723-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96723-136">NOTES</span></span>

## <span data-ttu-id="96723-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96723-137">RELATED LINKS</span></span>

