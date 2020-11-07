---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: be2b841511669ffa2ac3ffd416fd86072edcfb52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757459"
---
# <span data-ttu-id="2c468-101">New-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2c468-101">New-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="2c468-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c468-102">SYNOPSIS</span></span>
<span data-ttu-id="2c468-103">Skapar en ny auktoriseringsregel för den angivna tjänst bussens namnrymd eller kö eller ämne.</span><span class="sxs-lookup"><span data-stu-id="2c468-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c468-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c468-104">SYNTAX</span></span>

### <span data-ttu-id="2c468-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2c468-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c468-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2c468-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c468-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2c468-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c468-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c468-108">DESCRIPTION</span></span>
<span data-ttu-id="2c468-109">Cmdleten **New-AzureRmServiceBusAuthorizationRule** skapar en ny auktoriseringsregel för det angivna Service Bus-namnområdet eller kön eller avsnittet.</span><span class="sxs-lookup"><span data-stu-id="2c468-109">The **New-AzureRmServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="2c468-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c468-110">EXAMPLES</span></span>

### <span data-ttu-id="2c468-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2c468-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="2c468-112">Skapar `AuthoRule1` med behörigheterna **Lyssna** och **Skicka** för namn området `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="2c468-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="2c468-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="2c468-113">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="2c468-114">Skapar `AuthoRule1` med **lyssnar** och **Skicka** för kön `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="2c468-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="2c468-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="2c468-115">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="2c468-116">Skapar `AuthoRule1` med **lyssnar** och **skickar** behörighet för ämnet `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="2c468-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="2c468-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c468-117">PARAMETERS</span></span>

### <span data-ttu-id="2c468-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2c468-118">-Confirm</span></span>
<span data-ttu-id="2c468-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2c468-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c468-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="2c468-120">-Name</span></span>
<span data-ttu-id="2c468-121">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="2c468-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="2c468-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="2c468-122">-Namespace</span></span>
<span data-ttu-id="2c468-123">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="2c468-123">Namespace Name.</span></span>

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

### <span data-ttu-id="2c468-124">-Kö</span><span class="sxs-lookup"><span data-stu-id="2c468-124">-Queue</span></span>
<span data-ttu-id="2c468-125">Könamn.</span><span class="sxs-lookup"><span data-stu-id="2c468-125">Queue Name.</span></span>

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

### <span data-ttu-id="2c468-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c468-126">-ResourceGroupName</span></span>
<span data-ttu-id="2c468-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="2c468-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="2c468-128">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="2c468-128">-Rights</span></span>
<span data-ttu-id="2c468-129">Rättigheter, till exempel "lyssna", "Skicka", "hantera"</span><span class="sxs-lookup"><span data-stu-id="2c468-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="2c468-130">-Ämne</span><span class="sxs-lookup"><span data-stu-id="2c468-130">-Topic</span></span>
<span data-ttu-id="2c468-131">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="2c468-131">Topic Name.</span></span>

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

### <span data-ttu-id="2c468-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c468-132">-WhatIf</span></span>
<span data-ttu-id="2c468-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2c468-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c468-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2c468-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c468-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c468-135">-DefaultProfile</span></span>
<span data-ttu-id="2c468-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2c468-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c468-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c468-137">CommonParameters</span></span>
<span data-ttu-id="2c468-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c468-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c468-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c468-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c468-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c468-140">INPUTS</span></span>

### <span data-ttu-id="2c468-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2c468-141">System.String</span></span>
<span data-ttu-id="2c468-142">System. string []</span><span class="sxs-lookup"><span data-stu-id="2c468-142">System.String[]</span></span>

## <span data-ttu-id="2c468-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c468-143">OUTPUTS</span></span>

### <span data-ttu-id="2c468-144">Microsoft. Azure. commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="2c468-144">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="2c468-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c468-145">NOTES</span></span>

## <span data-ttu-id="2c468-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c468-146">RELATED LINKS</span></span>

