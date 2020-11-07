---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: d1cb165b537815227a15223a1b646c38892005bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746903"
---
# <span data-ttu-id="91b77-101">Remove-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="91b77-101">Remove-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="91b77-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="91b77-102">SYNOPSIS</span></span>
<span data-ttu-id="91b77-103">Tar bort auktoriseringsregeln för ett Service Bus-namnområde eller en kö eller ett ämne från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="91b77-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

## <span data-ttu-id="91b77-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="91b77-104">SYNTAX</span></span>

### <span data-ttu-id="91b77-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="91b77-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91b77-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="91b77-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91b77-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="91b77-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91b77-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="91b77-108">DESCRIPTION</span></span>
<span data-ttu-id="91b77-109">Cmdleten **Remove-AzServiceBusAuthorizationRule** tar bort auktoriseringsregeln för ett Service Bus-namnområde eller en kö eller ett ämne för den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="91b77-109">The **Remove-AzServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="91b77-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="91b77-110">EXAMPLES</span></span>

### <span data-ttu-id="91b77-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="91b77-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="91b77-112">Tar bort auktoriseringsregeln `SBAuthoRule1` för namn område `SB-Example1` från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="91b77-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="91b77-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="91b77-113">Example 2</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="91b77-114">Tar bort auktoriseringsregeln `SBAuthoRule1` för kö `SBQueue` från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="91b77-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="91b77-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="91b77-115">Example 3</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="91b77-116">Tar bort auktoriseringsregeln `SBAuthoRule1` för ett ämne `SBTopic` från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="91b77-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="91b77-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="91b77-117">PARAMETERS</span></span>

### <span data-ttu-id="91b77-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91b77-118">-DefaultProfile</span></span>
<span data-ttu-id="91b77-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="91b77-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91b77-120">-Force</span><span class="sxs-lookup"><span data-stu-id="91b77-120">-Force</span></span>
<span data-ttu-id="91b77-121">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="91b77-121">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b77-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91b77-122">-InputObject</span></span>
<span data-ttu-id="91b77-123">ServiceBus AuthorizationRule-objekt</span><span class="sxs-lookup"><span data-stu-id="91b77-123">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91b77-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="91b77-124">-Name</span></span>
<span data-ttu-id="91b77-125">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="91b77-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="91b77-126">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="91b77-126">-Namespace</span></span>
<span data-ttu-id="91b77-127">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="91b77-127">Namespace Name</span></span>

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

### <span data-ttu-id="91b77-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91b77-128">-PassThru</span></span>
<span data-ttu-id="91b77-129">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="91b77-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="91b77-130">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="91b77-130">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b77-131">-Kö</span><span class="sxs-lookup"><span data-stu-id="91b77-131">-Queue</span></span>
<span data-ttu-id="91b77-132">Könamn</span><span class="sxs-lookup"><span data-stu-id="91b77-132">Queue Name</span></span>

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

### <span data-ttu-id="91b77-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91b77-133">-ResourceGroupName</span></span>
<span data-ttu-id="91b77-134">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="91b77-134">Resource Group Name</span></span>

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

### <span data-ttu-id="91b77-135">-Ämne</span><span class="sxs-lookup"><span data-stu-id="91b77-135">-Topic</span></span>
<span data-ttu-id="91b77-136">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="91b77-136">Topic Name</span></span>

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

### <span data-ttu-id="91b77-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="91b77-137">-Confirm</span></span>
<span data-ttu-id="91b77-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="91b77-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91b77-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91b77-139">-WhatIf</span></span>
<span data-ttu-id="91b77-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="91b77-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91b77-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="91b77-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91b77-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91b77-142">CommonParameters</span></span>
<span data-ttu-id="91b77-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91b77-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91b77-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91b77-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91b77-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="91b77-145">INPUTS</span></span>

### <span data-ttu-id="91b77-146">System. String</span><span class="sxs-lookup"><span data-stu-id="91b77-146">System.String</span></span>

### <span data-ttu-id="91b77-147">Microsoft. Azure. commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="91b77-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="91b77-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="91b77-148">OUTPUTS</span></span>

### <span data-ttu-id="91b77-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="91b77-149">System.Boolean</span></span>

## <span data-ttu-id="91b77-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="91b77-150">NOTES</span></span>

## <span data-ttu-id="91b77-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="91b77-151">RELATED LINKS</span></span>
