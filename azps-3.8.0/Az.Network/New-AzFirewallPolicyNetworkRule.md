---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: b4cbc404139cd56e75f03c5cb19cb9b761576e39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089543"
---
# <span data-ttu-id="84591-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="84591-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="84591-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="84591-102">SYNOPSIS</span></span>
<span data-ttu-id="84591-103">Skapa en ny Azure Firewall-brandväggsregel</span><span class="sxs-lookup"><span data-stu-id="84591-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="84591-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="84591-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84591-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="84591-105">DESCRIPTION</span></span>
<span data-ttu-id="84591-106">Cmdleten **New-AzFirewallPolicyNetworkRule** skapar en nätverks regel för en Azure Firewall-princip.</span><span class="sxs-lookup"><span data-stu-id="84591-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="84591-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="84591-107">EXAMPLES</span></span>

### <span data-ttu-id="84591-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="84591-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="84591-109">I det här exemplet skapas en nätverks regel med käll adress, protokoll, mål adress och målport</span><span class="sxs-lookup"><span data-stu-id="84591-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="84591-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="84591-110">PARAMETERS</span></span>

### <span data-ttu-id="84591-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84591-111">-DefaultProfile</span></span>
<span data-ttu-id="84591-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="84591-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84591-113">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="84591-113">-Description</span></span>
<span data-ttu-id="84591-114">Beskrivning av regeln</span><span class="sxs-lookup"><span data-stu-id="84591-114">The description of the rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84591-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="84591-115">-DestinationAddress</span></span>
<span data-ttu-id="84591-116">Mål adresserna för regeln</span><span class="sxs-lookup"><span data-stu-id="84591-116">The destination addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84591-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="84591-117">-DestinationPort</span></span>
<span data-ttu-id="84591-118">Mål portarna för regeln</span><span class="sxs-lookup"><span data-stu-id="84591-118">The destination ports of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84591-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="84591-119">-Name</span></span>
<span data-ttu-id="84591-120">Namnet på nätverks regeln</span><span class="sxs-lookup"><span data-stu-id="84591-120">The name of the Network Rule</span></span>

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

### <span data-ttu-id="84591-121">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="84591-121">-Protocols</span></span>
<span data-ttu-id="84591-122">Regelns protokoll</span><span class="sxs-lookup"><span data-stu-id="84591-122">The protocols of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84591-123">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="84591-123">-SourceAddress</span></span>
<span data-ttu-id="84591-124">Käll adresserna för regeln</span><span class="sxs-lookup"><span data-stu-id="84591-124">The source addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84591-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="84591-125">-Confirm</span></span>
<span data-ttu-id="84591-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="84591-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84591-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84591-127">-WhatIf</span></span>
<span data-ttu-id="84591-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="84591-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84591-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="84591-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84591-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84591-130">CommonParameters</span></span>
<span data-ttu-id="84591-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84591-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84591-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84591-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84591-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="84591-133">INPUTS</span></span>

### <span data-ttu-id="84591-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="84591-134">None</span></span>

## <span data-ttu-id="84591-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="84591-135">OUTPUTS</span></span>

### <span data-ttu-id="84591-136">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="84591-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="84591-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="84591-137">NOTES</span></span>

## <span data-ttu-id="84591-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="84591-138">RELATED LINKS</span></span>
