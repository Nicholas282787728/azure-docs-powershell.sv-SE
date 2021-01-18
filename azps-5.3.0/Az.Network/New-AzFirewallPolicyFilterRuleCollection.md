---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyfilterrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
ms.openlocfilehash: d5871a9e1a99a27cc0b2728ca3638a0548f42fc6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523260"
---
# <span data-ttu-id="f8ca3-101">New-AzFirewallPolicyFilterRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f8ca3-101">New-AzFirewallPolicyFilterRuleCollection</span></span>

## <span data-ttu-id="f8ca3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f8ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="f8ca3-103">Skapa en ny regel samling för Azure Firewall policy</span><span class="sxs-lookup"><span data-stu-id="f8ca3-103">Create a new Azure Firewall Policy Filter Rule Collection</span></span>

## <span data-ttu-id="f8ca3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f8ca3-104">SYNTAX</span></span>

```
New-AzFirewallPolicyFilterRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallPolicyRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8ca3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f8ca3-105">DESCRIPTION</span></span>
<span data-ttu-id="f8ca3-106">Cmdleten **New-AzFirewallPolicyFilterRuleCollection** skapar en filter regel samling för en Azure Firewall-princip.</span><span class="sxs-lookup"><span data-stu-id="f8ca3-106">The **New-AzFirewallPolicyFilterRuleCollection** cmdlet creates a Filter rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="f8ca3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f8ca3-107">EXAMPLES</span></span>

### <span data-ttu-id="f8ca3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f8ca3-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyFilterRuleCollection -Name FR1 -Priority 400 -Rule $appRule1 ,$appRule2 -ActionType "Allow"
```

<span data-ttu-id="f8ca3-109">I det här exemplet skapas en filter regel med två regel villkor</span><span class="sxs-lookup"><span data-stu-id="f8ca3-109">This example creates a Filter rule with 2 rule conditions</span></span>

## <span data-ttu-id="f8ca3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f8ca3-110">PARAMETERS</span></span>

### <span data-ttu-id="f8ca3-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="f8ca3-111">-ActionType</span></span>
<span data-ttu-id="f8ca3-112">Åtgärden för regel samlingen</span><span class="sxs-lookup"><span data-stu-id="f8ca3-112">The action of the rule collection</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ca3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8ca3-113">-DefaultProfile</span></span>
<span data-ttu-id="f8ca3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f8ca3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8ca3-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="f8ca3-115">-Name</span></span>
<span data-ttu-id="f8ca3-116">Namnet på program regel samlingen</span><span class="sxs-lookup"><span data-stu-id="f8ca3-116">The name of the Application Rule Collection</span></span>

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

### <span data-ttu-id="f8ca3-117">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="f8ca3-117">-Priority</span></span>
<span data-ttu-id="f8ca3-118">Prioriteten för regel samlingen</span><span class="sxs-lookup"><span data-stu-id="f8ca3-118">The priority of the rule collection</span></span>

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

### <span data-ttu-id="f8ca3-119">-Regel</span><span class="sxs-lookup"><span data-stu-id="f8ca3-119">-Rule</span></span>
<span data-ttu-id="f8ca3-120">Listan med program regler</span><span class="sxs-lookup"><span data-stu-id="f8ca3-120">The list of application rules</span></span>

```yaml
Type: PSAzureFirewallPolicyRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ca3-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f8ca3-121">-Confirm</span></span>
<span data-ttu-id="f8ca3-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f8ca3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8ca3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8ca3-123">-WhatIf</span></span>
<span data-ttu-id="f8ca3-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f8ca3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8ca3-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f8ca3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8ca3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8ca3-126">CommonParameters</span></span>
<span data-ttu-id="f8ca3-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8ca3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8ca3-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8ca3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8ca3-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f8ca3-129">INPUTS</span></span>

### <span data-ttu-id="f8ca3-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="f8ca3-130">None</span></span>

## <span data-ttu-id="f8ca3-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f8ca3-131">OUTPUTS</span></span>

### <span data-ttu-id="f8ca3-132">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="f8ca3-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="f8ca3-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f8ca3-133">NOTES</span></span>

## <span data-ttu-id="f8ca3-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f8ca3-134">RELATED LINKS</span></span>
