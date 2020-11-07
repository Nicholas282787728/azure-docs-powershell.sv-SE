---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 7823594993dbf2d276f87136c3909ffe88a85918
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923530"
---
# <span data-ttu-id="3ef29-101">Remove-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3ef29-101">Remove-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="3ef29-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ef29-102">SYNOPSIS</span></span>
<span data-ttu-id="3ef29-103">Ta bort IpRules eller VirtualNetworkRules från egenskapen NetWorkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="3ef29-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="3ef29-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ef29-104">SYNTAX</span></span>

### <span data-ttu-id="3ef29-105">NetWorkRuleString (standard)</span><span class="sxs-lookup"><span data-stu-id="3ef29-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ef29-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="3ef29-106">IpRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ef29-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="3ef29-107">NetworkRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ef29-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="3ef29-108">IpRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ef29-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ef29-109">DESCRIPTION</span></span>
<span data-ttu-id="3ef29-110">Cmdleten **Remove-AzStorageAccountNetworkRule** tar bort IpRules eller VirtualNetworkRules från egenskapen NetWorkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="3ef29-110">The **Remove-AzStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="3ef29-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ef29-111">EXAMPLES</span></span>

### <span data-ttu-id="3ef29-112">Exempel 1: ta bort flera IpRules med IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3ef29-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="3ef29-113">Det här kommandot tar bort flera IpRules med IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="3ef29-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="3ef29-114">Exempel 2: ta bort en VirtualNetworkRule med VirtualNetworkRule indata från JSON</span><span class="sxs-lookup"><span data-stu-id="3ef29-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="3ef29-115">Det här kommandot tar bort en VirtualNetworkRule med VirtualNetworkRule-objekt med JSON.</span><span class="sxs-lookup"><span data-stu-id="3ef29-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="3ef29-116">Exempel 3: ta bort First IpRule med pipeline</span><span class="sxs-lookup"><span data-stu-id="3ef29-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="3ef29-117">Det här kommandot tar bort första IpRule med pipeline.</span><span class="sxs-lookup"><span data-stu-id="3ef29-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="3ef29-118">Exempel 4: ta bort flera VirtualNetworkRules med VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="3ef29-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="3ef29-119">Det här kommandot tar bort flera VirtualNetworkRules med VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="3ef29-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="3ef29-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ef29-120">PARAMETERS</span></span>

### <span data-ttu-id="3ef29-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ef29-121">-AsJob</span></span>
<span data-ttu-id="3ef29-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3ef29-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ef29-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ef29-123">-DefaultProfile</span></span>
<span data-ttu-id="3ef29-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3ef29-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ef29-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3ef29-125">-IPAddressOrRange</span></span>
<span data-ttu-id="3ef29-126">Matrisen med IpAddressOrRange tar bort IpRule med samma IpAddressOrRange från egenskapen NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="3ef29-126">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="3ef29-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="3ef29-127">-IPRule</span></span>
<span data-ttu-id="3ef29-128">Matrisen med IpRule-objekt som ska tas bort från egenskapen NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="3ef29-128">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="3ef29-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="3ef29-129">-Name</span></span>
<span data-ttu-id="3ef29-130">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="3ef29-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="3ef29-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ef29-131">-ResourceGroupName</span></span>
<span data-ttu-id="3ef29-132">Anger namnet på resurs gruppen som innehåller lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="3ef29-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="3ef29-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="3ef29-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="3ef29-134">Matrisen med VirtualNetworkResourceId tar bort VirtualNetworkRule med samma VirtualNetworkResourceId från egenskapen NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="3ef29-134">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="3ef29-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3ef29-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="3ef29-136">Matrisen med VirtualNetworkRule-objekt som ska tas bort från egenskapen NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="3ef29-136">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="3ef29-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3ef29-137">-Confirm</span></span>
<span data-ttu-id="3ef29-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3ef29-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ef29-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ef29-139">-WhatIf</span></span>
<span data-ttu-id="3ef29-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3ef29-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ef29-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3ef29-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ef29-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ef29-142">CommonParameters</span></span>
<span data-ttu-id="3ef29-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ef29-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ef29-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ef29-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ef29-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ef29-145">INPUTS</span></span>

### <span data-ttu-id="3ef29-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3ef29-146">System.String</span></span>

### <span data-ttu-id="3ef29-147">Microsoft. Azure. commands. Management. Storage. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="3ef29-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>
<span data-ttu-id="3ef29-148">Parametrar: IPRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3ef29-148">Parameters: IPRule (ByValue)</span></span>

### <span data-ttu-id="3ef29-149">Microsoft. Azure. commands. Management. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="3ef29-149">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>
<span data-ttu-id="3ef29-150">Parametrar: VirtualNetworkRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3ef29-150">Parameters: VirtualNetworkRule (ByValue)</span></span>

## <span data-ttu-id="3ef29-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ef29-151">OUTPUTS</span></span>

### <span data-ttu-id="3ef29-152">Microsoft. Azure. commands. Management. Storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3ef29-152">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="3ef29-153">Microsoft. Azure. commands. Management. Storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="3ef29-153">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="3ef29-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ef29-154">NOTES</span></span>

## <span data-ttu-id="3ef29-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ef29-155">RELATED LINKS</span></span>
