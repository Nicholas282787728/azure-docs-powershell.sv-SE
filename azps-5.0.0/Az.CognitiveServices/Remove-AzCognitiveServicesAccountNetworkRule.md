---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 2faf890cda0c87d15704a14f9c4ae12c5b3d81c2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323951"
---
# <span data-ttu-id="de5fc-101">Remove-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="de5fc-101">Remove-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="de5fc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de5fc-102">SYNOPSIS</span></span>
<span data-ttu-id="de5fc-103">Ta bort IpRules eller VirtualNetworkRules från egenskapen NetWorkRule för ett kognitivt Services-konto</span><span class="sxs-lookup"><span data-stu-id="de5fc-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="de5fc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de5fc-104">SYNTAX</span></span>

### <span data-ttu-id="de5fc-105">NetWorkRuleString (standard)</span><span class="sxs-lookup"><span data-stu-id="de5fc-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de5fc-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="de5fc-106">IpRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpRule <PSIpRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de5fc-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="de5fc-107">NetworkRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de5fc-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="de5fc-108">IpRuleString</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de5fc-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de5fc-109">DESCRIPTION</span></span>
<span data-ttu-id="de5fc-110">Cmdleten **Remove-AzCognitiveServicesAccountNetworkRule** tar bort IpRules eller VirtualNetworkRules från egenskapen NetWorkRule för ett konto för kognitiva tjänster</span><span class="sxs-lookup"><span data-stu-id="de5fc-110">The **Remove-AzCognitiveServicesAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="de5fc-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de5fc-111">EXAMPLES</span></span>

### <span data-ttu-id="de5fc-112">Exempel 1: ta bort flera IpRules med IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="de5fc-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="de5fc-113">Det här kommandot tar bort flera IpRules med IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="de5fc-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="de5fc-114">Exempel 2: ta bort en VirtualNetworkRule med VirtualNetworkRule indata från JSON</span><span class="sxs-lookup"><span data-stu-id="de5fc-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"})
```

<span data-ttu-id="de5fc-115">Det här kommandot tar bort en VirtualNetworkRule med VirtualNetworkRule-objekt med JSON.</span><span class="sxs-lookup"><span data-stu-id="de5fc-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="de5fc-116">Exempel 3: ta bort First IpRule med pipeline</span><span class="sxs-lookup"><span data-stu-id="de5fc-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount").IpRules[0] | Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="de5fc-117">Det här kommandot tar bort första IpRule med pipeline.</span><span class="sxs-lookup"><span data-stu-id="de5fc-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="de5fc-118">Exempel 4: ta bort flera VirtualNetworkRules med VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="de5fc-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="de5fc-119">Det här kommandot tar bort flera VirtualNetworkRules med VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="de5fc-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span> 

## <span data-ttu-id="de5fc-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de5fc-120">PARAMETERS</span></span>

### <span data-ttu-id="de5fc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de5fc-121">-DefaultProfile</span></span>
<span data-ttu-id="de5fc-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="de5fc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de5fc-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="de5fc-123">-IpAddressOrRange</span></span>
<span data-ttu-id="de5fc-124">Kognitiva tjänst konton NetworkRule IpRules IpAddressOrRange i strängen.</span><span class="sxs-lookup"><span data-stu-id="de5fc-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="de5fc-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="de5fc-125">-IpRule</span></span>
<span data-ttu-id="de5fc-126">Kognitiva tjänster-NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="de5fc-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="de5fc-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="de5fc-127">-Name</span></span>
<span data-ttu-id="de5fc-128">Konto namn för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="de5fc-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="de5fc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de5fc-129">-ResourceGroupName</span></span>
<span data-ttu-id="de5fc-130">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="de5fc-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="de5fc-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="de5fc-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="de5fc-132">Kognitiva tjänst konton NetworkRule VirtualNetworkRules VirtualNetworkResourceId i strängen.</span><span class="sxs-lookup"><span data-stu-id="de5fc-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="de5fc-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="de5fc-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="de5fc-134">Kognitiva tjänster-NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="de5fc-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="de5fc-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="de5fc-135">-Confirm</span></span>
<span data-ttu-id="de5fc-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="de5fc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de5fc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de5fc-137">-WhatIf</span></span>
<span data-ttu-id="de5fc-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="de5fc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de5fc-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="de5fc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de5fc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de5fc-140">CommonParameters</span></span>
<span data-ttu-id="de5fc-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de5fc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de5fc-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de5fc-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de5fc-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de5fc-143">INPUTS</span></span>

### <span data-ttu-id="de5fc-144">System. String</span><span class="sxs-lookup"><span data-stu-id="de5fc-144">System.String</span></span>

### <span data-ttu-id="de5fc-145">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="de5fc-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="de5fc-146">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="de5fc-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="de5fc-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de5fc-147">OUTPUTS</span></span>

### <span data-ttu-id="de5fc-148">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="de5fc-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="de5fc-149">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="de5fc-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="de5fc-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de5fc-150">NOTES</span></span>

## <span data-ttu-id="de5fc-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de5fc-151">RELATED LINKS</span></span>
