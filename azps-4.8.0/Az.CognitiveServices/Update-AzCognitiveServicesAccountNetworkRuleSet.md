---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/update-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 0f094ba8bdfa8dbf40f2af8495ee2f8cfa6fca16
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260146"
---
# <span data-ttu-id="a0242-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a0242-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="a0242-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a0242-102">SYNOPSIS</span></span>
<span data-ttu-id="a0242-103">Uppdatera egenskapen NetworkRule för ett konto för kognitiva tjänster</span><span class="sxs-lookup"><span data-stu-id="a0242-103">Update the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="a0242-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a0242-104">SYNTAX</span></span>

```
Update-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IpRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0242-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a0242-105">DESCRIPTION</span></span>
<span data-ttu-id="a0242-106">Cmdleten **Update-AzCognitiveServicesAccountNetworkRuleSet** uppdaterar egenskapen NetworkRule för ett konto för kognitiva tjänster</span><span class="sxs-lookup"><span data-stu-id="a0242-106">The **Update-AzCognitiveServicesAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="a0242-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a0242-107">EXAMPLES</span></span>

### <span data-ttu-id="a0242-108">Exempel 1: uppdatera alla egenskaper för NetworkRule, inmatnings regler med JSON</span><span class="sxs-lookup"><span data-stu-id="a0242-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -DefaultAction Allow -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2"})
```

<span data-ttu-id="a0242-109">Det här kommandot uppdaterar alla egenskaper för NetworkRule, inmatnings regler med JSON.</span><span class="sxs-lookup"><span data-stu-id="a0242-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="a0242-110">Exempel 2: förbigå egenskapen bypass för NetworkRule</span><span class="sxs-lookup"><span data-stu-id="a0242-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="a0242-111">Den här kommando uppdateringen förbigå egenskap för NetworkRule (andra egenskaper ändras inte).</span><span class="sxs-lookup"><span data-stu-id="a0242-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="a0242-112">Exempel 3: Rensa regler med NetworkRule för ett konto för kognitiva tjänster</span><span class="sxs-lookup"><span data-stu-id="a0242-112">Example 3: Clean up rules of NetworkRule of a Cognitive Services account</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="a0242-113">Det här kommandot rensar bort NetworkRule för ett konto för kognitiva tjänster (andra egenskaper inte ändras).</span><span class="sxs-lookup"><span data-stu-id="a0242-113">This command clean up rules of NetworkRule of a Cognitive Services account (other properties not change).</span></span>

## <span data-ttu-id="a0242-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a0242-114">PARAMETERS</span></span>

### <span data-ttu-id="a0242-115">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="a0242-115">-DefaultAction</span></span>
<span data-ttu-id="a0242-116">Kognitiva tjänster-NetworkRule DefaultAction.</span><span class="sxs-lookup"><span data-stu-id="a0242-116">Cognitive Services Account NetworkRule DefaultAction.</span></span> <span data-ttu-id="a0242-117">Standardvärde `Deny` .</span><span class="sxs-lookup"><span data-stu-id="a0242-117">Default value `Deny`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0242-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0242-118">-DefaultProfile</span></span>
<span data-ttu-id="a0242-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a0242-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0242-120">-IpRule</span><span class="sxs-lookup"><span data-stu-id="a0242-120">-IpRule</span></span>
<span data-ttu-id="a0242-121">Kognitiva tjänster-NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="a0242-121">Cognitive Services Account NetworkRule IpRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0242-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="a0242-122">-Name</span></span>
<span data-ttu-id="a0242-123">Konto namn för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="a0242-123">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0242-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0242-124">-ResourceGroupName</span></span>
<span data-ttu-id="a0242-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="a0242-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a0242-126">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a0242-126">-VirtualNetworkRule</span></span>
<span data-ttu-id="a0242-127">Kognitiva tjänster-NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="a0242-127">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0242-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a0242-128">-Confirm</span></span>
<span data-ttu-id="a0242-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a0242-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0242-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0242-130">-WhatIf</span></span>
<span data-ttu-id="a0242-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a0242-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0242-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a0242-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0242-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0242-133">CommonParameters</span></span>
<span data-ttu-id="a0242-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0242-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0242-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0242-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0242-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a0242-136">INPUTS</span></span>

### <span data-ttu-id="a0242-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a0242-137">System.String</span></span>

### <span data-ttu-id="a0242-138">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="a0242-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="a0242-139">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="a0242-139">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="a0242-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a0242-140">OUTPUTS</span></span>

### <span data-ttu-id="a0242-141">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a0242-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="a0242-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a0242-142">NOTES</span></span>

## <span data-ttu-id="a0242-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a0242-143">RELATED LINKS</span></span>