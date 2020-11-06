---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
ms.openlocfilehash: 3eb629665f8bc4ed030b5c616410fb47455136e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583012"
---
# <span data-ttu-id="8874e-101">Get-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="8874e-101">Get-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="8874e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8874e-102">SYNOPSIS</span></span>
<span data-ttu-id="8874e-103">Hämtar en beskrivning av den angivna regeln för ett givet abonnemang av ämnet.</span><span class="sxs-lookup"><span data-stu-id="8874e-103">Gets a description of the specified rule for a given Subscription of  Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8874e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8874e-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8874e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8874e-105">DESCRIPTION</span></span>
<span data-ttu-id="8874e-106">Cmdleten **Get-AzureRmServiceBusRule** hämtar beskrivningen av den angivna regeln i det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8874e-106">The **Get-AzureRmServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="8874e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8874e-107">EXAMPLES</span></span>

### <span data-ttu-id="8874e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8874e-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -NAme SBRule
```

<span data-ttu-id="8874e-109">Returnerar den angivna regel beskrivningen för en angiven prenumeration.</span><span class="sxs-lookup"><span data-stu-id="8874e-109">Returns the specified rule description for a specified subscription.</span></span>

## <span data-ttu-id="8874e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8874e-110">PARAMETERS</span></span>

### <span data-ttu-id="8874e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8874e-111">-DefaultProfile</span></span>
<span data-ttu-id="8874e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8874e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8874e-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="8874e-113">-Name</span></span>
<span data-ttu-id="8874e-114">Regel namn.</span><span class="sxs-lookup"><span data-stu-id="8874e-114">Rule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8874e-115">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="8874e-115">-Namespace</span></span>
<span data-ttu-id="8874e-116">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="8874e-116">Namespace Name.</span></span>

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

### <span data-ttu-id="8874e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8874e-117">-ResourceGroupName</span></span>
<span data-ttu-id="8874e-118">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="8874e-118">The name of the resource group</span></span>

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

### <span data-ttu-id="8874e-119">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="8874e-119">-Subscription</span></span>
<span data-ttu-id="8874e-120">Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="8874e-120">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8874e-121">-Ämne</span><span class="sxs-lookup"><span data-stu-id="8874e-121">-Topic</span></span>
<span data-ttu-id="8874e-122">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="8874e-122">Topic Name.</span></span>

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

### <span data-ttu-id="8874e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8874e-123">CommonParameters</span></span>
<span data-ttu-id="8874e-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8874e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8874e-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8874e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8874e-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8874e-126">INPUTS</span></span>

### <span data-ttu-id="8874e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8874e-127">System.String</span></span>

## <span data-ttu-id="8874e-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8874e-128">OUTPUTS</span></span>

### <span data-ttu-id="8874e-129">Microsoft. Azure. commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="8874e-129">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="8874e-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8874e-130">NOTES</span></span>

## <span data-ttu-id="8874e-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8874e-131">RELATED LINKS</span></span>

