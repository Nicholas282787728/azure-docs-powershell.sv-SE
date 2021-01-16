---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: beba9c457378949dfe82811186bde84522b46ae5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397019"
---
# <span data-ttu-id="8e753-101">New-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8e753-101">New-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="8e753-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8e753-102">SYNOPSIS</span></span>
<span data-ttu-id="8e753-103">Skapar en ny auktoriseringsregel för den angivna tjänst bussens namnrymd eller kö eller ämne.</span><span class="sxs-lookup"><span data-stu-id="8e753-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="8e753-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8e753-104">SYNTAX</span></span>

### <span data-ttu-id="8e753-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8e753-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e753-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8e753-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e753-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8e753-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e753-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8e753-108">DESCRIPTION</span></span>
<span data-ttu-id="8e753-109">Cmdleten **New-AzServiceBusAuthorizationRule** skapar en ny auktoriseringsregel för det angivna Service Bus-namnområdet eller kön eller avsnittet.</span><span class="sxs-lookup"><span data-stu-id="8e753-109">The **New-AzServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="8e753-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8e753-110">EXAMPLES</span></span>

### <span data-ttu-id="8e753-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8e753-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="8e753-112">Skapar `AuthoRule1` med behörigheterna **Lyssna** och **Skicka** för namn området `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="8e753-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="8e753-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8e753-113">Example 2</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="8e753-114">Skapar `AuthoRule1` med **lyssnar** och **Skicka** för kön `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="8e753-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="8e753-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="8e753-115">Example 3</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="8e753-116">Skapar `AuthoRule1` med **lyssnar** och **skickar** behörighet för ämnet `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="8e753-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="8e753-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8e753-117">PARAMETERS</span></span>

### <span data-ttu-id="8e753-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e753-118">-DefaultProfile</span></span>
<span data-ttu-id="8e753-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8e753-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e753-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="8e753-120">-Name</span></span>
<span data-ttu-id="8e753-121">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="8e753-121">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e753-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="8e753-122">-Namespace</span></span>
<span data-ttu-id="8e753-123">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="8e753-123">Namespace Name</span></span>

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

### <span data-ttu-id="8e753-124">-Kö</span><span class="sxs-lookup"><span data-stu-id="8e753-124">-Queue</span></span>
<span data-ttu-id="8e753-125">Könamn</span><span class="sxs-lookup"><span data-stu-id="8e753-125">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e753-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e753-126">-ResourceGroupName</span></span>
<span data-ttu-id="8e753-127">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="8e753-127">Resource Group Name</span></span>

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

### <span data-ttu-id="8e753-128">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="8e753-128">-Rights</span></span>
<span data-ttu-id="8e753-129">Rättigheter, till exempel "lyssna", "Skicka", "hantera"</span><span class="sxs-lookup"><span data-stu-id="8e753-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e753-130">-Ämne</span><span class="sxs-lookup"><span data-stu-id="8e753-130">-Topic</span></span>
<span data-ttu-id="8e753-131">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="8e753-131">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e753-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8e753-132">-Confirm</span></span>
<span data-ttu-id="8e753-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8e753-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e753-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e753-134">-WhatIf</span></span>
<span data-ttu-id="8e753-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8e753-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e753-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8e753-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e753-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e753-137">CommonParameters</span></span>
<span data-ttu-id="8e753-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e753-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e753-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e753-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e753-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8e753-140">INPUTS</span></span>

### <span data-ttu-id="8e753-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8e753-141">System.String</span></span>

### <span data-ttu-id="8e753-142">System. string []</span><span class="sxs-lookup"><span data-stu-id="8e753-142">System.String[]</span></span>

## <span data-ttu-id="8e753-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8e753-143">OUTPUTS</span></span>

### <span data-ttu-id="8e753-144">Microsoft. Azure. commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="8e753-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="8e753-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8e753-145">NOTES</span></span>

## <span data-ttu-id="8e753-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8e753-146">RELATED LINKS</span></span>
