---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 7722ee1a84aee6ef16642a84ac9f72f259d9772f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755638"
---
# <span data-ttu-id="52617-101">Remove-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="52617-101">Remove-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="52617-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52617-102">SYNOPSIS</span></span>
<span data-ttu-id="52617-103">Tar bort auktoriseringsregeln för ett Service Bus-namnområde eller en kö eller ett ämne från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="52617-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52617-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52617-104">SYNTAX</span></span>

### <span data-ttu-id="52617-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="52617-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="52617-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="52617-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-Queue] <String> [-Name] <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="52617-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="52617-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-Topic] <String> [-Name] <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="52617-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52617-108">DESCRIPTION</span></span>
<span data-ttu-id="52617-109">Cmdleten **Remove-AzureRmServiceBusAuthorizationRule** tar bort auktoriseringsregeln för ett Service Bus-namnområde eller en kö eller ett ämne för den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="52617-109">The **Remove-AzureRmServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="52617-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52617-110">EXAMPLES</span></span>

### <span data-ttu-id="52617-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="52617-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```
<span data-ttu-id="52617-112">Tar bort auktoriseringsregeln `SBAuthoRule1` för namn område `SB-Example1` från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="52617-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="52617-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="52617-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```
<span data-ttu-id="52617-114">Tar bort auktoriseringsregeln `SBAuthoRule1` för kö `SBQueue` från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="52617-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="52617-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="52617-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```
<span data-ttu-id="52617-116">Tar bort auktoriseringsregeln `SBAuthoRule1` för ett ämne `SBTopic` från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="52617-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="52617-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52617-117">PARAMETERS</span></span>

### <span data-ttu-id="52617-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="52617-118">-Confirm</span></span>
<span data-ttu-id="52617-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="52617-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52617-120">-Force</span><span class="sxs-lookup"><span data-stu-id="52617-120">-Force</span></span>
<span data-ttu-id="52617-121">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="52617-121">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52617-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="52617-122">-Name</span></span>
<span data-ttu-id="52617-123">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="52617-123">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52617-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="52617-124">-Namespace</span></span>
<span data-ttu-id="52617-125">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="52617-125">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52617-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52617-126">-PassThru</span></span>
<span data-ttu-id="52617-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="52617-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52617-128">-Kö</span><span class="sxs-lookup"><span data-stu-id="52617-128">-Queue</span></span>
<span data-ttu-id="52617-129">Könamn.</span><span class="sxs-lookup"><span data-stu-id="52617-129">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52617-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52617-130">-ResourceGroupName</span></span>
<span data-ttu-id="52617-131">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="52617-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="52617-132">-Ämne</span><span class="sxs-lookup"><span data-stu-id="52617-132">-Topic</span></span>
<span data-ttu-id="52617-133">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="52617-133">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52617-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52617-134">-WhatIf</span></span>
<span data-ttu-id="52617-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="52617-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52617-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="52617-136">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="52617-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52617-137">INPUTS</span></span>

### <span data-ttu-id="52617-138">System. String</span><span class="sxs-lookup"><span data-stu-id="52617-138">System.String</span></span>


## <span data-ttu-id="52617-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52617-139">OUTPUTS</span></span>

### <span data-ttu-id="52617-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52617-140">System.Boolean</span></span>


## <span data-ttu-id="52617-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52617-141">NOTES</span></span>

## <span data-ttu-id="52617-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52617-142">RELATED LINKS</span></span>

