---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 53a46e9c78544919c325f63b8bc8ccf9fd457f31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577519"
---
# <span data-ttu-id="dc8ac-101">Get-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="dc8ac-101">Get-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="dc8ac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc8ac-102">SYNOPSIS</span></span>
<span data-ttu-id="dc8ac-103">Hämtar beskrivningen av en angiven auktoriseringsregel för angivna relä enheter (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="dc8ac-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc8ac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc8ac-104">SYNTAX</span></span>

### <span data-ttu-id="dc8ac-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="dc8ac-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc8ac-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="dc8ac-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc8ac-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="dc8ac-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc8ac-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc8ac-108">DESCRIPTION</span></span>
<span data-ttu-id="dc8ac-109">Cmdleten **Get-AzureRmRelayAuthorizationRule** hämtar beskrivningen av den angivna auktoriseringsregeln i angivna relä enheter (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="dc8ac-109">The **Get-AzureRmRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="dc8ac-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc8ac-110">EXAMPLES</span></span>

### <span data-ttu-id="dc8ac-111">Exempel 1 – namnrymd</span><span class="sxs-lookup"><span data-stu-id="dc8ac-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="dc8ac-112">Returnerar den angivna beskrivningen för auktoriseringsregeln för ett angivet namn område.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="dc8ac-113">Exempel 2 – WcfRelay</span><span class="sxs-lookup"><span data-stu-id="dc8ac-113">Example 2 - WcfRelay</span></span>
```
PS C:\>Get-AzureRmWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
```

<span data-ttu-id="dc8ac-114">Returnerar den angivna beskrivningen av auktoriseringsregeln för en viss WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="dc8ac-115">Exempel 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="dc8ac-115">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="dc8ac-116">Returnerar den angivna beskrivningen av auktoriseringsregeln för en viss HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="dc8ac-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc8ac-117">PARAMETERS</span></span>

### <span data-ttu-id="dc8ac-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="dc8ac-118">-HybridConnection</span></span>
<span data-ttu-id="dc8ac-119">HybridConnection namn.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="dc8ac-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="dc8ac-120">-Name</span></span>
<span data-ttu-id="dc8ac-121">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-121">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc8ac-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="dc8ac-122">-Namespace</span></span>
<span data-ttu-id="dc8ac-123">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-123">Namespace Name.</span></span>

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

### <span data-ttu-id="dc8ac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc8ac-124">-ResourceGroupName</span></span>
<span data-ttu-id="dc8ac-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="dc8ac-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="dc8ac-126">-WcfRelay</span></span>
<span data-ttu-id="dc8ac-127">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="dc8ac-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc8ac-128">-DefaultProfile</span></span>
<span data-ttu-id="dc8ac-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc8ac-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc8ac-130">CommonParameters</span></span>
<span data-ttu-id="dc8ac-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc8ac-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc8ac-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc8ac-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc8ac-133">INPUTS</span></span>

### <span data-ttu-id="dc8ac-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc8ac-134">-ResourceGroupName</span></span>
 <span data-ttu-id="dc8ac-135">System. String</span><span class="sxs-lookup"><span data-stu-id="dc8ac-135">System.String</span></span> 

### <span data-ttu-id="dc8ac-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="dc8ac-136">-NamespaceName</span></span>
 <span data-ttu-id="dc8ac-137">System. String</span><span class="sxs-lookup"><span data-stu-id="dc8ac-137">System.String</span></span> 
 

### <span data-ttu-id="dc8ac-138">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="dc8ac-138">-HybridConnectionsName</span></span>
 <span data-ttu-id="dc8ac-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dc8ac-139">System.String</span></span> 

### <span data-ttu-id="dc8ac-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="dc8ac-140">-WcfRelayName</span></span>
 <span data-ttu-id="dc8ac-141">System. String</span><span class="sxs-lookup"><span data-stu-id="dc8ac-141">System.String</span></span> 

### <span data-ttu-id="dc8ac-142">-Namn</span><span class="sxs-lookup"><span data-stu-id="dc8ac-142">-Name</span></span>
 <span data-ttu-id="dc8ac-143">System. String</span><span class="sxs-lookup"><span data-stu-id="dc8ac-143">System.String</span></span>

## <span data-ttu-id="dc8ac-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc8ac-144">OUTPUTS</span></span>

### <span data-ttu-id="dc8ac-145">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Relay. Models. AuthorizationRuleAttributes, Microsoft. Azure. commands. Relay, version = 0.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dc8ac-145">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="dc8ac-146">Exempel 1 – namnrymd</span><span class="sxs-lookup"><span data-stu-id="dc8ac-146">Example 1 - Namespace</span></span>
<span data-ttu-id="dc8ac-147">Rättigheter: {lyssning, skicka} namn: AuthoRule1 typ: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut hoRule1</span><span class="sxs-lookup"><span data-stu-id="dc8ac-147">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut hoRule1</span></span>

### <span data-ttu-id="dc8ac-148">Exempel 2 – WcfRelay</span><span class="sxs-lookup"><span data-stu-id="dc8ac-148">Example 2 - WcfRelay</span></span>
<span data-ttu-id="dc8ac-149">Rättigheter: {lyssning, skicka} namn: AuthoRule1 typ: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay 1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="dc8ac-149">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay 1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="dc8ac-150">Exempel 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="dc8ac-150">Example 3 - HybridConnection</span></span>
<span data-ttu-id="dc8ac-151">Rättigheter: {lyssning, skicka} namn: AuthoRule1 typ: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test HybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="dc8ac-151">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test HybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="dc8ac-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc8ac-152">NOTES</span></span>

## <span data-ttu-id="dc8ac-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc8ac-153">RELATED LINKS</span></span>

