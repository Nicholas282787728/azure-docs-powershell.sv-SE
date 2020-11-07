---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
ms.openlocfilehash: 2d249d8935b79c310e4ca0aa1270ee67bf33ece3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756129"
---
# <span data-ttu-id="fcc3c-101">Get-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="fcc3c-101">Get-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="fcc3c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fcc3c-102">SYNOPSIS</span></span>
<span data-ttu-id="fcc3c-103">Skapar en ny regel för ett givet abonnemang av ämnet.</span><span class="sxs-lookup"><span data-stu-id="fcc3c-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcc3c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fcc3c-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fcc3c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fcc3c-105">DESCRIPTION</span></span>
<span data-ttu-id="fcc3c-106">Cmdleten **Get-AzureRmServiceBusRule** hämtar beskrivningen av den angivna regeln i det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="fcc3c-106">The **Get-AzureRmServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="fcc3c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fcc3c-107">EXAMPLES</span></span>

### <span data-ttu-id="fcc3c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fcc3c-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="fcc3c-109">Returnerar den angivna regel beskrivningen för en angiven prenumeration.</span><span class="sxs-lookup"><span data-stu-id="fcc3c-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="fcc3c-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="fcc3c-110">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="fcc3c-111">Returnerar en lista med regel beskrivningar för en angiven prenumeration.</span><span class="sxs-lookup"><span data-stu-id="fcc3c-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="fcc3c-112">Standard regeln för 100 kommer att returneras, om fler än 100-regeln returneras, Använd-MaxCount-parametern.</span><span class="sxs-lookup"><span data-stu-id="fcc3c-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="fcc3c-113">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="fcc3c-113">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="fcc3c-114">Returnerar en lista med de första regel beskrivningarna för 150 för en viss prenumeration.</span><span class="sxs-lookup"><span data-stu-id="fcc3c-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="fcc3c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fcc3c-115">PARAMETERS</span></span>

### <span data-ttu-id="fcc3c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcc3c-116">-DefaultProfile</span></span>
<span data-ttu-id="fcc3c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fcc3c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcc3c-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="fcc3c-118">-MaxCount</span></span>
<span data-ttu-id="fcc3c-119">Ange det maximala antalet regler som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="fcc3c-119">Determine the maximum number of Rules to return.</span></span>

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

### <span data-ttu-id="fcc3c-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="fcc3c-120">-Name</span></span>
<span data-ttu-id="fcc3c-121">Regel namn</span><span class="sxs-lookup"><span data-stu-id="fcc3c-121">Rule Name</span></span>

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

### <span data-ttu-id="fcc3c-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="fcc3c-122">-Namespace</span></span>
<span data-ttu-id="fcc3c-123">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="fcc3c-123">Namespace Name</span></span>

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

### <span data-ttu-id="fcc3c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcc3c-124">-ResourceGroupName</span></span>
<span data-ttu-id="fcc3c-125">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="fcc3c-125">The name of the resource group</span></span>

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

### <span data-ttu-id="fcc3c-126">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="fcc3c-126">-Subscription</span></span>
<span data-ttu-id="fcc3c-127">Prenumerationens namn</span><span class="sxs-lookup"><span data-stu-id="fcc3c-127">Subscription Name</span></span>

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

### <span data-ttu-id="fcc3c-128">-Ämne</span><span class="sxs-lookup"><span data-stu-id="fcc3c-128">-Topic</span></span>
<span data-ttu-id="fcc3c-129">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="fcc3c-129">Topic Name</span></span>

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

### <span data-ttu-id="fcc3c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcc3c-130">CommonParameters</span></span>
<span data-ttu-id="fcc3c-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcc3c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcc3c-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcc3c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcc3c-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fcc3c-133">INPUTS</span></span>

### <span data-ttu-id="fcc3c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fcc3c-134">System.String</span></span>

## <span data-ttu-id="fcc3c-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fcc3c-135">OUTPUTS</span></span>

### <span data-ttu-id="fcc3c-136">Microsoft. Azure. commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="fcc3c-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="fcc3c-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fcc3c-137">NOTES</span></span>

## <span data-ttu-id="fcc3c-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fcc3c-138">RELATED LINKS</span></span>
