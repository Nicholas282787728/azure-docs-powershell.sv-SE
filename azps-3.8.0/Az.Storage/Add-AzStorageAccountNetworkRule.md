---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: e1517801c964c4794c21ada6b7d64152c6e58178
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091200"
---
# <span data-ttu-id="ff0f2-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ff0f2-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="ff0f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff0f2-102">SYNOPSIS</span></span>
 <span data-ttu-id="ff0f2-103">Lägga till IpRules eller VirtualNetworkRules till egenskapen NetworkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="ff0f2-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="ff0f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff0f2-104">SYNTAX</span></span>

### <span data-ttu-id="ff0f2-105">NetWorkRuleString (standard)</span><span class="sxs-lookup"><span data-stu-id="ff0f2-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff0f2-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="ff0f2-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff0f2-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="ff0f2-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff0f2-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="ff0f2-108">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff0f2-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff0f2-109">DESCRIPTION</span></span>
<span data-ttu-id="ff0f2-110">Cmdleten **Add-AzStorageAccountNetworkRule** lägger till IpRules eller VirtualNetworkRules i egenskapen NetworkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="ff0f2-110">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="ff0f2-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff0f2-111">EXAMPLES</span></span>

### <span data-ttu-id="ff0f2-112">Exempel 1: lägga till flera IpRules med IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="ff0f2-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="ff0f2-113">Det här kommandot lägger till flera IpRules med IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="ff0f2-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="ff0f2-114">Exempel 2: lägga till en VirtualNetworkRule med VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="ff0f2-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="ff0f2-115">Det här kommandot lägger till en VirtualNetworkRule med VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="ff0f2-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="ff0f2-116">Exempel 3: lägga till VirtualNetworkRules med VirtualNetworkRule objekt från ett annat konto</span><span class="sxs-lookup"><span data-stu-id="ff0f2-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="ff0f2-117">Det här kommandot lägger till VirtualNetworkRules med VirtualNetworkRule-objekt från ett annat konto.</span><span class="sxs-lookup"><span data-stu-id="ff0f2-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="ff0f2-118">Exempel 4: lägga till flera IpRule med IpRule-objekt, inmatning med JSON</span><span class="sxs-lookup"><span data-stu-id="ff0f2-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="ff0f2-119">Det här kommandot lägger till flera IpRule med IpRule-objekt, indata med JSON.</span><span class="sxs-lookup"><span data-stu-id="ff0f2-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="ff0f2-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff0f2-120">PARAMETERS</span></span>

### <span data-ttu-id="ff0f2-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff0f2-121">-AsJob</span></span>
<span data-ttu-id="ff0f2-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ff0f2-122">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff0f2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff0f2-123">-DefaultProfile</span></span>
<span data-ttu-id="ff0f2-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ff0f2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff0f2-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="ff0f2-125">-IPAddressOrRange</span></span>
<span data-ttu-id="ff0f2-126">Matrisen med IpAddressOrRange, Lägg till IpRules med inmatnings IpAddressOrRange och standard åtgärden Tillåt NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="ff0f2-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="ff0f2-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="ff0f2-127">-IPRule</span></span>
<span data-ttu-id="ff0f2-128">Matrisen med IpRule-objekt som ska läggas till i egenskapen NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="ff0f2-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: IpRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff0f2-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="ff0f2-129">-Name</span></span>
<span data-ttu-id="ff0f2-130">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="ff0f2-130">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff0f2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff0f2-131">-ResourceGroupName</span></span>
<span data-ttu-id="ff0f2-132">Anger namnet på resurs gruppen som innehåller lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="ff0f2-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="ff0f2-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="ff0f2-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="ff0f2-134">Matrisen med VirtualNetworkResourceId lägger till VirtualNetworkRule med inmatnings VirtualNetworkResourceId och standard åtgärd Tillåt NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="ff0f2-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="ff0f2-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ff0f2-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="ff0f2-136">Matrisen med VirtualNetworkRule-objekt som ska läggas till i egenskapen NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="ff0f2-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff0f2-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ff0f2-137">-Confirm</span></span>
<span data-ttu-id="ff0f2-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ff0f2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff0f2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff0f2-139">-WhatIf</span></span>
<span data-ttu-id="ff0f2-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ff0f2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff0f2-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ff0f2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff0f2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff0f2-142">CommonParameters</span></span>
<span data-ttu-id="ff0f2-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff0f2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff0f2-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff0f2-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff0f2-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff0f2-145">INPUTS</span></span>

### <span data-ttu-id="ff0f2-146">System. String</span><span class="sxs-lookup"><span data-stu-id="ff0f2-146">System.String</span></span>

### <span data-ttu-id="ff0f2-147">Microsoft. Azure. commands. Management. Storage. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="ff0f2-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="ff0f2-148">Microsoft. Azure. commands. Management. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="ff0f2-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="ff0f2-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff0f2-149">OUTPUTS</span></span>

### <span data-ttu-id="ff0f2-150">Microsoft. Azure. commands. Management. Storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ff0f2-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="ff0f2-151">Microsoft. Azure. commands. Management. Storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="ff0f2-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="ff0f2-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff0f2-152">NOTES</span></span>

## <span data-ttu-id="ff0f2-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff0f2-153">RELATED LINKS</span></span>
