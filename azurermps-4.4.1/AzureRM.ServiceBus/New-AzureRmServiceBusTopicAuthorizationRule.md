---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: 603eb1363e15b58a324f7131dd986a7c84371a89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755639"
---
# <span data-ttu-id="de84d-101">New-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="de84d-101">New-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="de84d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de84d-102">SYNOPSIS</span></span>
<span data-ttu-id="de84d-103">Skapar en ny auktoriseringsregel för den angivna tjänst Bus artikeln.</span><span class="sxs-lookup"><span data-stu-id="de84d-103">Creates a new authorization rule for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de84d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de84d-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -Name <String> [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de84d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de84d-105">DESCRIPTION</span></span>
<span data-ttu-id="de84d-106">Cmdleten **New-AzureRmServiceBusTopicAuthorizationRule** skapar en ny auktoriseringsregel för den angivna tjänst Bus artikeln.</span><span class="sxs-lookup"><span data-stu-id="de84d-106">The **New-AzureRmServiceBusTopicAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus topic.</span></span>

## <span data-ttu-id="de84d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de84d-107">EXAMPLES</span></span>

### <span data-ttu-id="de84d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="de84d-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="de84d-109">Skapar en auktoriseringsregel `SBTopicAuthoRule1` med **lyssnar** och **skickar** behörighet för ämnet `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="de84d-109">Creates authorization rule `SBTopicAuthoRule1` with **Listen** and **Send** rights for the topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="de84d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de84d-110">PARAMETERS</span></span>

### <span data-ttu-id="de84d-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="de84d-111">-ResourceGroup</span></span>
<span data-ttu-id="de84d-112">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="de84d-112">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de84d-113">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="de84d-113">-Rights</span></span>
<span data-ttu-id="de84d-114">Rättigheterna; till exempel @ ("lyssna", "Skicka", "hantera")</span><span class="sxs-lookup"><span data-stu-id="de84d-114">The rights; for example, @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de84d-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="de84d-115">-Confirm</span></span>
<span data-ttu-id="de84d-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="de84d-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de84d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de84d-117">-WhatIf</span></span>
<span data-ttu-id="de84d-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="de84d-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de84d-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="de84d-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de84d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de84d-120">-DefaultProfile</span></span>
<span data-ttu-id="de84d-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="de84d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de84d-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="de84d-122">-Name</span></span>
<span data-ttu-id="de84d-123">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="de84d-123">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de84d-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="de84d-124">-Namespace</span></span>
<span data-ttu-id="de84d-125">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="de84d-125">Namespace Name.</span></span>

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

### <span data-ttu-id="de84d-126">-Ämne</span><span class="sxs-lookup"><span data-stu-id="de84d-126">-Topic</span></span>
<span data-ttu-id="de84d-127">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="de84d-127">Topic Name.</span></span>

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

### <span data-ttu-id="de84d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de84d-128">CommonParameters</span></span>
<span data-ttu-id="de84d-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de84d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de84d-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de84d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de84d-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de84d-131">INPUTS</span></span>

### <span data-ttu-id="de84d-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="de84d-132">-ResourceGroup</span></span>
 <span data-ttu-id="de84d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="de84d-133">System.String</span></span>
 

### <span data-ttu-id="de84d-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="de84d-134">-NamespaceName</span></span>
 <span data-ttu-id="de84d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="de84d-135">System.String</span></span>
 

### <span data-ttu-id="de84d-136">-TopicName</span><span class="sxs-lookup"><span data-stu-id="de84d-136">-TopicName</span></span>
 <span data-ttu-id="de84d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="de84d-137">System.String</span></span>
 

### <span data-ttu-id="de84d-138">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="de84d-138">-AuthorizationRuleName</span></span>
 <span data-ttu-id="de84d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="de84d-139">System.String</span></span>

## <span data-ttu-id="de84d-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de84d-140">OUTPUTS</span></span>

### <span data-ttu-id="de84d-141">Microsoft. Azure. commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="de84d-141">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="de84d-142">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorizati onRules/SBTopicAuthoRule1 Skriv: Microsoft. ServiceBus/AuthorizationRules namn: SBTopicAuthoRule1 plats: West US-Taggar: rättigheter: {avlyssna, skicka}</span><span class="sxs-lookup"><span data-stu-id="de84d-142">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorizati onRules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="de84d-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de84d-143">NOTES</span></span>

## <span data-ttu-id="de84d-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de84d-144">RELATED LINKS</span></span>

