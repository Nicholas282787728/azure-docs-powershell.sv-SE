---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
ms.openlocfilehash: 0f765f8cf59453ee8b89317da2fa123785ee7f90
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100847"
---
# <span data-ttu-id="502b0-101">Get-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="502b0-101">Get-AzServiceBusRule</span></span>

## <span data-ttu-id="502b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="502b0-102">SYNOPSIS</span></span>
<span data-ttu-id="502b0-103">Hämtar definitionen av en befintlig regel i ett angivet abonnemang av ämnet.</span><span class="sxs-lookup"><span data-stu-id="502b0-103">Retrieves the definition of an existing rule in a given Subscription of Topic.</span></span> 

## <span data-ttu-id="502b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="502b0-104">SYNTAX</span></span>

```
Get-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="502b0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="502b0-105">DESCRIPTION</span></span>
<span data-ttu-id="502b0-106">Cmdleten **Get-AzServiceBusRule** hämtar beskrivningen av den angivna regeln i det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="502b0-106">The **Get-AzServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="502b0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="502b0-107">EXAMPLES</span></span>

### <span data-ttu-id="502b0-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="502b0-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="502b0-109">Returnerar den angivna regel beskrivningen för en angiven prenumeration.</span><span class="sxs-lookup"><span data-stu-id="502b0-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="502b0-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="502b0-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="502b0-111">Returnerar en lista med regel beskrivningar för en angiven prenumeration.</span><span class="sxs-lookup"><span data-stu-id="502b0-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="502b0-112">Standard regeln för 100 kommer att returneras, om fler än 100-regeln returneras, Använd-MaxCount-parametern.</span><span class="sxs-lookup"><span data-stu-id="502b0-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="502b0-113">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="502b0-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="502b0-114">Returnerar en lista med de första regel beskrivningarna för 150 för en viss prenumeration.</span><span class="sxs-lookup"><span data-stu-id="502b0-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="502b0-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="502b0-115">PARAMETERS</span></span>

### <span data-ttu-id="502b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="502b0-116">-DefaultProfile</span></span>
<span data-ttu-id="502b0-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="502b0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="502b0-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="502b0-118">-MaxCount</span></span>
<span data-ttu-id="502b0-119">Ange det maximala antalet regler som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="502b0-119">Determine the maximum number of Rules to return.</span></span>

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

### <span data-ttu-id="502b0-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="502b0-120">-Name</span></span>
<span data-ttu-id="502b0-121">Regel namn</span><span class="sxs-lookup"><span data-stu-id="502b0-121">Rule Name</span></span>

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

### <span data-ttu-id="502b0-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="502b0-122">-Namespace</span></span>
<span data-ttu-id="502b0-123">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="502b0-123">Namespace Name</span></span>

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

### <span data-ttu-id="502b0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="502b0-124">-ResourceGroupName</span></span>
<span data-ttu-id="502b0-125">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="502b0-125">The name of the resource group</span></span>

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

### <span data-ttu-id="502b0-126">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="502b0-126">-Subscription</span></span>
<span data-ttu-id="502b0-127">Prenumerationens namn</span><span class="sxs-lookup"><span data-stu-id="502b0-127">Subscription Name</span></span>

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

### <span data-ttu-id="502b0-128">-Ämne</span><span class="sxs-lookup"><span data-stu-id="502b0-128">-Topic</span></span>
<span data-ttu-id="502b0-129">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="502b0-129">Topic Name</span></span>

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

### <span data-ttu-id="502b0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="502b0-130">CommonParameters</span></span>
<span data-ttu-id="502b0-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="502b0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="502b0-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="502b0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="502b0-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="502b0-133">INPUTS</span></span>

### <span data-ttu-id="502b0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="502b0-134">System.String</span></span>

## <span data-ttu-id="502b0-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="502b0-135">OUTPUTS</span></span>

### <span data-ttu-id="502b0-136">Microsoft. Azure. commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="502b0-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="502b0-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="502b0-137">NOTES</span></span>

## <span data-ttu-id="502b0-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="502b0-138">RELATED LINKS</span></span>