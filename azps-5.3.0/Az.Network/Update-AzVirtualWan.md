---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: e93bcc320f14a8311a29c6be9824da16506ea499
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525724"
---
# <span data-ttu-id="82454-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="82454-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="82454-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82454-102">SYNOPSIS</span></span>
<span data-ttu-id="82454-103">Uppdaterar en Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="82454-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="82454-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82454-104">SYNTAX</span></span>

### <span data-ttu-id="82454-105">ByVirtualWanName (standard)</span><span class="sxs-lookup"><span data-stu-id="82454-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82454-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="82454-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82454-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="82454-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82454-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82454-108">DESCRIPTION</span></span>
<span data-ttu-id="82454-109">Uppdaterar en Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="82454-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="82454-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82454-110">EXAMPLES</span></span>

### <span data-ttu-id="82454-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="82454-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="82454-112">Ovanstående skapar en resurs grupp "testRG" i området "västra USA" och ett Azure Virtual WAN i den resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="82454-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="82454-113">VirtualWan uppdateras med nya egenskaper.</span><span class="sxs-lookup"><span data-stu-id="82454-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="82454-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82454-114">PARAMETERS</span></span>

### <span data-ttu-id="82454-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="82454-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="82454-116">Tillåt gren till gren trafik för VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="82454-116">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82454-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="82454-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="82454-118">Tillåt VNet till VNet-trafik för VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="82454-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82454-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82454-119">-AsJob</span></span>
<span data-ttu-id="82454-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="82454-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="82454-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82454-121">-DefaultProfile</span></span>
<span data-ttu-id="82454-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="82454-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82454-123">-Force</span><span class="sxs-lookup"><span data-stu-id="82454-123">-Force</span></span>
<span data-ttu-id="82454-124">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="82454-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="82454-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82454-125">-InputObject</span></span>
<span data-ttu-id="82454-126">Det virtuella WAN-objektet som ska ändras</span><span class="sxs-lookup"><span data-stu-id="82454-126">The virtual wan object to be modified</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82454-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="82454-127">-Name</span></span>
<span data-ttu-id="82454-128">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="82454-128">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82454-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82454-129">-ResourceGroupName</span></span>
<span data-ttu-id="82454-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="82454-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82454-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82454-131">-ResourceId</span></span>
<span data-ttu-id="82454-132">Azure Resource ID för den virtuella WAN-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="82454-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82454-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="82454-133">-Tag</span></span>
<span data-ttu-id="82454-134">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="82454-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82454-135">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="82454-135">-VirtualWANType</span></span>
<span data-ttu-id="82454-136">Typen av virtuellt WAN.</span><span class="sxs-lookup"><span data-stu-id="82454-136">The type of the Virtual Wan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82454-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="82454-137">-Confirm</span></span>
<span data-ttu-id="82454-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="82454-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82454-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82454-139">-WhatIf</span></span>
<span data-ttu-id="82454-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="82454-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82454-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="82454-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82454-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82454-142">CommonParameters</span></span>
<span data-ttu-id="82454-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82454-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82454-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82454-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82454-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82454-145">INPUTS</span></span>

### <span data-ttu-id="82454-146">Microsoft. Azure. commands. Networks. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="82454-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="82454-147">System. String</span><span class="sxs-lookup"><span data-stu-id="82454-147">System.String</span></span>

## <span data-ttu-id="82454-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82454-148">OUTPUTS</span></span>

### <span data-ttu-id="82454-149">Microsoft. Azure. commands. Networks. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="82454-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="82454-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82454-150">NOTES</span></span>

## <span data-ttu-id="82454-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82454-151">RELATED LINKS</span></span>

[<span data-ttu-id="82454-152">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="82454-152">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="82454-153">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="82454-153">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="82454-154">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="82454-154">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)
