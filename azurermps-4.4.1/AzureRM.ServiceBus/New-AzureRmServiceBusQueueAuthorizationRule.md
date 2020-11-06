---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 098c61be4eaf405d3c3a031601b48f20de1e234a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574517"
---
# <span data-ttu-id="9b01a-101">New-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9b01a-101">New-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="9b01a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b01a-102">SYNOPSIS</span></span>
<span data-ttu-id="9b01a-103">Skapar en ny auktoriseringsregel för den angivna tjänst buss kön.</span><span class="sxs-lookup"><span data-stu-id="9b01a-103">Creates a new authorization rule for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b01a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b01a-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 -Name <String> [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b01a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b01a-105">DESCRIPTION</span></span>
<span data-ttu-id="9b01a-106">Cmdleten **New-AzureRmServiceBusQueueAuthorizationRule** skapar en ny auktoriseringsregel för den angivna tjänst buss kön.</span><span class="sxs-lookup"><span data-stu-id="9b01a-106">The **New-AzureRmServiceBusQueueAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus queue.</span></span>

## <span data-ttu-id="9b01a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b01a-107">EXAMPLES</span></span>

### <span data-ttu-id="9b01a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9b01a-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="9b01a-109">Skapar en auktoriseringsregel `SBAuthoRule1` med behörigheten **lyssna och skicka** för kön `SB-Queue_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="9b01a-109">Creates authorization rule `SBAuthoRule1` with **Listen and Send** rights for the queue `SB-Queue_exampl1`.</span></span>

## <span data-ttu-id="9b01a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b01a-110">PARAMETERS</span></span>

### <span data-ttu-id="9b01a-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9b01a-111">-ResourceGroup</span></span>
<span data-ttu-id="9b01a-112">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9b01a-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="9b01a-113">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="9b01a-113">-Rights</span></span>
<span data-ttu-id="9b01a-114">Anger rättigheterna; till exempel:</span><span class="sxs-lookup"><span data-stu-id="9b01a-114">Specifies the rights; for example,</span></span>  
<span data-ttu-id="9b01a-115">@ ("Lyssna", "Skicka", "hantera")</span><span class="sxs-lookup"><span data-stu-id="9b01a-115">@("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="9b01a-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9b01a-116">-Confirm</span></span>
<span data-ttu-id="9b01a-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9b01a-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b01a-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b01a-118">-WhatIf</span></span>
<span data-ttu-id="9b01a-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9b01a-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b01a-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9b01a-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b01a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b01a-121">-DefaultProfile</span></span>
<span data-ttu-id="9b01a-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9b01a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b01a-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="9b01a-123">-Name</span></span>
<span data-ttu-id="9b01a-124">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="9b01a-124">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="9b01a-125">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="9b01a-125">-Namespace</span></span>
<span data-ttu-id="9b01a-126">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="9b01a-126">Namespace Name.</span></span>

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

### <span data-ttu-id="9b01a-127">-Kö</span><span class="sxs-lookup"><span data-stu-id="9b01a-127">-Queue</span></span>
<span data-ttu-id="9b01a-128">Könamn.</span><span class="sxs-lookup"><span data-stu-id="9b01a-128">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b01a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b01a-129">CommonParameters</span></span>
<span data-ttu-id="9b01a-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b01a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b01a-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b01a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b01a-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b01a-132">INPUTS</span></span>

### <span data-ttu-id="9b01a-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9b01a-133">-ResourceGroup</span></span>
 <span data-ttu-id="9b01a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9b01a-134">System.String</span></span>
 

### <span data-ttu-id="9b01a-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="9b01a-135">-NamespaceName</span></span>
 <span data-ttu-id="9b01a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9b01a-136">System.String</span></span>
 

### <span data-ttu-id="9b01a-137">-QueueName</span><span class="sxs-lookup"><span data-stu-id="9b01a-137">-QueueName</span></span>
 <span data-ttu-id="9b01a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9b01a-138">System.String</span></span>
 

### <span data-ttu-id="9b01a-139">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="9b01a-139">-AuthorizationRuleName</span></span>
 <span data-ttu-id="9b01a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9b01a-140">System.String</span></span>

## <span data-ttu-id="9b01a-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b01a-141">OUTPUTS</span></span>

### <span data-ttu-id="9b01a-142">Microsoft. Azure. commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="9b01a-142">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="9b01a-143">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 Skriv: Microsoft. ServiceBus/AuthorizationRules namn: SBAuthoRule1 plats: West US-Taggar: rättigheter: {avlyssna, skicka}</span><span class="sxs-lookup"><span data-stu-id="9b01a-143">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="9b01a-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b01a-144">NOTES</span></span>

## <span data-ttu-id="9b01a-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b01a-145">RELATED LINKS</span></span>

