---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
ms.openlocfilehash: af83820d33b9f36d93cc7623001d22a6cb5e0212
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259177"
---
# <span data-ttu-id="1059f-101">Get-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1059f-101">Get-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="1059f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1059f-102">SYNOPSIS</span></span>
<span data-ttu-id="1059f-103">Hämtar beskrivningen av en angiven auktoriseringsregel för angivna relä enheter (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="1059f-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="1059f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1059f-104">SYNTAX</span></span>

### <span data-ttu-id="1059f-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1059f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1059f-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1059f-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1059f-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1059f-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1059f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1059f-108">DESCRIPTION</span></span>
<span data-ttu-id="1059f-109">Cmdleten **Get-AzRelayAuthorizationRule** hämtar beskrivningen av den angivna auktoriseringsregeln i angivna relä enheter (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="1059f-109">The **Get-AzRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="1059f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1059f-110">EXAMPLES</span></span>

### <span data-ttu-id="1059f-111">Exempel 1: namnrymd</span><span class="sxs-lookup"><span data-stu-id="1059f-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="1059f-112">Returnerar den angivna beskrivningen för auktoriseringsregeln för ett angivet namn område.</span><span class="sxs-lookup"><span data-stu-id="1059f-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="1059f-113">Exempel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="1059f-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>Get-AzWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="1059f-114">Returnerar den angivna beskrivningen av auktoriseringsregeln för en viss WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="1059f-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="1059f-115">Exempel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="1059f-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="1059f-116">Returnerar den angivna beskrivningen av auktoriseringsregeln för en viss HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="1059f-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="1059f-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1059f-117">PARAMETERS</span></span>

### <span data-ttu-id="1059f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1059f-118">-DefaultProfile</span></span>
<span data-ttu-id="1059f-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1059f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1059f-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="1059f-120">-HybridConnection</span></span>
<span data-ttu-id="1059f-121">HybridConnection namn.</span><span class="sxs-lookup"><span data-stu-id="1059f-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="1059f-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="1059f-122">-Name</span></span>
<span data-ttu-id="1059f-123">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="1059f-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="1059f-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="1059f-124">-Namespace</span></span>
<span data-ttu-id="1059f-125">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="1059f-125">Namespace Name.</span></span>

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

### <span data-ttu-id="1059f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1059f-126">-ResourceGroupName</span></span>
<span data-ttu-id="1059f-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="1059f-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="1059f-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="1059f-128">-WcfRelay</span></span>
<span data-ttu-id="1059f-129">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="1059f-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="1059f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1059f-130">CommonParameters</span></span>
<span data-ttu-id="1059f-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1059f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1059f-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1059f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1059f-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1059f-133">INPUTS</span></span>

### <span data-ttu-id="1059f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1059f-134">System.String</span></span>

## <span data-ttu-id="1059f-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1059f-135">OUTPUTS</span></span>

### <span data-ttu-id="1059f-136">Microsoft. Azure. commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="1059f-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="1059f-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1059f-137">NOTES</span></span>

## <span data-ttu-id="1059f-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1059f-138">RELATED LINKS</span></span>