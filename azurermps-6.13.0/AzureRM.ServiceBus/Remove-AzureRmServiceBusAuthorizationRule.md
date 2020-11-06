---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: fa9745703046ec835812d5fe477da938ef3fde48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576074"
---
# <span data-ttu-id="545b7-101">Remove-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="545b7-101">Remove-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="545b7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="545b7-102">SYNOPSIS</span></span>
<span data-ttu-id="545b7-103">Tar bort auktoriseringsregeln för ett Service Bus-namnområde eller en kö eller ett ämne från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="545b7-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="545b7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="545b7-104">SYNTAX</span></span>

### <span data-ttu-id="545b7-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="545b7-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="545b7-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="545b7-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="545b7-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="545b7-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="545b7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="545b7-108">DESCRIPTION</span></span>
<span data-ttu-id="545b7-109">Cmdleten **Remove-AzureRmServiceBusAuthorizationRule** tar bort auktoriseringsregeln för ett Service Bus-namnområde eller en kö eller ett ämne för den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="545b7-109">The **Remove-AzureRmServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="545b7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="545b7-110">EXAMPLES</span></span>

### <span data-ttu-id="545b7-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="545b7-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="545b7-112">Tar bort auktoriseringsregeln `SBAuthoRule1` för namn område `SB-Example1` från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="545b7-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="545b7-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="545b7-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="545b7-114">Tar bort auktoriseringsregeln `SBAuthoRule1` för kö `SBQueue` från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="545b7-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="545b7-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="545b7-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="545b7-116">Tar bort auktoriseringsregeln `SBAuthoRule1` för ett ämne `SBTopic` från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="545b7-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="545b7-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="545b7-117">PARAMETERS</span></span>

### <span data-ttu-id="545b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="545b7-118">-DefaultProfile</span></span>
<span data-ttu-id="545b7-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="545b7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="545b7-120">-Force</span><span class="sxs-lookup"><span data-stu-id="545b7-120">-Force</span></span>
<span data-ttu-id="545b7-121">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="545b7-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="545b7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="545b7-122">-InputObject</span></span>
<span data-ttu-id="545b7-123">ServiceBus AuthorizationRule-objekt</span><span class="sxs-lookup"><span data-stu-id="545b7-123">ServiceBus AuthorizationRule Object</span></span>

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

### <span data-ttu-id="545b7-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="545b7-124">-Name</span></span>
<span data-ttu-id="545b7-125">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="545b7-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="545b7-126">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="545b7-126">-Namespace</span></span>
<span data-ttu-id="545b7-127">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="545b7-127">Namespace Name</span></span>

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

### <span data-ttu-id="545b7-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="545b7-128">-PassThru</span></span>
<span data-ttu-id="545b7-129">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="545b7-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="545b7-130">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="545b7-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="545b7-131">-Kö</span><span class="sxs-lookup"><span data-stu-id="545b7-131">-Queue</span></span>
<span data-ttu-id="545b7-132">Könamn</span><span class="sxs-lookup"><span data-stu-id="545b7-132">Queue Name</span></span>

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

### <span data-ttu-id="545b7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="545b7-133">-ResourceGroupName</span></span>
<span data-ttu-id="545b7-134">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="545b7-134">Resource Group Name</span></span>

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

### <span data-ttu-id="545b7-135">-Ämne</span><span class="sxs-lookup"><span data-stu-id="545b7-135">-Topic</span></span>
<span data-ttu-id="545b7-136">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="545b7-136">Topic Name</span></span>

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

### <span data-ttu-id="545b7-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="545b7-137">-Confirm</span></span>
<span data-ttu-id="545b7-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="545b7-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="545b7-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="545b7-139">-WhatIf</span></span>
<span data-ttu-id="545b7-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="545b7-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="545b7-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="545b7-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="545b7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="545b7-142">CommonParameters</span></span>
<span data-ttu-id="545b7-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="545b7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="545b7-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="545b7-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="545b7-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="545b7-145">INPUTS</span></span>

### <span data-ttu-id="545b7-146">System. String</span><span class="sxs-lookup"><span data-stu-id="545b7-146">System.String</span></span>

### <span data-ttu-id="545b7-147">Microsoft. Azure. commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="545b7-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="545b7-148">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="545b7-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="545b7-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="545b7-149">OUTPUTS</span></span>

### <span data-ttu-id="545b7-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="545b7-150">System.Boolean</span></span>

## <span data-ttu-id="545b7-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="545b7-151">NOTES</span></span>

## <span data-ttu-id="545b7-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="545b7-152">RELATED LINKS</span></span>
