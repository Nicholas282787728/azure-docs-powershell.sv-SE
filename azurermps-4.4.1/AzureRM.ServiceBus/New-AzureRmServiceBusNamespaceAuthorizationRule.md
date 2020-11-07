---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 6e20ceb2a6809e1e6010263563006468753cd41c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757458"
---
# <span data-ttu-id="c12fd-101">New-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c12fd-101">New-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="c12fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c12fd-102">SYNOPSIS</span></span>
<span data-ttu-id="c12fd-103">Skapar en ny auktoriseringsregel för det angivna Service Bus-namnområdet</span><span class="sxs-lookup"><span data-stu-id="c12fd-103">Creates a new authorization rule for the specified Service Bus namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c12fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c12fd-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c12fd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c12fd-105">DESCRIPTION</span></span>
<span data-ttu-id="c12fd-106">Cmdleten **New-AzureRmServiceBusNamespaceAuthorizationRule** skapar en ny auktoriseringsregel för det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="c12fd-106">The **New-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="c12fd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c12fd-107">EXAMPLES</span></span>

### <span data-ttu-id="c12fd-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c12fd-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="c12fd-109">Skapar `AuthoRule1` med behörigheterna **Lyssna** och **Skicka** för namn området `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="c12fd-109">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="c12fd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c12fd-110">PARAMETERS</span></span>

### <span data-ttu-id="c12fd-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c12fd-111">-ResourceGroup</span></span>
<span data-ttu-id="c12fd-112">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c12fd-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="c12fd-113">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="c12fd-113">-Rights</span></span>
<span data-ttu-id="c12fd-114">Rättigheterna; till exempel @ ("lyssna", "Skicka", "hantera")</span><span class="sxs-lookup"><span data-stu-id="c12fd-114">The Rights; for example, @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="c12fd-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c12fd-115">-Confirm</span></span>
<span data-ttu-id="c12fd-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c12fd-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c12fd-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c12fd-117">-WhatIf</span></span>
<span data-ttu-id="c12fd-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c12fd-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c12fd-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c12fd-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c12fd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c12fd-120">-DefaultProfile</span></span>
<span data-ttu-id="c12fd-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c12fd-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c12fd-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="c12fd-122">-Name</span></span>
<span data-ttu-id="c12fd-123">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="c12fd-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="c12fd-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="c12fd-124">-Namespace</span></span>
<span data-ttu-id="c12fd-125">Namn områdes namnet ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="c12fd-125">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="c12fd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c12fd-126">CommonParameters</span></span>
<span data-ttu-id="c12fd-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c12fd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c12fd-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c12fd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c12fd-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c12fd-129">INPUTS</span></span>

### <span data-ttu-id="c12fd-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c12fd-130">-ResourceGroup</span></span>
 <span data-ttu-id="c12fd-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c12fd-131">System.String</span></span>
 

### <span data-ttu-id="c12fd-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="c12fd-132">-NamespaceName</span></span>
 <span data-ttu-id="c12fd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c12fd-133">System.String</span></span>
 

### <span data-ttu-id="c12fd-134">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="c12fd-134">-AuthorizationRuleName</span></span>
 <span data-ttu-id="c12fd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c12fd-135">System.String</span></span>
 

### <span data-ttu-id="c12fd-136">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="c12fd-136">-Rights</span></span>
 <span data-ttu-id="c12fd-137">System. string []</span><span class="sxs-lookup"><span data-stu-id="c12fd-137">System.String []</span></span>

## <span data-ttu-id="c12fd-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c12fd-138">OUTPUTS</span></span>

### <span data-ttu-id="c12fd-139">Microsoft. Azure. commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="c12fd-139">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="c12fd-140">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 typ: Microsoft. ServiceBus/AuthorizationRules namn: AuthoRule1 Location: tagg: Rights: {Listener, Send}</span><span class="sxs-lookup"><span data-stu-id="c12fd-140">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="c12fd-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c12fd-141">NOTES</span></span>

## <span data-ttu-id="c12fd-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c12fd-142">RELATED LINKS</span></span>

