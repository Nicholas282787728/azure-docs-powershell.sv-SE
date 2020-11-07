---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 13de3f05879234a0db1af34517d37172c2a5a6bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757543"
---
# <span data-ttu-id="e3746-101">Get-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e3746-101">Get-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="e3746-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3746-102">SYNOPSIS</span></span>
<span data-ttu-id="e3746-103">Hämtar beskrivningen av en angiven auktoriseringsregel för angivna relä enheter (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="e3746-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3746-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3746-104">SYNTAX</span></span>

### <span data-ttu-id="e3746-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e3746-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3746-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3746-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3746-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3746-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3746-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3746-108">DESCRIPTION</span></span>
<span data-ttu-id="e3746-109">Cmdleten **Get-AzureRmRelayAuthorizationRule** hämtar beskrivningen av den angivna auktoriseringsregeln i angivna relä enheter (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="e3746-109">The **Get-AzureRmRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="e3746-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3746-110">EXAMPLES</span></span>

### <span data-ttu-id="e3746-111">Exempel 1 – namnrymd</span><span class="sxs-lookup"><span data-stu-id="e3746-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="e3746-112">Returnerar den angivna beskrivningen för auktoriseringsregeln för ett angivet namn område.</span><span class="sxs-lookup"><span data-stu-id="e3746-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="e3746-113">Exempel 2 – WcfRelay</span><span class="sxs-lookup"><span data-stu-id="e3746-113">Example 2 - WcfRelay</span></span>
```
PS C:\>Get-AzureRmWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="e3746-114">Returnerar den angivna beskrivningen av auktoriseringsregeln för en viss WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="e3746-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="e3746-115">Exempel 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="e3746-115">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="e3746-116">Returnerar den angivna beskrivningen av auktoriseringsregeln för en viss HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="e3746-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="e3746-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3746-117">PARAMETERS</span></span>

### <span data-ttu-id="e3746-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3746-118">-DefaultProfile</span></span>
<span data-ttu-id="e3746-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e3746-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3746-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="e3746-120">-HybridConnection</span></span>
<span data-ttu-id="e3746-121">HybridConnection namn.</span><span class="sxs-lookup"><span data-stu-id="e3746-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="e3746-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="e3746-122">-Name</span></span>
<span data-ttu-id="e3746-123">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="e3746-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="e3746-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="e3746-124">-Namespace</span></span>
<span data-ttu-id="e3746-125">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="e3746-125">Namespace Name.</span></span>

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

### <span data-ttu-id="e3746-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3746-126">-ResourceGroupName</span></span>
<span data-ttu-id="e3746-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="e3746-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="e3746-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="e3746-128">-WcfRelay</span></span>
<span data-ttu-id="e3746-129">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="e3746-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="e3746-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3746-130">CommonParameters</span></span>
<span data-ttu-id="e3746-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3746-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e3746-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3746-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3746-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3746-133">INPUTS</span></span>

### <span data-ttu-id="e3746-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e3746-134">System.String</span></span>


## <span data-ttu-id="e3746-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3746-135">OUTPUTS</span></span>

### <span data-ttu-id="e3746-136">Microsoft. Azure. commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e3746-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="e3746-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3746-137">NOTES</span></span>

## <span data-ttu-id="e3746-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3746-138">RELATED LINKS</span></span>
