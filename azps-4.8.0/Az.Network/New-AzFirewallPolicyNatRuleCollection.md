---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
ms.openlocfilehash: 010fd83d8b8e26e67e35afcc54b03ca0c1a5bd5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259304"
---
# <span data-ttu-id="c936b-101">New-AzFirewallPolicyNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c936b-101">New-AzFirewallPolicyNatRuleCollection</span></span>

## <span data-ttu-id="c936b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c936b-102">SYNOPSIS</span></span>
<span data-ttu-id="c936b-103">Skapa en ny regel samling för Azure Firewall-principer</span><span class="sxs-lookup"><span data-stu-id="c936b-103">Create a new Azure Firewall Policy Nat Rule Collection</span></span>

## <span data-ttu-id="c936b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c936b-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallPolicyNetworkRule> -ActionType <String> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c936b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c936b-105">DESCRIPTION</span></span>
<span data-ttu-id="c936b-106">Cmdleten **New-AzFirewallPolicyNatRuleCollection** skapar en NAT-regel samling för en Azure Firewall-princip.</span><span class="sxs-lookup"><span data-stu-id="c936b-106">The **New-AzFirewallPolicyNatRuleCollection** cmdlet creates a Nat rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="c936b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c936b-107">EXAMPLES</span></span>

### <span data-ttu-id="c936b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c936b-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRuleCollection -Name NatRule1 -Priority 200 -Rule $netRule1 -ActionType "Dnat" -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="c936b-109">I det här exemplet skapas en NAT-regel samling med en nätverks regel</span><span class="sxs-lookup"><span data-stu-id="c936b-109">This example creates a nat rule collection with a network rule</span></span>

## <span data-ttu-id="c936b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c936b-110">PARAMETERS</span></span>

### <span data-ttu-id="c936b-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="c936b-111">-ActionType</span></span>
<span data-ttu-id="c936b-112">Typ av regel åtgärd</span><span class="sxs-lookup"><span data-stu-id="c936b-112">The type of the rule action</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Dnat

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c936b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c936b-113">-DefaultProfile</span></span>
<span data-ttu-id="c936b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c936b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c936b-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="c936b-115">-Name</span></span>
<span data-ttu-id="c936b-116">Namnet på nätverks regel samlingen</span><span class="sxs-lookup"><span data-stu-id="c936b-116">The name of the Network Rule Collection</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c936b-117">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="c936b-117">-Priority</span></span>
<span data-ttu-id="c936b-118">Prioriteten för regel samlingen</span><span class="sxs-lookup"><span data-stu-id="c936b-118">The priority of the rule collection</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c936b-119">-Regel</span><span class="sxs-lookup"><span data-stu-id="c936b-119">-Rule</span></span>
<span data-ttu-id="c936b-120">Listan med nätverks regler</span><span class="sxs-lookup"><span data-stu-id="c936b-120">The list of network rules</span></span>

```yaml
Type: PSAzureFirewallPolicyNetworkRule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c936b-121">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="c936b-121">-TranslatedAddress</span></span>
<span data-ttu-id="c936b-122">Den översatta adressen för denna NAT-regel</span><span class="sxs-lookup"><span data-stu-id="c936b-122">The translated address for this NAT rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c936b-123">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="c936b-123">-TranslatedPort</span></span>
<span data-ttu-id="c936b-124">Den översatta porten för denna NAT-regel</span><span class="sxs-lookup"><span data-stu-id="c936b-124">The translated port for this NAT rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c936b-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c936b-125">-Confirm</span></span>
<span data-ttu-id="c936b-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c936b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c936b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c936b-127">-WhatIf</span></span>
<span data-ttu-id="c936b-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c936b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c936b-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c936b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c936b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c936b-130">CommonParameters</span></span>
<span data-ttu-id="c936b-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c936b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c936b-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c936b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c936b-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c936b-133">INPUTS</span></span>

### <span data-ttu-id="c936b-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="c936b-134">None</span></span>

## <span data-ttu-id="c936b-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c936b-135">OUTPUTS</span></span>

### <span data-ttu-id="c936b-136">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c936b-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="c936b-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c936b-137">NOTES</span></span>

## <span data-ttu-id="c936b-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c936b-138">RELATED LINKS</span></span>