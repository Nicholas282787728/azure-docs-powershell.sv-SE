---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: 1b9fd10e11cb283f880979e7e4a5d703521c9a87
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925569"
---
# <span data-ttu-id="05770-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="05770-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="05770-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05770-102">SYNOPSIS</span></span>
<span data-ttu-id="05770-103">Skapa en ny regel för programmet för Azure Firewall-principer</span><span class="sxs-lookup"><span data-stu-id="05770-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="05770-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05770-104">SYNTAX</span></span>

### <span data-ttu-id="05770-105">TargetFqdn (standard)</span><span class="sxs-lookup"><span data-stu-id="05770-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="05770-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="05770-106">FqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05770-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05770-107">DESCRIPTION</span></span>
<span data-ttu-id="05770-108">Cmdleten **New-AzFirewallPolicyApplicationRule** skapar en program regel för en Azure Firewall-princip.</span><span class="sxs-lookup"><span data-stu-id="05770-108">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="05770-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05770-109">EXAMPLES</span></span>

### <span data-ttu-id="05770-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="05770-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="05770-111">I det här exemplet skapas en program regel med käll adress, protokoll och mål-FQDN.</span><span class="sxs-lookup"><span data-stu-id="05770-111">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

## <span data-ttu-id="05770-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05770-112">PARAMETERS</span></span>

### <span data-ttu-id="05770-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05770-113">-DefaultProfile</span></span>
<span data-ttu-id="05770-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="05770-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05770-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="05770-115">-Description</span></span>
<span data-ttu-id="05770-116">Beskrivning av regeln</span><span class="sxs-lookup"><span data-stu-id="05770-116">The description of the rule</span></span>

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

### <span data-ttu-id="05770-117">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="05770-117">-FqdnTag</span></span>
<span data-ttu-id="05770-118">Regelns FQDN-Taggar</span><span class="sxs-lookup"><span data-stu-id="05770-118">The FQDN Tags of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05770-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="05770-119">-Name</span></span>
<span data-ttu-id="05770-120">Namnet på program regeln</span><span class="sxs-lookup"><span data-stu-id="05770-120">The name of the Application Rule</span></span>

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

### <span data-ttu-id="05770-121">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="05770-121">-Protocol</span></span>
<span data-ttu-id="05770-122">Regelns protokoll</span><span class="sxs-lookup"><span data-stu-id="05770-122">The protocols of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05770-123">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="05770-123">-SourceAddress</span></span>
<span data-ttu-id="05770-124">Käll adresserna för regeln</span><span class="sxs-lookup"><span data-stu-id="05770-124">The source addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05770-125">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="05770-125">-TargetFqdn</span></span>
<span data-ttu-id="05770-126">Mål-FQDN för regeln</span><span class="sxs-lookup"><span data-stu-id="05770-126">The target FQDNs of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05770-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="05770-127">-Confirm</span></span>
<span data-ttu-id="05770-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="05770-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05770-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05770-129">-WhatIf</span></span>
<span data-ttu-id="05770-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="05770-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05770-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="05770-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05770-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05770-132">CommonParameters</span></span>
<span data-ttu-id="05770-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05770-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05770-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05770-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05770-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05770-135">INPUTS</span></span>

### <span data-ttu-id="05770-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="05770-136">None</span></span>

## <span data-ttu-id="05770-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05770-137">OUTPUTS</span></span>

### <span data-ttu-id="05770-138">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="05770-138">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="05770-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05770-139">NOTES</span></span>

## <span data-ttu-id="05770-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05770-140">RELATED LINKS</span></span>
