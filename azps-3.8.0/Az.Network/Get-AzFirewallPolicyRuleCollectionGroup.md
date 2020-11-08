---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 8ce5369605f419821994c771dc9200e138e5ad7a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091070"
---
# <span data-ttu-id="4f8ce-101">Get-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="4f8ce-101">Get-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="4f8ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f8ce-102">SYNOPSIS</span></span>
<span data-ttu-id="4f8ce-103">Hämtar en grupp för regel insamling för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="4f8ce-103">Gets a Azure Firewall Policy Rule Collection Group</span></span>

## <span data-ttu-id="4f8ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f8ce-104">SYNTAX</span></span>

### <span data-ttu-id="4f8ce-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4f8ce-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f8ce-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f8ce-106">GetByInputObjectParameterSet</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -Name <String> -AzureFirewallPolicy <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f8ce-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f8ce-107">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f8ce-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f8ce-108">DESCRIPTION</span></span>
<span data-ttu-id="4f8ce-109">Cmdleten **Get-AzFirewallPolicyRuleCollectionGroup** hämtar de RuleCollectionGroup som nämns i en brand Väggs princip</span><span class="sxs-lookup"><span data-stu-id="4f8ce-109">The **Get-AzFirewallPolicyRuleCollectionGroup** cmdlet gets the RuleCollectionGroup mentioned from a Firewall Policy</span></span>

## <span data-ttu-id="4f8ce-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f8ce-110">EXAMPLES</span></span>

### <span data-ttu-id="4f8ce-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4f8ce-111">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicyRuleCollectionGroup -Name rg1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="4f8ce-112">Det här exemplet får regeln collectionGroup i brand Väggs princip $fp</span><span class="sxs-lookup"><span data-stu-id="4f8ce-112">This example get the rule collectionGroup in the firewall policy $fp</span></span>

## <span data-ttu-id="4f8ce-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f8ce-113">PARAMETERS</span></span>

### <span data-ttu-id="4f8ce-114">-AzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="4f8ce-114">-AzureFirewallPolicy</span></span>
<span data-ttu-id="4f8ce-115">Brand Väggs princip.</span><span class="sxs-lookup"><span data-stu-id="4f8ce-115">Firewall Policy.</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f8ce-116">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="4f8ce-116">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="4f8ce-117">Namnet på brand Väggs principen</span><span class="sxs-lookup"><span data-stu-id="4f8ce-117">The Firewall policy name</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f8ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f8ce-118">-DefaultProfile</span></span>
<span data-ttu-id="4f8ce-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4f8ce-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f8ce-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="4f8ce-120">-Name</span></span>
<span data-ttu-id="4f8ce-121">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="4f8ce-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f8ce-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f8ce-122">-ResourceGroupName</span></span>
<span data-ttu-id="4f8ce-123">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4f8ce-123">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f8ce-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f8ce-124">-ResourceId</span></span>
<span data-ttu-id="4f8ce-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="4f8ce-125">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f8ce-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f8ce-126">CommonParameters</span></span>
<span data-ttu-id="4f8ce-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f8ce-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f8ce-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f8ce-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f8ce-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f8ce-129">INPUTS</span></span>

### <span data-ttu-id="4f8ce-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4f8ce-130">System.String</span></span>

### <span data-ttu-id="4f8ce-131">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="4f8ce-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="4f8ce-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f8ce-132">OUTPUTS</span></span>

### <span data-ttu-id="4f8ce-133">Microsoft. Azure. commands. Networks. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="4f8ce-133">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="4f8ce-134">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. Network. Models. PSAzureFirewall, Microsoft. Azure. PowerShell. cmdletar. Network, version = 1.12.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4f8ce-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4f8ce-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f8ce-135">NOTES</span></span>

## <span data-ttu-id="4f8ce-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f8ce-136">RELATED LINKS</span></span>
