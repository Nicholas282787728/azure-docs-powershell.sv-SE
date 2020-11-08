---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/add-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 039a3e4bf676f29d55f48e7e0883f5818e7367b7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088046"
---
# <span data-ttu-id="61326-101">Add-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="61326-101">Add-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="61326-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="61326-102">SYNOPSIS</span></span>
<span data-ttu-id="61326-103">Lägga till IpRules eller VirtualNetworkRules till egenskapen NetworkRule för ett kognitivt Services-konto</span><span class="sxs-lookup"><span data-stu-id="61326-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="61326-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="61326-104">SYNTAX</span></span>

### <span data-ttu-id="61326-105">NetWorkRuleString (standard)</span><span class="sxs-lookup"><span data-stu-id="61326-105">NetWorkRuleString (Default)</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61326-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="61326-106">IpRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IpRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61326-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="61326-107">NetworkRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61326-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="61326-108">IpRuleString</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61326-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="61326-109">DESCRIPTION</span></span>
<span data-ttu-id="61326-110">Cmdleten **Add-AzCognitiveServicesAccountNetworkRule** lägger till IpRules eller VirtualNetworkRules i egenskapen NetworkRule för ett konto för kognitiva tjänster</span><span class="sxs-lookup"><span data-stu-id="61326-110">The **Add-AzCognitiveServicesAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="61326-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="61326-111">EXAMPLES</span></span>

### <span data-ttu-id="61326-112">Exempel 1: lägga till flera IpRules med IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="61326-112">Example 1: Add several IpRules with IpAddressOrRange</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "200.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="61326-113">Det här kommandot lägger till flera IpRules med IpAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="61326-113">This command add several IpRules with IpAddressOrRange.</span></span>

### <span data-ttu-id="61326-114">Exempel 2: lägga till en VirtualNetworkRule med VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="61326-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="61326-115">Det här kommandot lägger till en VirtualNetworkRule med VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="61326-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="61326-116">Exempel 3: lägga till VirtualNetworkRules med VirtualNetworkRule objekt från ett annat konto</span><span class="sxs-lookup"><span data-stu-id="61326-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount1"
PS C:\> Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="61326-117">Det här kommandot lägger till VirtualNetworkRules med VirtualNetworkRule-objekt från ett annat konto.</span><span class="sxs-lookup"><span data-stu-id="61326-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="61326-118">Exempel 4: lägga till flera IpRule med IpRule-objekt, inmatning med JSON</span><span class="sxs-lookup"><span data-stu-id="61326-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
```

<span data-ttu-id="61326-119">Det här kommandot lägger till flera IpRule med IpRule-objekt, indata med JSON.</span><span class="sxs-lookup"><span data-stu-id="61326-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="61326-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="61326-120">PARAMETERS</span></span>

### <span data-ttu-id="61326-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61326-121">-DefaultProfile</span></span>
<span data-ttu-id="61326-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="61326-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61326-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="61326-123">-IpAddressOrRange</span></span>
<span data-ttu-id="61326-124">Kognitiva tjänst konton NetworkRule IpRules IpAddressOrRange i strängen.</span><span class="sxs-lookup"><span data-stu-id="61326-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IpRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61326-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="61326-125">-IpRule</span></span>
<span data-ttu-id="61326-126">Kognitiva tjänster-NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="61326-126">Cognitive Services Account NetworkRule IpRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]
Parameter Sets: IpRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61326-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="61326-127">-Name</span></span>
<span data-ttu-id="61326-128">Konto namn för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="61326-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="61326-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61326-129">-ResourceGroupName</span></span>
<span data-ttu-id="61326-130">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="61326-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="61326-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="61326-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="61326-132">Kognitiva tjänst konton NetworkRule VirtualNetworkRules VirtualNetworkResourceId i strängen.</span><span class="sxs-lookup"><span data-stu-id="61326-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

```yaml
Type: System.String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61326-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="61326-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="61326-134">Kognitiva tjänster-NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="61326-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61326-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="61326-135">-Confirm</span></span>
<span data-ttu-id="61326-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="61326-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61326-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61326-137">-WhatIf</span></span>
<span data-ttu-id="61326-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="61326-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61326-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="61326-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61326-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61326-140">CommonParameters</span></span>
<span data-ttu-id="61326-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61326-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61326-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61326-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61326-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="61326-143">INPUTS</span></span>

### <span data-ttu-id="61326-144">System. String</span><span class="sxs-lookup"><span data-stu-id="61326-144">System.String</span></span>

### <span data-ttu-id="61326-145">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="61326-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="61326-146">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="61326-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="61326-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="61326-147">OUTPUTS</span></span>

### <span data-ttu-id="61326-148">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="61326-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="61326-149">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="61326-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="61326-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="61326-150">NOTES</span></span>

## <span data-ttu-id="61326-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="61326-151">RELATED LINKS</span></span>
