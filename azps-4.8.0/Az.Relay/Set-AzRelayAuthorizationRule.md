---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
ms.openlocfilehash: 4ca8156e80a827c9916def7ef749cfa9abb9389a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259168"
---
# <span data-ttu-id="8f6b1-101">Set-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8f6b1-101">Set-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="8f6b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8f6b1-102">SYNOPSIS</span></span>
<span data-ttu-id="8f6b1-103">Uppdaterar den angivna beskrivningen av auktoriseringsregeln för angivna relä enheter (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="8f6b1-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="8f6b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8f6b1-104">SYNTAX</span></span>

### <span data-ttu-id="8f6b1-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8f6b1-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f6b1-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8f6b1-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f6b1-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8f6b1-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f6b1-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8f6b1-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f6b1-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="8f6b1-109">AuthoRulePropertiesSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f6b1-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8f6b1-110">DESCRIPTION</span></span>
<span data-ttu-id="8f6b1-111">Cmdleten **set-AzRelayAuthorizationRule** uppdaterar beskrivningen för den angivna auktoriseringsregeln av angivna relä enheter (namnrymd/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="8f6b1-111">The **Set-AzRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="8f6b1-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8f6b1-112">EXAMPLES</span></span>

### <span data-ttu-id="8f6b1-113">Exempel 1,1-namn område med InputObject</span><span class="sxs-lookup"><span data-stu-id="8f6b1-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="8f6b1-114">Lägger till **Skicka** från åtkomst rättigheterna för auktoriseringsregeln `AuthoRule1` i namn området `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="8f6b1-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="8f6b1-115">Exempel 1,2-namnrymd med parametern Rights</span><span class="sxs-lookup"><span data-stu-id="8f6b1-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="8f6b1-116">Lägger till **Skicka** från åtkomst rättigheterna för auktoriseringsregeln `AuthoRule1` i namn området `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="8f6b1-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="8f6b1-117">Exempel 2,1-WcfRelay med InputObject</span><span class="sxs-lookup"><span data-stu-id="8f6b1-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="8f6b1-118">Lägger **till** åtkomst rättigheterna för auktoriseringsregeln `AuthoRule1` för WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="8f6b1-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="8f6b1-119">Exempel 2,2-WcfRelay med parametern Rights</span><span class="sxs-lookup"><span data-stu-id="8f6b1-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="8f6b1-120">Lägger **till** åtkomst rättigheterna för auktoriseringsregeln `AuthoRule1` för WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="8f6b1-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="8f6b1-121">Exempel 3,1-HybridConnection med InputObject</span><span class="sxs-lookup"><span data-stu-id="8f6b1-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="8f6b1-122">Lägger **till** åtkomst rättigheterna för auktoriseringsregeln `AuthoRule1` för HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="8f6b1-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="8f6b1-123">Exempel 3,2-HybridConnection med parametern Rights</span><span class="sxs-lookup"><span data-stu-id="8f6b1-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="8f6b1-124">Lägger **till** åtkomst rättigheterna för auktoriseringsregeln `AuthoRule1` för HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="8f6b1-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="8f6b1-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8f6b1-125">PARAMETERS</span></span>

### <span data-ttu-id="8f6b1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f6b1-126">-DefaultProfile</span></span>
<span data-ttu-id="8f6b1-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8f6b1-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f6b1-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="8f6b1-128">-HybridConnection</span></span>
<span data-ttu-id="8f6b1-129">HybridConnection namn.</span><span class="sxs-lookup"><span data-stu-id="8f6b1-129">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f6b1-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f6b1-130">-InputObject</span></span>
<span data-ttu-id="8f6b1-131">Relät AuthorizationRule-objekt.</span><span class="sxs-lookup"><span data-stu-id="8f6b1-131">Relay AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f6b1-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="8f6b1-132">-Name</span></span>
<span data-ttu-id="8f6b1-133">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="8f6b1-133">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f6b1-134">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="8f6b1-134">-Namespace</span></span>
<span data-ttu-id="8f6b1-135">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="8f6b1-135">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f6b1-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f6b1-136">-ResourceGroupName</span></span>
<span data-ttu-id="8f6b1-137">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="8f6b1-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="8f6b1-138">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="8f6b1-138">-Rights</span></span>
<span data-ttu-id="8f6b1-139">Rättigheter, till exempel @ ("lyssna", "Skicka", "hantera")</span><span class="sxs-lookup"><span data-stu-id="8f6b1-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f6b1-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="8f6b1-140">-WcfRelay</span></span>
<span data-ttu-id="8f6b1-141">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="8f6b1-141">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f6b1-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8f6b1-142">-Confirm</span></span>
<span data-ttu-id="8f6b1-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8f6b1-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f6b1-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f6b1-144">-WhatIf</span></span>
<span data-ttu-id="8f6b1-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8f6b1-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f6b1-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8f6b1-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f6b1-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f6b1-147">CommonParameters</span></span>
<span data-ttu-id="8f6b1-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f6b1-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f6b1-149">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f6b1-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f6b1-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8f6b1-150">INPUTS</span></span>

### <span data-ttu-id="8f6b1-151">System. String</span><span class="sxs-lookup"><span data-stu-id="8f6b1-151">System.String</span></span>

### <span data-ttu-id="8f6b1-152">Microsoft. Azure. commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="8f6b1-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="8f6b1-153">System. string []</span><span class="sxs-lookup"><span data-stu-id="8f6b1-153">System.String[]</span></span>

## <span data-ttu-id="8f6b1-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8f6b1-154">OUTPUTS</span></span>

### <span data-ttu-id="8f6b1-155">Microsoft. Azure. commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="8f6b1-155">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="8f6b1-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8f6b1-156">NOTES</span></span>

## <span data-ttu-id="8f6b1-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8f6b1-157">RELATED LINKS</span></span>
