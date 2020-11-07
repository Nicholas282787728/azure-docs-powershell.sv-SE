---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 62edcb426fe62f834b876b0dd4e2006712f81348
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746916"
---
# <span data-ttu-id="53b77-101">New-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="53b77-101">New-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="53b77-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53b77-102">SYNOPSIS</span></span>
<span data-ttu-id="53b77-103">Skapar en ny auktoriseringsregel för den angivna tjänst bussens namnrymd eller kö eller ämne.</span><span class="sxs-lookup"><span data-stu-id="53b77-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="53b77-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53b77-104">SYNTAX</span></span>

### <span data-ttu-id="53b77-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="53b77-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53b77-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="53b77-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53b77-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="53b77-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53b77-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53b77-108">DESCRIPTION</span></span>
<span data-ttu-id="53b77-109">Cmdleten **New-AzServiceBusAuthorizationRule** skapar en ny auktoriseringsregel för det angivna Service Bus-namnområdet eller kön eller avsnittet.</span><span class="sxs-lookup"><span data-stu-id="53b77-109">The **New-AzServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="53b77-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53b77-110">EXAMPLES</span></span>

### <span data-ttu-id="53b77-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="53b77-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="53b77-112">Skapar `AuthoRule1` med behörigheterna **Lyssna** och **Skicka** för namn området `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="53b77-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="53b77-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="53b77-113">Example 2</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="53b77-114">Skapar `AuthoRule1` med **lyssnar** och **Skicka** för kön `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="53b77-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="53b77-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="53b77-115">Example 3</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="53b77-116">Skapar `AuthoRule1` med **lyssnar** och **skickar** behörighet för ämnet `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="53b77-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="53b77-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53b77-117">PARAMETERS</span></span>

### <span data-ttu-id="53b77-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53b77-118">-DefaultProfile</span></span>
<span data-ttu-id="53b77-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="53b77-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53b77-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="53b77-120">-Name</span></span>
<span data-ttu-id="53b77-121">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="53b77-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="53b77-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="53b77-122">-Namespace</span></span>
<span data-ttu-id="53b77-123">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="53b77-123">Namespace Name</span></span>

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

### <span data-ttu-id="53b77-124">-Kö</span><span class="sxs-lookup"><span data-stu-id="53b77-124">-Queue</span></span>
<span data-ttu-id="53b77-125">Könamn</span><span class="sxs-lookup"><span data-stu-id="53b77-125">Queue Name</span></span>

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

### <span data-ttu-id="53b77-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53b77-126">-ResourceGroupName</span></span>
<span data-ttu-id="53b77-127">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="53b77-127">Resource Group Name</span></span>

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

### <span data-ttu-id="53b77-128">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="53b77-128">-Rights</span></span>
<span data-ttu-id="53b77-129">Rättigheter, till exempel "lyssna", "Skicka", "hantera"</span><span class="sxs-lookup"><span data-stu-id="53b77-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="53b77-130">-Ämne</span><span class="sxs-lookup"><span data-stu-id="53b77-130">-Topic</span></span>
<span data-ttu-id="53b77-131">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="53b77-131">Topic Name</span></span>

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

### <span data-ttu-id="53b77-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="53b77-132">-Confirm</span></span>
<span data-ttu-id="53b77-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="53b77-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53b77-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53b77-134">-WhatIf</span></span>
<span data-ttu-id="53b77-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="53b77-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53b77-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="53b77-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53b77-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53b77-137">CommonParameters</span></span>
<span data-ttu-id="53b77-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53b77-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53b77-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53b77-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53b77-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53b77-140">INPUTS</span></span>

### <span data-ttu-id="53b77-141">System. String</span><span class="sxs-lookup"><span data-stu-id="53b77-141">System.String</span></span>

### <span data-ttu-id="53b77-142">System. string []</span><span class="sxs-lookup"><span data-stu-id="53b77-142">System.String[]</span></span>

## <span data-ttu-id="53b77-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53b77-143">OUTPUTS</span></span>

### <span data-ttu-id="53b77-144">Microsoft. Azure. commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="53b77-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="53b77-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53b77-145">NOTES</span></span>

## <span data-ttu-id="53b77-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53b77-146">RELATED LINKS</span></span>
