---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: 3a1d30f3ae44b0e6893682cf0c1d700207682803
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747649"
---
# <span data-ttu-id="97c69-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="97c69-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="97c69-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97c69-102">SYNOPSIS</span></span>
<span data-ttu-id="97c69-103">Uppdaterar en Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="97c69-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="97c69-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97c69-104">SYNTAX</span></span>

### <span data-ttu-id="97c69-105">ByVirtualWanName (standard)</span><span class="sxs-lookup"><span data-stu-id="97c69-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97c69-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="97c69-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97c69-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="97c69-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97c69-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97c69-108">DESCRIPTION</span></span>
<span data-ttu-id="97c69-109">Uppdaterar en Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="97c69-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="97c69-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97c69-110">EXAMPLES</span></span>

### <span data-ttu-id="97c69-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="97c69-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="97c69-112">Ovanstående skapar en resurs grupp "testRG" i området "västra USA" och ett Azure Virtual WAN i den resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="97c69-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="97c69-113">VirtualWan uppdateras med nya egenskaper.</span><span class="sxs-lookup"><span data-stu-id="97c69-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="97c69-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97c69-114">PARAMETERS</span></span>

### <span data-ttu-id="97c69-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="97c69-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="97c69-116">Tillåt gren till gren trafik för VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="97c69-116">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97c69-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="97c69-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="97c69-118">Tillåt VNet till VNet-trafik för VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="97c69-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97c69-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97c69-119">-AsJob</span></span>
<span data-ttu-id="97c69-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="97c69-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97c69-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97c69-121">-DefaultProfile</span></span>
<span data-ttu-id="97c69-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="97c69-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97c69-123">-Force</span><span class="sxs-lookup"><span data-stu-id="97c69-123">-Force</span></span>
<span data-ttu-id="97c69-124">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="97c69-124">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="97c69-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97c69-125">-InputObject</span></span>
<span data-ttu-id="97c69-126">Det virtuella WAN-objektet som ska ändras</span><span class="sxs-lookup"><span data-stu-id="97c69-126">The virtual wan object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97c69-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="97c69-127">-Name</span></span>
<span data-ttu-id="97c69-128">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="97c69-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97c69-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97c69-129">-ResourceGroupName</span></span>
<span data-ttu-id="97c69-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="97c69-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97c69-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97c69-131">-ResourceId</span></span>
<span data-ttu-id="97c69-132">Azure Resource ID för den virtuella WAN-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="97c69-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97c69-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="97c69-133">-Tag</span></span>
<span data-ttu-id="97c69-134">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="97c69-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97c69-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="97c69-135">-Confirm</span></span>
<span data-ttu-id="97c69-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="97c69-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97c69-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97c69-137">-WhatIf</span></span>
<span data-ttu-id="97c69-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="97c69-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97c69-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="97c69-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97c69-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97c69-140">CommonParameters</span></span>
<span data-ttu-id="97c69-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97c69-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97c69-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97c69-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97c69-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97c69-143">INPUTS</span></span>

### <span data-ttu-id="97c69-144">Microsoft. Azure. commands. Networks. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="97c69-144">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="97c69-145">System. String</span><span class="sxs-lookup"><span data-stu-id="97c69-145">System.String</span></span>

## <span data-ttu-id="97c69-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97c69-146">OUTPUTS</span></span>

### <span data-ttu-id="97c69-147">Microsoft. Azure. commands. Networks. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="97c69-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="97c69-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97c69-148">NOTES</span></span>

## <span data-ttu-id="97c69-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97c69-149">RELATED LINKS</span></span>

[<span data-ttu-id="97c69-150">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="97c69-150">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="97c69-151">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="97c69-151">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="97c69-152">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="97c69-152">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)
