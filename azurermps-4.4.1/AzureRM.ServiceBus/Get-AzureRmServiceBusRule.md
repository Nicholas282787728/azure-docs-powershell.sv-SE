---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
ms.openlocfilehash: e09e4f19a63eef1cd4b87760239d4456afee70fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574526"
---
# <span data-ttu-id="6dac3-101">Get-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="6dac3-101">Get-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="6dac3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6dac3-102">SYNOPSIS</span></span>
<span data-ttu-id="6dac3-103">Hämtar en beskrivning av den angivna regeln för ett givet abonnemang av ämnet.</span><span class="sxs-lookup"><span data-stu-id="6dac3-103">Gets a description of the specified rule for a given Subscription of  Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6dac3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6dac3-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dac3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6dac3-105">DESCRIPTION</span></span>
<span data-ttu-id="6dac3-106">Cmdleten **Get-AzureRmServiceBusRule** hämtar beskrivningen av den angivna regeln i det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6dac3-106">The **Get-AzureRmServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="6dac3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6dac3-107">EXAMPLES</span></span>

### <span data-ttu-id="6dac3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6dac3-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -NAme SBRule
```

<span data-ttu-id="6dac3-109">Returnerar den angivna regel beskrivningen för en angiven prenumeration.</span><span class="sxs-lookup"><span data-stu-id="6dac3-109">Returns the specified rule description for a specified subscription.</span></span>

## <span data-ttu-id="6dac3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6dac3-110">PARAMETERS</span></span>

### <span data-ttu-id="6dac3-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="6dac3-111">-Name</span></span>
<span data-ttu-id="6dac3-112">Regel namn.</span><span class="sxs-lookup"><span data-stu-id="6dac3-112">Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dac3-113">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="6dac3-113">-Namespace</span></span>
<span data-ttu-id="6dac3-114">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="6dac3-114">Namespace Name.</span></span>

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

### <span data-ttu-id="6dac3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dac3-115">-ResourceGroupName</span></span>
<span data-ttu-id="6dac3-116">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="6dac3-116">The name of the resource group</span></span>

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

### <span data-ttu-id="6dac3-117">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="6dac3-117">-Subscription</span></span>
<span data-ttu-id="6dac3-118">Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="6dac3-118">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dac3-119">-Ämne</span><span class="sxs-lookup"><span data-stu-id="6dac3-119">-Topic</span></span>
<span data-ttu-id="6dac3-120">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="6dac3-120">Topic Name.</span></span>

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

### <span data-ttu-id="6dac3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dac3-121">-DefaultProfile</span></span>
<span data-ttu-id="6dac3-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6dac3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6dac3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dac3-123">CommonParameters</span></span>
<span data-ttu-id="6dac3-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dac3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dac3-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dac3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dac3-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6dac3-126">INPUTS</span></span>

### <span data-ttu-id="6dac3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6dac3-127">System.String</span></span>

## <span data-ttu-id="6dac3-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6dac3-128">OUTPUTS</span></span>

### <span data-ttu-id="6dac3-129">Microsoft. Azure. commands. ServiceBus. Models. RulesAttributes</span><span class="sxs-lookup"><span data-stu-id="6dac3-129">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>

## <span data-ttu-id="6dac3-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6dac3-130">NOTES</span></span>

## <span data-ttu-id="6dac3-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6dac3-131">RELATED LINKS</span></span>

