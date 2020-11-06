---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 9e4eecad543346efa60dfb0b9a20e31c47a59036
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575873"
---
# <span data-ttu-id="784f2-101">New-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="784f2-101">New-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="784f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="784f2-102">SYNOPSIS</span></span>
<span data-ttu-id="784f2-103">Skapar en ny auktoriseringsregel för angivna relä enheter (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="784f2-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="784f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="784f2-104">SYNTAX</span></span>

### <span data-ttu-id="784f2-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="784f2-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="784f2-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="784f2-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="784f2-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="784f2-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="784f2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="784f2-108">DESCRIPTION</span></span>
<span data-ttu-id="784f2-109">Cmdleten **New-AzureRmRelayAuthorizationRule** skapar en ny auktoriseringsregel för angivna relä enheter (namnrymd/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="784f2-109">The **New-AzureRmRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="784f2-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="784f2-110">EXAMPLES</span></span>

### <span data-ttu-id="784f2-111">Exempel 1 – namnrymd</span><span class="sxs-lookup"><span data-stu-id="784f2-111">Example 1 - Namespace</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="784f2-112">Skapar `AuthoRule1` med **lyssnar** rättigheter för namn området `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="784f2-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="784f2-113">Exempel 2 – WcfRelay</span><span class="sxs-lookup"><span data-stu-id="784f2-113">Example 2 - WcfRelay</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="784f2-114">Skapar en auktoriseringsregel `AuthoRule1` med **lyssnar** rättigheter för WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="784f2-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="784f2-115">Exempel 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="784f2-115">Example 3 - HybridConnection</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="784f2-116">Skapar `AuthoRule1` med **lyssnar** rättigheter för namn området `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="784f2-116">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="784f2-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="784f2-117">PARAMETERS</span></span>

### <span data-ttu-id="784f2-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="784f2-118">-Confirm</span></span>
<span data-ttu-id="784f2-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="784f2-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="784f2-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="784f2-120">-HybridConnection</span></span>
<span data-ttu-id="784f2-121">HybridConnection namn.</span><span class="sxs-lookup"><span data-stu-id="784f2-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="784f2-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="784f2-122">-Name</span></span>
<span data-ttu-id="784f2-123">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="784f2-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="784f2-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="784f2-124">-Namespace</span></span>
<span data-ttu-id="784f2-125">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="784f2-125">Namespace Name.</span></span>

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

### <span data-ttu-id="784f2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="784f2-126">-ResourceGroupName</span></span>
<span data-ttu-id="784f2-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="784f2-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="784f2-128">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="784f2-128">-Rights</span></span>
<span data-ttu-id="784f2-129">Rättigheter, till exempel "lyssna", "Skicka", "hantera"</span><span class="sxs-lookup"><span data-stu-id="784f2-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="784f2-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="784f2-130">-WcfRelay</span></span>
<span data-ttu-id="784f2-131">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="784f2-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="784f2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="784f2-132">-WhatIf</span></span>
<span data-ttu-id="784f2-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="784f2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="784f2-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="784f2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="784f2-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="784f2-135">-DefaultProfile</span></span>
<span data-ttu-id="784f2-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="784f2-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="784f2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="784f2-137">CommonParameters</span></span>
<span data-ttu-id="784f2-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="784f2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="784f2-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="784f2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="784f2-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="784f2-140">INPUTS</span></span>

### <span data-ttu-id="784f2-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="784f2-141">-ResourceGroupName</span></span>
 <span data-ttu-id="784f2-142">System. String</span><span class="sxs-lookup"><span data-stu-id="784f2-142">System.String</span></span> 

### <span data-ttu-id="784f2-143">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="784f2-143">-Namespace</span></span>
 <span data-ttu-id="784f2-144">System. String</span><span class="sxs-lookup"><span data-stu-id="784f2-144">System.String</span></span> 
 

### <span data-ttu-id="784f2-145">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="784f2-145">-WcfRelay</span></span>
 <span data-ttu-id="784f2-146">System. String</span><span class="sxs-lookup"><span data-stu-id="784f2-146">System.String</span></span> 

### <span data-ttu-id="784f2-147">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="784f2-147">-HybridConnection</span></span>
 <span data-ttu-id="784f2-148">System. String</span><span class="sxs-lookup"><span data-stu-id="784f2-148">System.String</span></span> 
 

### <span data-ttu-id="784f2-149">-Namn</span><span class="sxs-lookup"><span data-stu-id="784f2-149">-Name</span></span>
 <span data-ttu-id="784f2-150">System. String</span><span class="sxs-lookup"><span data-stu-id="784f2-150">System.String</span></span>
 

### <span data-ttu-id="784f2-151">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="784f2-151">-Rights</span></span>
 <span data-ttu-id="784f2-152">System. string []</span><span class="sxs-lookup"><span data-stu-id="784f2-152">System.String []</span></span>

## <span data-ttu-id="784f2-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="784f2-153">OUTPUTS</span></span>

### <span data-ttu-id="784f2-154">Microsoft. Azure. commands. Relay. Models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="784f2-154">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>

### <span data-ttu-id="784f2-155">Exempel 1 – namnrymd</span><span class="sxs-lookup"><span data-stu-id="784f2-155">Example 1 - Namespace</span></span>
<span data-ttu-id="784f2-156">Rättigheter: {lyssning} namn: AuthoRule1 typ: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="784f2-156">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="784f2-157">Exempel 2 – WcfRelay</span><span class="sxs-lookup"><span data-stu-id="784f2-157">Example 2 - WcfRelay</span></span>
<span data-ttu-id="784f2-158">Rättigheter: {lyssning} namn: AuthoRule1 typ: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="784f2-158">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="784f2-159">Exempel 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="784f2-159">Example 3 - HybridConnection</span></span>
<span data-ttu-id="784f2-160">Rättigheter: {lyssning} namn: AuthoRule1 typ: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="784f2-160">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="784f2-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="784f2-161">NOTES</span></span>

## <span data-ttu-id="784f2-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="784f2-162">RELATED LINKS</span></span>

