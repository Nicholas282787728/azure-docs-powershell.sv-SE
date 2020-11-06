---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 166b47a231b2ca6fc2cf74137212e60123f25445
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584520"
---
# <span data-ttu-id="5388c-101">Set-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5388c-101">Set-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="5388c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5388c-102">SYNOPSIS</span></span>
<span data-ttu-id="5388c-103">Uppdaterar den angivna beskrivningen av auktoriseringsregeln för den angivna tjänst buss kön.</span><span class="sxs-lookup"><span data-stu-id="5388c-103">Updates the specified authorization rule description for the given Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5388c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5388c-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> [-NamespaceName] <String>
 [-QueueName] <String> [-AuthRuleObj] <SharedAccessAuthorizationRuleAttributes>
 [[-AuthorizationRuleName] <String>] [[-Rights] <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5388c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5388c-105">DESCRIPTION</span></span>
<span data-ttu-id="5388c-106">Cmdleten **set-AzureRmServiceBusQueueAuthorizationRule** uppdaterar beskrivningen för den angivna auktoriseringsregeln för den angivna tjänst buss kön.</span><span class="sxs-lookup"><span data-stu-id="5388c-106">The **Set-AzureRmServiceBusQueueAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Service Bus queue.</span></span>

## <span data-ttu-id="5388c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5388c-107">EXAMPLES</span></span>

### <span data-ttu-id="5388c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5388c-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1

PS C:\> $authRuleObj.Rights.Add("Manage")

PS C:\> Set-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="5388c-109">Lägger **till behörigheter för** behörighets reglerna för `SBAuthoRule1` kön `SB-Queue_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="5388c-109">Adds **Manage** to the access rights of the authorization rule `SBAuthoRule1` of the queue `SB-Queue_exampl1`.</span></span>

## <span data-ttu-id="5388c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5388c-110">PARAMETERS</span></span>

### <span data-ttu-id="5388c-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="5388c-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="5388c-112">Namn på auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="5388c-112">The authorization rule name.</span></span> <span data-ttu-id="5388c-113">Obligatoriskt om **-AuthruleObj** inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="5388c-113">Required if **-AuthruleObj** is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5388c-114">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="5388c-114">-AuthRuleObj</span></span>
<span data-ttu-id="5388c-115">Objektet för auktoriseringsregeln för Service Bus Queue.</span><span class="sxs-lookup"><span data-stu-id="5388c-115">The Service Bus queue authorization rule object.</span></span>

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5388c-116">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="5388c-116">-NamespaceName</span></span>
<span data-ttu-id="5388c-117">Namn på Service Bus-namnrymden.</span><span class="sxs-lookup"><span data-stu-id="5388c-117">The Service Bus namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5388c-118">-QueueName</span><span class="sxs-lookup"><span data-stu-id="5388c-118">-QueueName</span></span>
<span data-ttu-id="5388c-119">Namn på Service Bus-kön.</span><span class="sxs-lookup"><span data-stu-id="5388c-119">The Service Bus queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5388c-120">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5388c-120">-ResourceGroup</span></span>
<span data-ttu-id="5388c-121">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5388c-121">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5388c-122">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="5388c-122">-Rights</span></span>
<span data-ttu-id="5388c-123">Rättigheterna; till exempel @ ("lyssna", "Skicka", "hantera").</span><span class="sxs-lookup"><span data-stu-id="5388c-123">The rights; for example @("Listen","Send","Manage").</span></span> <span data-ttu-id="5388c-124">Obligatoriskt om ' AuthruleObj ' inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="5388c-124">Required if 'AuthruleObj' not specified.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5388c-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5388c-125">-Confirm</span></span>
<span data-ttu-id="5388c-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5388c-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5388c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5388c-127">-WhatIf</span></span>
<span data-ttu-id="5388c-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5388c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5388c-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5388c-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5388c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5388c-130">CommonParameters</span></span>
<span data-ttu-id="5388c-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5388c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5388c-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5388c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5388c-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5388c-133">INPUTS</span></span>

### <span data-ttu-id="5388c-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5388c-134">-ResourceGroup</span></span>
 <span data-ttu-id="5388c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5388c-135">System.String</span></span>

### <span data-ttu-id="5388c-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="5388c-136">-NamespaceName</span></span>
 <span data-ttu-id="5388c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5388c-137">System.String</span></span>

### <span data-ttu-id="5388c-138">-QueueName</span><span class="sxs-lookup"><span data-stu-id="5388c-138">-QueueName</span></span>
 <span data-ttu-id="5388c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5388c-139">System.String</span></span>

### <span data-ttu-id="5388c-140">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="5388c-140">-AuthRuleObj</span></span>
 <span data-ttu-id="5388c-141">Microsoft. Azure. commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="5388c-141">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="5388c-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5388c-142">OUTPUTS</span></span>

### <span data-ttu-id="5388c-143">Microsoft. Azure. commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="5388c-143">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="5388c-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5388c-144">NOTES</span></span>

## <span data-ttu-id="5388c-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5388c-145">RELATED LINKS</span></span>

