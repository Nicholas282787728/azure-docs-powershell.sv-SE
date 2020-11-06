---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/add-azurermstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageAccountNetworkRule.md
ms.openlocfilehash: b6ec1908af93642cf064b72b1a78a64641749409
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574141"
---
# <span data-ttu-id="cfdba-101">Add-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cfdba-101">Add-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="cfdba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cfdba-102">SYNOPSIS</span></span>
 <span data-ttu-id="cfdba-103">Lägga till IpRules eller VirtualNetworkRules till egenskapen NetworkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="cfdba-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfdba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cfdba-104">SYNTAX</span></span>

### <span data-ttu-id="cfdba-105">NetWorkRuleString (standard)</span><span class="sxs-lookup"><span data-stu-id="cfdba-105">NetWorkRuleString (Default)</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cfdba-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="cfdba-106">IpRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfdba-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="cfdba-107">NetworkRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfdba-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="cfdba-108">IpRuleString</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cfdba-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cfdba-109">DESCRIPTION</span></span>
<span data-ttu-id="cfdba-110">Cmdleten **Add-AzureRmStorageAccountNetworkRule** lägger till IpRules eller VirtualNetworkRules i egenskapen NetworkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="cfdba-110">The **Add-AzureRmStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="cfdba-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cfdba-111">EXAMPLES</span></span>

### <span data-ttu-id="cfdba-112">Exempel 1: lägga till flera IpRules med IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="cfdba-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="cfdba-113">Det här kommandot lägger till flera IpRules med IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="cfdba-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="cfdba-114">Exempel 2: lägga till en VirtualNetworkRule med VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="cfdba-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzureRmVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzureRmVirtualNetworkSubnetConfig
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="cfdba-115">Det här kommandot lägger till en VirtualNetworkRule med VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="cfdba-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="cfdba-116">Exempel 3: lägga till VirtualNetworkRules med VirtualNetworkRule objekt från ett annat konto</span><span class="sxs-lookup"><span data-stu-id="cfdba-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzureRMStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount1"
PS C:\> Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="cfdba-117">Det här kommandot lägger till VirtualNetworkRules med VirtualNetworkRule-objekt från ett annat konto.</span><span class="sxs-lookup"><span data-stu-id="cfdba-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="cfdba-118">Exempel 4: lägga till flera IpRule med IpRule-objekt, inmatning med JSON</span><span class="sxs-lookup"><span data-stu-id="cfdba-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="cfdba-119">Det här kommandot lägger till flera IpRule med IpRule-objekt, indata med JSON.</span><span class="sxs-lookup"><span data-stu-id="cfdba-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="cfdba-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cfdba-120">PARAMETERS</span></span>

### <span data-ttu-id="cfdba-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cfdba-121">-AsJob</span></span>
<span data-ttu-id="cfdba-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="cfdba-122">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfdba-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfdba-123">-DefaultProfile</span></span>
<span data-ttu-id="cfdba-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cfdba-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfdba-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="cfdba-125">-IPAddressOrRange</span></span>
<span data-ttu-id="cfdba-126">Matrisen med IpAddressOrRange, Lägg till IpRules med inmatnings IpAddressOrRange och standard åtgärden Tillåt NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="cfdba-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

```yaml
Type: String[]
Parameter Sets: IpRuleString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfdba-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="cfdba-127">-IPRule</span></span>
<span data-ttu-id="cfdba-128">Matrisen med IpRule-objekt som ska läggas till i egenskapen NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="cfdba-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

```yaml
Type: PSIpRule[]
Parameter Sets: IpRuleObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfdba-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="cfdba-129">-Name</span></span>
<span data-ttu-id="cfdba-130">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="cfdba-130">Specifies the name of the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfdba-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfdba-131">-ResourceGroupName</span></span>
<span data-ttu-id="cfdba-132">Anger namnet på resurs gruppen som innehåller lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="cfdba-132">Specifies the name of the resource group contains the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfdba-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="cfdba-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="cfdba-134">Matrisen med VirtualNetworkResourceId lägger till VirtualNetworkRule med inmatnings VirtualNetworkResourceId och standard åtgärd Tillåt NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="cfdba-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

```yaml
Type: String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfdba-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cfdba-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="cfdba-136">Matrisen med VirtualNetworkRule-objekt som ska läggas till i egenskapen NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="cfdba-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfdba-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cfdba-137">-Confirm</span></span>
<span data-ttu-id="cfdba-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cfdba-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfdba-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfdba-139">-WhatIf</span></span>
<span data-ttu-id="cfdba-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cfdba-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfdba-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cfdba-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfdba-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfdba-142">CommonParameters</span></span>
<span data-ttu-id="cfdba-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfdba-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfdba-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfdba-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfdba-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cfdba-145">INPUTS</span></span>

### <span data-ttu-id="cfdba-146">System. String</span><span class="sxs-lookup"><span data-stu-id="cfdba-146">System.String</span></span>
<span data-ttu-id="cfdba-147">Microsoft. Azure. commands. Management. Storage. Models. PSIpRule [] Microsoft. Azure. commands. Management. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="cfdba-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="cfdba-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cfdba-148">OUTPUTS</span></span>

### <span data-ttu-id="cfdba-149">Microsoft. Azure. commands. Management. Storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cfdba-149">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>
<span data-ttu-id="cfdba-150">Microsoft. Azure. commands. Management. Storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="cfdba-150">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="cfdba-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cfdba-151">NOTES</span></span>

## <span data-ttu-id="cfdba-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cfdba-152">RELATED LINKS</span></span>

