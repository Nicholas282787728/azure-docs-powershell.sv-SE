---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccountNetworkRule.md
ms.openlocfilehash: abfd6f06a0d3f81c84f79e4a5fa6870ad60ba18d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756319"
---
# <span data-ttu-id="ab006-101">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ab006-101">Remove-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="ab006-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab006-102">SYNOPSIS</span></span>
<span data-ttu-id="ab006-103">Ta bort IpRules eller VirtualNetworkRules från egenskapen NetWorkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="ab006-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab006-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab006-104">SYNTAX</span></span>

### <span data-ttu-id="ab006-105">NetWorkRuleString (standard)</span><span class="sxs-lookup"><span data-stu-id="ab006-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab006-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="ab006-106">IpRuleObject</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab006-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="ab006-107">NetworkRuleObject</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab006-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="ab006-108">IpRuleString</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab006-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab006-109">DESCRIPTION</span></span>
<span data-ttu-id="ab006-110">Cmdleten **Remove-AzureRmStorageAccountNetworkRule** tar bort IpRules eller VirtualNetworkRules från egenskapen NetWorkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="ab006-110">The **Remove-AzureRmStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage Account</span></span>

## <span data-ttu-id="ab006-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab006-111">EXAMPLES</span></span>

### <span data-ttu-id="ab006-112">Exempel 1: ta bort flera IpRules med IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="ab006-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="ab006-113">Det här kommandot tar bort flera IpRules med IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="ab006-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="ab006-114">Exempel 2: ta bort en VirtualNetworkRule med VirtualNetworkRule indata från JSON</span><span class="sxs-lookup"><span data-stu-id="ab006-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="ab006-115">Det här kommandot tar bort en VirtualNetworkRule med VirtualNetworkRule-objekt med JSON.</span><span class="sxs-lookup"><span data-stu-id="ab006-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="ab006-116">Exempel 3: ta bort First IpRule med pipeline</span><span class="sxs-lookup"><span data-stu-id="ab006-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount").IpRules[0] | Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="ab006-117">Det här kommandot tar bort första IpRule med pipeline.</span><span class="sxs-lookup"><span data-stu-id="ab006-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="ab006-118">Exempel 4: ta bort flera VirtualNetworkRules med VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="ab006-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="ab006-119">Det här kommandot tar bort flera VirtualNetworkRules med VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="ab006-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="ab006-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab006-120">PARAMETERS</span></span>

### <span data-ttu-id="ab006-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="ab006-121">-IPAddressOrRange</span></span>
<span data-ttu-id="ab006-122">Matrisen med IpAddressOrRange tar bort IpRule med samma IpAddressOrRange från egenskapen NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="ab006-122">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="ab006-123">-IPRule</span><span class="sxs-lookup"><span data-stu-id="ab006-123">-IPRule</span></span>
<span data-ttu-id="ab006-124">Matrisen med IpRule-objekt som ska tas bort från egenskapen NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="ab006-124">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="ab006-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="ab006-125">-Name</span></span>
<span data-ttu-id="ab006-126">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="ab006-126">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="ab006-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab006-127">-ResourceGroupName</span></span>
<span data-ttu-id="ab006-128">Anger namnet på resurs gruppen som innehåller lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="ab006-128">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="ab006-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="ab006-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="ab006-130">Matrisen med VirtualNetworkResourceId tar bort VirtualNetworkRule med samma VirtualNetworkResourceId från egenskapen NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="ab006-130">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="ab006-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ab006-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="ab006-132">Matrisen med VirtualNetworkRule-objekt som ska tas bort från egenskapen NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="ab006-132">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="ab006-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ab006-133">-Confirm</span></span>
<span data-ttu-id="ab006-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ab006-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab006-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab006-135">-WhatIf</span></span>
<span data-ttu-id="ab006-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ab006-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab006-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ab006-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab006-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab006-138">-DefaultProfile</span></span>
<span data-ttu-id="ab006-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ab006-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab006-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab006-140">CommonParameters</span></span>
<span data-ttu-id="ab006-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab006-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab006-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab006-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab006-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab006-143">INPUTS</span></span>

### <span data-ttu-id="ab006-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ab006-144">System.String</span></span>
<span data-ttu-id="ab006-145">Microsoft. Azure. commands. Management. Storage. Models. PSIpRule [] Microsoft. Azure. commands. Management. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="ab006-145">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="ab006-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab006-146">OUTPUTS</span></span>

### <span data-ttu-id="ab006-147">Microsoft. Azure. commands. Management. Storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ab006-147">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>
<span data-ttu-id="ab006-148">Microsoft. Azure. commands. Management. Storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="ab006-148">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="ab006-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab006-149">NOTES</span></span>

## <span data-ttu-id="ab006-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab006-150">RELATED LINKS</span></span>

