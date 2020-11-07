---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 2b4ddf625e5565de0d345a5477d3ba368dcb186b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757031"
---
# <span data-ttu-id="15073-101">Set-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="15073-101">Set-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="15073-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="15073-102">SYNOPSIS</span></span>
<span data-ttu-id="15073-103">Uppdaterar den angivna beskrivningen av auktoriseringsregeln för det angivna Service Bus-namnområdet eller kön eller avsnittet.</span><span class="sxs-lookup"><span data-stu-id="15073-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15073-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="15073-104">SYNTAX</span></span>

### <span data-ttu-id="15073-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="15073-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15073-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="15073-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15073-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="15073-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15073-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="15073-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15073-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="15073-109">DESCRIPTION</span></span>
<span data-ttu-id="15073-110">Cmdleten **set-AzureRmServiceBusAuthorizationRule** uppdaterar beskrivningen för den angivna auktoriseringsregeln i ett angivet Service Bus-namnområde eller en kö eller ett ämne.</span><span class="sxs-lookup"><span data-stu-id="15073-110">The **Set-AzureRmServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="15073-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="15073-111">EXAMPLES</span></span>

### <span data-ttu-id="15073-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="15073-112">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="15073-113">Tar bort **Hantera** från åtkomst rättigheterna för auktoriseringsregeln `AuthoRule1` i namn området `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="15073-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="15073-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="15073-114">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="15073-115">Tar **bort** behörigheter från åtkomst rättigheterna för auktoriseringsregeln `AuthoRule1` i kö `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="15073-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="15073-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="15073-116">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="15073-117">Tar bort **Hantera** från åtkomst rättigheterna för auktoriseringsregeln `AuthoRule1` i avsnittet `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="15073-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="15073-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="15073-118">PARAMETERS</span></span>

### <span data-ttu-id="15073-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15073-119">-DefaultProfile</span></span>
<span data-ttu-id="15073-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="15073-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15073-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15073-121">-InputObject</span></span>
<span data-ttu-id="15073-122">ServiceBus AuthorizationRule-objekt</span><span class="sxs-lookup"><span data-stu-id="15073-122">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15073-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="15073-123">-Name</span></span>
<span data-ttu-id="15073-124">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="15073-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="15073-125">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="15073-125">-Namespace</span></span>
<span data-ttu-id="15073-126">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="15073-126">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15073-127">-Kö</span><span class="sxs-lookup"><span data-stu-id="15073-127">-Queue</span></span>
<span data-ttu-id="15073-128">Könamn</span><span class="sxs-lookup"><span data-stu-id="15073-128">Queue Name</span></span>

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

### <span data-ttu-id="15073-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15073-129">-ResourceGroupName</span></span>
<span data-ttu-id="15073-130">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="15073-130">Resource Group Name</span></span>

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

### <span data-ttu-id="15073-131">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="15073-131">-Rights</span></span>
<span data-ttu-id="15073-132">Rättigheter, till exempel @ ("lyssna", "Skicka", "hantera")</span><span class="sxs-lookup"><span data-stu-id="15073-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15073-133">-Ämne</span><span class="sxs-lookup"><span data-stu-id="15073-133">-Topic</span></span>
<span data-ttu-id="15073-134">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="15073-134">Topic Name</span></span>

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

### <span data-ttu-id="15073-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="15073-135">-Confirm</span></span>
<span data-ttu-id="15073-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="15073-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15073-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15073-137">-WhatIf</span></span>
<span data-ttu-id="15073-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="15073-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15073-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="15073-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15073-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15073-140">CommonParameters</span></span>
<span data-ttu-id="15073-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15073-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15073-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15073-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15073-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="15073-143">INPUTS</span></span>

### <span data-ttu-id="15073-144">System. String</span><span class="sxs-lookup"><span data-stu-id="15073-144">System.String</span></span>

### <span data-ttu-id="15073-145">Microsoft. Azure. commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="15073-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="15073-146">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="15073-146">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="15073-147">System. string []</span><span class="sxs-lookup"><span data-stu-id="15073-147">System.String[]</span></span>

## <span data-ttu-id="15073-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="15073-148">OUTPUTS</span></span>

### <span data-ttu-id="15073-149">Microsoft. Azure. commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="15073-149">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="15073-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="15073-150">NOTES</span></span>

## <span data-ttu-id="15073-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="15073-151">RELATED LINKS</span></span>
