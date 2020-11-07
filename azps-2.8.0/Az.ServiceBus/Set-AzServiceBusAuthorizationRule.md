---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e9ab4d4d2fb2c60561d85582f2dda922ba9eaae1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919953"
---
# <span data-ttu-id="ecd84-101">Set-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ecd84-101">Set-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="ecd84-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ecd84-102">SYNOPSIS</span></span>
<span data-ttu-id="ecd84-103">Uppdaterar den angivna beskrivningen av auktoriseringsregeln för det angivna Service Bus-namnområdet eller kön eller avsnittet.</span><span class="sxs-lookup"><span data-stu-id="ecd84-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="ecd84-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ecd84-104">SYNTAX</span></span>

### <span data-ttu-id="ecd84-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ecd84-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecd84-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ecd84-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecd84-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ecd84-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecd84-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ecd84-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecd84-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ecd84-109">DESCRIPTION</span></span>
<span data-ttu-id="ecd84-110">Cmdleten **set-AzServiceBusAuthorizationRule** uppdaterar beskrivningen för den angivna auktoriseringsregeln i ett angivet Service Bus-namnområde eller en kö eller ett ämne.</span><span class="sxs-lookup"><span data-stu-id="ecd84-110">The **Set-AzServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="ecd84-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ecd84-111">EXAMPLES</span></span>

### <span data-ttu-id="ecd84-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ecd84-112">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="ecd84-113">Tar bort **Hantera** från åtkomst rättigheterna för auktoriseringsregeln `AuthoRule1` i namn området `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="ecd84-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="ecd84-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ecd84-114">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="ecd84-115">Tar **bort** behörigheter från åtkomst rättigheterna för auktoriseringsregeln `AuthoRule1` i kö `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="ecd84-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="ecd84-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ecd84-116">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="ecd84-117">Tar bort **Hantera** från åtkomst rättigheterna för auktoriseringsregeln `AuthoRule1` i avsnittet `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="ecd84-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="ecd84-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ecd84-118">PARAMETERS</span></span>

### <span data-ttu-id="ecd84-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecd84-119">-DefaultProfile</span></span>
<span data-ttu-id="ecd84-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ecd84-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecd84-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecd84-121">-InputObject</span></span>
<span data-ttu-id="ecd84-122">ServiceBus AuthorizationRule-objekt</span><span class="sxs-lookup"><span data-stu-id="ecd84-122">ServiceBus AuthorizationRule Object</span></span>

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

### <span data-ttu-id="ecd84-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="ecd84-123">-Name</span></span>
<span data-ttu-id="ecd84-124">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="ecd84-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="ecd84-125">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="ecd84-125">-Namespace</span></span>
<span data-ttu-id="ecd84-126">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="ecd84-126">Namespace Name</span></span>

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

### <span data-ttu-id="ecd84-127">-Kö</span><span class="sxs-lookup"><span data-stu-id="ecd84-127">-Queue</span></span>
<span data-ttu-id="ecd84-128">Könamn</span><span class="sxs-lookup"><span data-stu-id="ecd84-128">Queue Name</span></span>

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

### <span data-ttu-id="ecd84-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecd84-129">-ResourceGroupName</span></span>
<span data-ttu-id="ecd84-130">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="ecd84-130">Resource Group Name</span></span>

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

### <span data-ttu-id="ecd84-131">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="ecd84-131">-Rights</span></span>
<span data-ttu-id="ecd84-132">Rättigheter, till exempel @ ("lyssna", "Skicka", "hantera")</span><span class="sxs-lookup"><span data-stu-id="ecd84-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="ecd84-133">-Ämne</span><span class="sxs-lookup"><span data-stu-id="ecd84-133">-Topic</span></span>
<span data-ttu-id="ecd84-134">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="ecd84-134">Topic Name</span></span>

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

### <span data-ttu-id="ecd84-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ecd84-135">-Confirm</span></span>
<span data-ttu-id="ecd84-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ecd84-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecd84-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecd84-137">-WhatIf</span></span>
<span data-ttu-id="ecd84-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ecd84-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecd84-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ecd84-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecd84-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecd84-140">CommonParameters</span></span>
<span data-ttu-id="ecd84-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecd84-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecd84-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecd84-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecd84-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ecd84-143">INPUTS</span></span>

### <span data-ttu-id="ecd84-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ecd84-144">System.String</span></span>

### <span data-ttu-id="ecd84-145">Microsoft. Azure. commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ecd84-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="ecd84-146">System. string []</span><span class="sxs-lookup"><span data-stu-id="ecd84-146">System.String[]</span></span>

## <span data-ttu-id="ecd84-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ecd84-147">OUTPUTS</span></span>

### <span data-ttu-id="ecd84-148">Microsoft. Azure. commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ecd84-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="ecd84-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ecd84-149">NOTES</span></span>

## <span data-ttu-id="ecd84-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ecd84-150">RELATED LINKS</span></span>
