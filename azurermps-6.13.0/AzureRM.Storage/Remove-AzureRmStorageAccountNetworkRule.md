---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccountNetworkRule.md
ms.openlocfilehash: 73f096c516bb285b89e45d90107ff6a3ad406dbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757818"
---
# <span data-ttu-id="8a884-101">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8a884-101">Remove-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="8a884-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a884-102">SYNOPSIS</span></span>
<span data-ttu-id="8a884-103">Ta bort IpRules eller VirtualNetworkRules från egenskapen NetWorkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="8a884-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a884-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a884-104">SYNTAX</span></span>

### <span data-ttu-id="8a884-105">NetWorkRuleString (standard)</span><span class="sxs-lookup"><span data-stu-id="8a884-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a884-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="8a884-106">IpRuleObject</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a884-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="8a884-107">NetworkRuleObject</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a884-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="8a884-108">IpRuleString</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a884-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a884-109">DESCRIPTION</span></span>
<span data-ttu-id="8a884-110">Cmdleten **Remove-AzureRmStorageAccountNetworkRule** tar bort IpRules eller VirtualNetworkRules från egenskapen NetWorkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="8a884-110">The **Remove-AzureRmStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="8a884-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a884-111">EXAMPLES</span></span>

### <span data-ttu-id="8a884-112">Exempel 1: ta bort flera IpRules med IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="8a884-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="8a884-113">Det här kommandot tar bort flera IpRules med IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="8a884-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="8a884-114">Exempel 2: ta bort en VirtualNetworkRule med VirtualNetworkRule indata från JSON</span><span class="sxs-lookup"><span data-stu-id="8a884-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="8a884-115">Det här kommandot tar bort en VirtualNetworkRule med VirtualNetworkRule-objekt med JSON.</span><span class="sxs-lookup"><span data-stu-id="8a884-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="8a884-116">Exempel 3: ta bort First IpRule med pipeline</span><span class="sxs-lookup"><span data-stu-id="8a884-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="8a884-117">Det här kommandot tar bort första IpRule med pipeline.</span><span class="sxs-lookup"><span data-stu-id="8a884-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="8a884-118">Exempel 4: ta bort flera VirtualNetworkRules med VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="8a884-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="8a884-119">Det här kommandot tar bort flera VirtualNetworkRules med VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="8a884-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="8a884-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a884-120">PARAMETERS</span></span>

### <span data-ttu-id="8a884-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a884-121">-AsJob</span></span>
<span data-ttu-id="8a884-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="8a884-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a884-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a884-123">-DefaultProfile</span></span>
<span data-ttu-id="8a884-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8a884-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a884-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="8a884-125">-IPAddressOrRange</span></span>
<span data-ttu-id="8a884-126">Matrisen med IpAddressOrRange tar bort IpRule med samma IpAddressOrRange från egenskapen NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="8a884-126">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="8a884-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="8a884-127">-IPRule</span></span>
<span data-ttu-id="8a884-128">Matrisen med IpRule-objekt som ska tas bort från egenskapen NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="8a884-128">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="8a884-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="8a884-129">-Name</span></span>
<span data-ttu-id="8a884-130">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="8a884-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="8a884-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a884-131">-ResourceGroupName</span></span>
<span data-ttu-id="8a884-132">Anger namnet på resurs gruppen som innehåller lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="8a884-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="8a884-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="8a884-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="8a884-134">Matrisen med VirtualNetworkResourceId tar bort VirtualNetworkRule med samma VirtualNetworkResourceId från egenskapen NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="8a884-134">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="8a884-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8a884-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="8a884-136">Matrisen med VirtualNetworkRule-objekt som ska tas bort från egenskapen NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="8a884-136">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="8a884-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8a884-137">-Confirm</span></span>
<span data-ttu-id="8a884-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8a884-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a884-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a884-139">-WhatIf</span></span>
<span data-ttu-id="8a884-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8a884-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a884-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8a884-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a884-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a884-142">CommonParameters</span></span>
<span data-ttu-id="8a884-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a884-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a884-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a884-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a884-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a884-145">INPUTS</span></span>

### <span data-ttu-id="8a884-146">System. String</span><span class="sxs-lookup"><span data-stu-id="8a884-146">System.String</span></span>

### <span data-ttu-id="8a884-147">Microsoft. Azure. commands. Management. Storage. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="8a884-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>
<span data-ttu-id="8a884-148">Parametrar: IPRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8a884-148">Parameters: IPRule (ByValue)</span></span>

### <span data-ttu-id="8a884-149">Microsoft. Azure. commands. Management. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="8a884-149">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>
<span data-ttu-id="8a884-150">Parametrar: VirtualNetworkRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8a884-150">Parameters: VirtualNetworkRule (ByValue)</span></span>

## <span data-ttu-id="8a884-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a884-151">OUTPUTS</span></span>

### <span data-ttu-id="8a884-152">Microsoft. Azure. commands. Management. Storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8a884-152">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="8a884-153">Microsoft. Azure. commands. Management. Storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="8a884-153">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="8a884-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a884-154">NOTES</span></span>

## <span data-ttu-id="8a884-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a884-155">RELATED LINKS</span></span>
