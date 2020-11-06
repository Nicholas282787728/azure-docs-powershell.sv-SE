---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 3d99b261dc65af5d19a93acb575116a91c8a97fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583011"
---
# <span data-ttu-id="6efe3-101">Get-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="6efe3-101">Get-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="6efe3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6efe3-102">SYNOPSIS</span></span>
<span data-ttu-id="6efe3-103">Returnerar en prenumerations beskrivning för det angivna ämnet.</span><span class="sxs-lookup"><span data-stu-id="6efe3-103">Returns a subscription description for the specified topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6efe3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6efe3-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6efe3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6efe3-105">DESCRIPTION</span></span>
<span data-ttu-id="6efe3-106">Cmdleten **Get-AzureRmServiceBusSubscription** returnerar en prenumerations beskrivning för den angivna tjänst Bus artikeln.</span><span class="sxs-lookup"><span data-stu-id="6efe3-106">The **Get-AzureRmServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="6efe3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6efe3-107">EXAMPLES</span></span>

### <span data-ttu-id="6efe3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6efe3-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

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

<span data-ttu-id="6efe3-109">Returnerar en prenumerations beskrivning för den angivna tjänst Bus artikeln.</span><span class="sxs-lookup"><span data-stu-id="6efe3-109">Returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="6efe3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6efe3-110">PARAMETERS</span></span>

### <span data-ttu-id="6efe3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6efe3-111">-DefaultProfile</span></span>
<span data-ttu-id="6efe3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6efe3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6efe3-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="6efe3-113">-Name</span></span>
<span data-ttu-id="6efe3-114">Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="6efe3-114">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6efe3-115">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="6efe3-115">-Namespace</span></span>
<span data-ttu-id="6efe3-116">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="6efe3-116">Namespace Name.</span></span>

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

### <span data-ttu-id="6efe3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6efe3-117">-ResourceGroupName</span></span>
<span data-ttu-id="6efe3-118">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="6efe3-118">The name of the resource group</span></span>

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

### <span data-ttu-id="6efe3-119">-Ämne</span><span class="sxs-lookup"><span data-stu-id="6efe3-119">-Topic</span></span>
<span data-ttu-id="6efe3-120">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="6efe3-120">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6efe3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6efe3-121">CommonParameters</span></span>
<span data-ttu-id="6efe3-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6efe3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6efe3-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6efe3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6efe3-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6efe3-124">INPUTS</span></span>

### <span data-ttu-id="6efe3-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6efe3-125">-ResourceGroup</span></span>
 <span data-ttu-id="6efe3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6efe3-126">System.String</span></span>
 

### <span data-ttu-id="6efe3-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="6efe3-127">-NamespaceName</span></span>
 <span data-ttu-id="6efe3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6efe3-128">System.String</span></span>
 

### <span data-ttu-id="6efe3-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="6efe3-129">-TopicName</span></span>
 <span data-ttu-id="6efe3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6efe3-130">System.String</span></span>
 

### <span data-ttu-id="6efe3-131">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="6efe3-131">-SubscriptionName</span></span>
 <span data-ttu-id="6efe3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6efe3-132">System.String</span></span>
 

## <span data-ttu-id="6efe3-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6efe3-133">OUTPUTS</span></span>

### <span data-ttu-id="6efe3-134">Microsoft. Azure. commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="6efe3-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="6efe3-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6efe3-135">NOTES</span></span>

## <span data-ttu-id="6efe3-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6efe3-136">RELATED LINKS</span></span>

