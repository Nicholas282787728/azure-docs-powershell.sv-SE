---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
ms.openlocfilehash: 39bba687e355b1742210fb0c37fc8f1a65d957a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324444"
---
# <span data-ttu-id="c6e05-101">New-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c6e05-101">New-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="c6e05-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c6e05-102">SYNOPSIS</span></span>
<span data-ttu-id="c6e05-103">Skapar en ny auktoriseringsregel för angivna relä enheter (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="c6e05-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="c6e05-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c6e05-104">SYNTAX</span></span>

### <span data-ttu-id="c6e05-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c6e05-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6e05-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c6e05-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6e05-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c6e05-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6e05-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c6e05-108">DESCRIPTION</span></span>
<span data-ttu-id="c6e05-109">Cmdleten **New-AzRelayAuthorizationRule** skapar en ny auktoriseringsregel för angivna relä enheter (namnrymd/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="c6e05-109">The **New-AzRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="c6e05-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c6e05-110">EXAMPLES</span></span>

### <span data-ttu-id="c6e05-111">Exempel 1: namnrymd</span><span class="sxs-lookup"><span data-stu-id="c6e05-111">Example 1: Namespace</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="c6e05-112">Skapar `AuthoRule1` med **lyssnar** rättigheter för namn området `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="c6e05-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="c6e05-113">Exempel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="c6e05-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="c6e05-114">Skapar en auktoriseringsregel `AuthoRule1` med **lyssnar** rättigheter för WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="c6e05-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="c6e05-115">Exempel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="c6e05-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="c6e05-116">Skapar `AuthoRule1` med **lyssnings** rättigheter för Hybrid anslutningen `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="c6e05-116">Creates `AuthoRule1` with **Listen** rights for the Hybrid Connection `TestHybridConnection`.</span></span>

## <span data-ttu-id="c6e05-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c6e05-117">PARAMETERS</span></span>

### <span data-ttu-id="c6e05-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6e05-118">-DefaultProfile</span></span>
<span data-ttu-id="c6e05-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c6e05-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6e05-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="c6e05-120">-HybridConnection</span></span>
<span data-ttu-id="c6e05-121">HybridConnection namn.</span><span class="sxs-lookup"><span data-stu-id="c6e05-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="c6e05-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="c6e05-122">-Name</span></span>
<span data-ttu-id="c6e05-123">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="c6e05-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="c6e05-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="c6e05-124">-Namespace</span></span>
<span data-ttu-id="c6e05-125">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="c6e05-125">Namespace Name.</span></span>

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

### <span data-ttu-id="c6e05-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6e05-126">-ResourceGroupName</span></span>
<span data-ttu-id="c6e05-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="c6e05-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="c6e05-128">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="c6e05-128">-Rights</span></span>
<span data-ttu-id="c6e05-129">Rättigheter, till exempel "lyssna", "Skicka", "hantera"</span><span class="sxs-lookup"><span data-stu-id="c6e05-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="c6e05-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="c6e05-130">-WcfRelay</span></span>
<span data-ttu-id="c6e05-131">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="c6e05-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="c6e05-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c6e05-132">-Confirm</span></span>
<span data-ttu-id="c6e05-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c6e05-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6e05-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6e05-134">-WhatIf</span></span>
<span data-ttu-id="c6e05-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c6e05-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6e05-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c6e05-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6e05-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6e05-137">CommonParameters</span></span>
<span data-ttu-id="c6e05-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6e05-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6e05-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6e05-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6e05-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c6e05-140">INPUTS</span></span>

### <span data-ttu-id="c6e05-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c6e05-141">System.String</span></span>

### <span data-ttu-id="c6e05-142">System. string []</span><span class="sxs-lookup"><span data-stu-id="c6e05-142">System.String[]</span></span>

## <span data-ttu-id="c6e05-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c6e05-143">OUTPUTS</span></span>

### <span data-ttu-id="c6e05-144">Microsoft. Azure. commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="c6e05-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="c6e05-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c6e05-145">NOTES</span></span>

## <span data-ttu-id="c6e05-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c6e05-146">RELATED LINKS</span></span>
