---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
ms.openlocfilehash: 22e54316bd38907c1ab22e3b2c35e1b6949b0034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756449"
---
# <span data-ttu-id="8c062-101">New-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="8c062-101">New-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="8c062-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8c062-102">SYNOPSIS</span></span>
<span data-ttu-id="8c062-103">Skapar en ny regel för ett givet abonnemang av ämnet.</span><span class="sxs-lookup"><span data-stu-id="8c062-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c062-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8c062-104">SYNTAX</span></span>

```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c062-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8c062-105">DESCRIPTION</span></span>
<span data-ttu-id="8c062-106">Cmdleten **New-AzureRmServiceBusRule** skapar en ny regel för angiven prenumeration.</span><span class="sxs-lookup"><span data-stu-id="8c062-106">The **New-AzureRmServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="8c062-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8c062-107">EXAMPLES</span></span>

### <span data-ttu-id="8c062-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8c062-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="8c062-109">New-AzureRmServiceBusRule cmdlet skapar en ny regel för det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8c062-109">The New-AzureRmServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

## <span data-ttu-id="8c062-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8c062-110">PARAMETERS</span></span>

### <span data-ttu-id="8c062-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c062-111">-DefaultProfile</span></span>
<span data-ttu-id="8c062-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8c062-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c062-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="8c062-113">-Name</span></span>
<span data-ttu-id="8c062-114">Regel namn</span><span class="sxs-lookup"><span data-stu-id="8c062-114">Rule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c062-115">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="8c062-115">-Namespace</span></span>
<span data-ttu-id="8c062-116">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="8c062-116">Namespace Name.</span></span>

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

### <span data-ttu-id="8c062-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c062-117">-ResourceGroupName</span></span>
<span data-ttu-id="8c062-118">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="8c062-118">The name of the resource group</span></span>

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

### <span data-ttu-id="8c062-119">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="8c062-119">-SqlExpression</span></span>
<span data-ttu-id="8c062-120">SQL filtrera-uttryck</span><span class="sxs-lookup"><span data-stu-id="8c062-120">Sql Fillter Expression</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c062-121">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="8c062-121">-Subscription</span></span>
<span data-ttu-id="8c062-122">Prenumerationens namn</span><span class="sxs-lookup"><span data-stu-id="8c062-122">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c062-123">-Ämne</span><span class="sxs-lookup"><span data-stu-id="8c062-123">-Topic</span></span>
<span data-ttu-id="8c062-124">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="8c062-124">Topic Name.</span></span>

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

### <span data-ttu-id="8c062-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8c062-125">-Confirm</span></span>
<span data-ttu-id="8c062-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8c062-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c062-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c062-127">-WhatIf</span></span>
<span data-ttu-id="8c062-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8c062-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c062-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8c062-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c062-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c062-130">CommonParameters</span></span>
<span data-ttu-id="8c062-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c062-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c062-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c062-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c062-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8c062-133">INPUTS</span></span>

### <span data-ttu-id="8c062-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8c062-134">System.String</span></span>

## <span data-ttu-id="8c062-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8c062-135">OUTPUTS</span></span>

### <span data-ttu-id="8c062-136">Microsoft. Azure. commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="8c062-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="8c062-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8c062-137">NOTES</span></span>

## <span data-ttu-id="8c062-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8c062-138">RELATED LINKS</span></span>

