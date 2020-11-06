---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 91f37ad2ed49b4c1bd39306be803776ddce9ecff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583072"
---
# <span data-ttu-id="3d4c6-101">Set-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3d4c6-101">Set-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="3d4c6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d4c6-102">SYNOPSIS</span></span>
<span data-ttu-id="3d4c6-103">Uppdaterar den angivna beskrivningen av auktoriseringsregeln för angivna relä enheter (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="3d4c6-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d4c6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d4c6-104">SYNTAX</span></span>

### <span data-ttu-id="3d4c6-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3d4c6-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <AuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d4c6-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d4c6-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <AuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d4c6-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d4c6-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [[-InputObject] <AuthorizationRuleAttributes>]
 [[-Rights] <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d4c6-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3d4c6-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <AuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d4c6-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="3d4c6-109">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d4c6-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d4c6-110">DESCRIPTION</span></span>
<span data-ttu-id="3d4c6-111">Cmdleten **set-AzureRmRelayAuthorizationRule** uppdaterar beskrivningen för den angivna auktoriseringsregeln av angivna relä enheter (namnrymd/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="3d4c6-111">The **Set-AzureRmRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="3d4c6-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d4c6-112">EXAMPLES</span></span>

### <span data-ttu-id="3d4c6-113">Exempel 1,1-namn område med InputObject</span><span class="sxs-lookup"><span data-stu-id="3d4c6-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule
```

<span data-ttu-id="3d4c6-114">Lägger till **Skicka** från åtkomst rättigheterna för auktoriseringsregeln `AuthoRule1` i namn området `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="3d4c6-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="3d4c6-115">Exempel 1,2-namnrymd med parametern Rights</span><span class="sxs-lookup"><span data-stu-id="3d4c6-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"
```

<span data-ttu-id="3d4c6-116">Lägger till **Skicka** från åtkomst rättigheterna för auktoriseringsregeln `AuthoRule1` i namn området `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="3d4c6-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="3d4c6-117">Exempel 2,1-WcfRelay med InputObject</span><span class="sxs-lookup"><span data-stu-id="3d4c6-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho
```

<span data-ttu-id="3d4c6-118">Lägger **till** åtkomst rättigheterna för auktoriseringsregeln `AuthoRule1` för WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="3d4c6-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="3d4c6-119">Exempel 2,2-WcfRelay med parametern Rights</span><span class="sxs-lookup"><span data-stu-id="3d4c6-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="3d4c6-120">Lägger **till** åtkomst rättigheterna för auktoriseringsregeln `AuthoRule1` för WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="3d4c6-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="3d4c6-121">Exempel 3,1-HybridConnection med InputObject</span><span class="sxs-lookup"><span data-stu-id="3d4c6-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho
```

<span data-ttu-id="3d4c6-122">Lägger **till** åtkomst rättigheterna för auktoriseringsregeln `AuthoRule1` för HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="3d4c6-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="3d4c6-123">Exempel 3,2-HybridConnection med parametern Rights</span><span class="sxs-lookup"><span data-stu-id="3d4c6-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="3d4c6-124">Lägger **till** åtkomst rättigheterna för auktoriseringsregeln `AuthoRule1` för HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="3d4c6-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="3d4c6-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d4c6-125">PARAMETERS</span></span>

### <span data-ttu-id="3d4c6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d4c6-126">-DefaultProfile</span></span>
<span data-ttu-id="3d4c6-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d4c6-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4c6-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="3d4c6-128">-HybridConnection</span></span>
<span data-ttu-id="3d4c6-129">HybridConnection namn.</span><span class="sxs-lookup"><span data-stu-id="3d4c6-129">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d4c6-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d4c6-130">-InputObject</span></span>
<span data-ttu-id="3d4c6-131">AuthorizationRule-objekt</span><span class="sxs-lookup"><span data-stu-id="3d4c6-131">Relay AuthorizationRule Object</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4c6-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="3d4c6-132">-Name</span></span>
<span data-ttu-id="3d4c6-133">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="3d4c6-133">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d4c6-134">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="3d4c6-134">-Namespace</span></span>
<span data-ttu-id="3d4c6-135">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="3d4c6-135">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d4c6-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d4c6-136">-ResourceGroupName</span></span>
<span data-ttu-id="3d4c6-137">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="3d4c6-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="3d4c6-138">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="3d4c6-138">-Rights</span></span>
<span data-ttu-id="3d4c6-139">Rättigheter, till exempel @ ("lyssna", "Skicka", "hantera")</span><span class="sxs-lookup"><span data-stu-id="3d4c6-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4c6-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="3d4c6-140">-WcfRelay</span></span>
<span data-ttu-id="3d4c6-141">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="3d4c6-141">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d4c6-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3d4c6-142">-Confirm</span></span>
<span data-ttu-id="3d4c6-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d4c6-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d4c6-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d4c6-144">-WhatIf</span></span>
<span data-ttu-id="3d4c6-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3d4c6-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d4c6-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3d4c6-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d4c6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d4c6-147">CommonParameters</span></span>
<span data-ttu-id="3d4c6-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d4c6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d4c6-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d4c6-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d4c6-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d4c6-150">INPUTS</span></span>

### <span data-ttu-id="3d4c6-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d4c6-151">-ResourceGroupName</span></span>
 <span data-ttu-id="3d4c6-152">System. String</span><span class="sxs-lookup"><span data-stu-id="3d4c6-152">System.String</span></span> 

### <span data-ttu-id="3d4c6-153">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="3d4c6-153">-Namespace</span></span>
 <span data-ttu-id="3d4c6-154">System. String</span><span class="sxs-lookup"><span data-stu-id="3d4c6-154">System.String</span></span> 
 

### <span data-ttu-id="3d4c6-155">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="3d4c6-155">-WcfRelay</span></span>
 <span data-ttu-id="3d4c6-156">System. String</span><span class="sxs-lookup"><span data-stu-id="3d4c6-156">System.String</span></span> 

### <span data-ttu-id="3d4c6-157">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="3d4c6-157">-HybridConnection</span></span>
 <span data-ttu-id="3d4c6-158">System. String</span><span class="sxs-lookup"><span data-stu-id="3d4c6-158">System.String</span></span> 
 

### <span data-ttu-id="3d4c6-159">-Namn</span><span class="sxs-lookup"><span data-stu-id="3d4c6-159">-Name</span></span>
 <span data-ttu-id="3d4c6-160">System. String</span><span class="sxs-lookup"><span data-stu-id="3d4c6-160">System.String</span></span>

### <span data-ttu-id="3d4c6-161">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d4c6-161">-InputObject</span></span>
 <span data-ttu-id="3d4c6-162">Microsoft. Azure. commands. Relay. Models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="3d4c6-162">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>
 

### <span data-ttu-id="3d4c6-163">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="3d4c6-163">-Rights</span></span>
 <span data-ttu-id="3d4c6-164">System. string []</span><span class="sxs-lookup"><span data-stu-id="3d4c6-164">System.String []</span></span>

## <span data-ttu-id="3d4c6-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d4c6-165">OUTPUTS</span></span>

### <span data-ttu-id="3d4c6-166">Microsoft. Azure. commands. Relay. Models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="3d4c6-166">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>

### <span data-ttu-id="3d4c6-167">Exempel 1 – namnrymd</span><span class="sxs-lookup"><span data-stu-id="3d4c6-167">Example 1 - Namespace</span></span>
<span data-ttu-id="3d4c6-168">Rättigheter: {lyssning, skicka} namn: AuthoRule1 typ: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="3d4c6-168">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="3d4c6-169">Exempel 2 – WcfRelay</span><span class="sxs-lookup"><span data-stu-id="3d4c6-169">Example 2 - WcfRelay</span></span>
<span data-ttu-id="3d4c6-170">Rättigheter: {lyssning, skicka} namn: AuthoRule1 typ: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="3d4c6-170">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="3d4c6-171">Exempel 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="3d4c6-171">Example 3 - HybridConnection</span></span>
<span data-ttu-id="3d4c6-172">Rättigheter: {lyssning, skicka} namn: AuthoRule1 typ: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="3d4c6-172">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="3d4c6-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d4c6-173">NOTES</span></span>

## <span data-ttu-id="3d4c6-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d4c6-174">RELATED LINKS</span></span>

