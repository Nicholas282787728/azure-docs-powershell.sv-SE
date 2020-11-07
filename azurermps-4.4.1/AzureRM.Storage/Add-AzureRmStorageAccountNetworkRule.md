---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageAccountNetworkRule.md
ms.openlocfilehash: 9f8d098cb27532980b01cf46da6c83d4da30ed48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756320"
---
# <span data-ttu-id="fa564-101">Add-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fa564-101">Add-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="fa564-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fa564-102">SYNOPSIS</span></span>
 <span data-ttu-id="fa564-103">Lägga till IpRules eller VirtualNetworkRules till egenskapen NetworkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="fa564-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa564-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fa564-104">SYNTAX</span></span>

### <span data-ttu-id="fa564-105">NetWorkRuleString (standard)</span><span class="sxs-lookup"><span data-stu-id="fa564-105">NetWorkRuleString (Default)</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa564-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="fa564-106">IpRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa564-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="fa564-107">NetworkRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa564-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="fa564-108">IpRuleString</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa564-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fa564-109">DESCRIPTION</span></span>
<span data-ttu-id="fa564-110">Cmdleten **Add-AzureRmStorageAccountNetworkRule** lägger till IpRules eller VirtualNetworkRules i egenskapen NetworkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="fa564-110">The **Add-AzureRmStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage Account</span></span>

## <span data-ttu-id="fa564-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fa564-111">EXAMPLES</span></span>

### <span data-ttu-id="fa564-112">Exempel 1: lägga till flera IpRules med IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="fa564-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="fa564-113">Det här kommandot lägger till flera IpRules med IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="fa564-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="fa564-114">Exempel 2: lägga till en VirtualNetworkRule med VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="fa564-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzureRmVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzureRmVirtualNetworkSubnetConfig
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="fa564-115">Det här kommandot lägger till en VirtualNetworkRule med VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="fa564-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="fa564-116">Exempel 3: lägga till VirtualNetworkRules med VirtualNetworkRule objekt från ett annat konto</span><span class="sxs-lookup"><span data-stu-id="fa564-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzureRMStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount1"
PS C:\> Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="fa564-117">Det här kommandot lägger till VirtualNetworkRules med VirtualNetworkRule-objekt från ett annat konto.</span><span class="sxs-lookup"><span data-stu-id="fa564-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="fa564-118">Exempel 4: lägga till flera IpRule med IpRule-objekt, inmatning med JSON</span><span class="sxs-lookup"><span data-stu-id="fa564-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="fa564-119">Det här kommandot lägger till flera IpRule med IpRule-objekt, indata med JSON.</span><span class="sxs-lookup"><span data-stu-id="fa564-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="fa564-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fa564-120">PARAMETERS</span></span>

### <span data-ttu-id="fa564-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="fa564-121">-IPAddressOrRange</span></span>
<span data-ttu-id="fa564-122">Matrisen med IpAddressOrRange, Lägg till IpRules med inmatnings IpAddressOrRange och standard åtgärden Tillåt NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="fa564-122">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="fa564-123">-IPRule</span><span class="sxs-lookup"><span data-stu-id="fa564-123">-IPRule</span></span>
<span data-ttu-id="fa564-124">Matrisen med IpRule-objekt som ska läggas till i egenskapen NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="fa564-124">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="fa564-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="fa564-125">-Name</span></span>
<span data-ttu-id="fa564-126">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="fa564-126">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="fa564-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa564-127">-ResourceGroupName</span></span>
<span data-ttu-id="fa564-128">Anger namnet på resurs gruppen som innehåller lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="fa564-128">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="fa564-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="fa564-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="fa564-130">Matrisen med VirtualNetworkResourceId lägger till VirtualNetworkRule med inmatnings VirtualNetworkResourceId och standard åtgärd Tillåt NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="fa564-130">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="fa564-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fa564-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="fa564-132">Matrisen med VirtualNetworkRule-objekt som ska läggas till i egenskapen NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="fa564-132">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="fa564-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fa564-133">-Confirm</span></span>
<span data-ttu-id="fa564-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fa564-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa564-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa564-135">-WhatIf</span></span>
<span data-ttu-id="fa564-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fa564-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa564-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fa564-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa564-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa564-138">-DefaultProfile</span></span>
<span data-ttu-id="fa564-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fa564-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa564-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa564-140">CommonParameters</span></span>
<span data-ttu-id="fa564-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa564-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa564-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa564-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa564-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fa564-143">INPUTS</span></span>

### <span data-ttu-id="fa564-144">System. String</span><span class="sxs-lookup"><span data-stu-id="fa564-144">System.String</span></span>
<span data-ttu-id="fa564-145">Microsoft. Azure. commands. Management. Storage. Models. PSIpRule [] Microsoft. Azure. commands. Management. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="fa564-145">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="fa564-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fa564-146">OUTPUTS</span></span>

### <span data-ttu-id="fa564-147">Microsoft. Azure. commands. Management. Storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fa564-147">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>
<span data-ttu-id="fa564-148">Microsoft. Azure. commands. Management. Storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="fa564-148">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="fa564-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fa564-149">NOTES</span></span>

## <span data-ttu-id="fa564-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fa564-150">RELATED LINKS</span></span>

