---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
ms.openlocfilehash: 9b9ab59496ff52be2dc8ca538ea044ec34c34970
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272049"
---
# <span data-ttu-id="35752-101">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="35752-101">Remove-AzVpnSite</span></span>

## <span data-ttu-id="35752-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="35752-102">SYNOPSIS</span></span>
<span data-ttu-id="35752-103">Tar bort en Azure VpnSite-resurs.</span><span class="sxs-lookup"><span data-stu-id="35752-103">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="35752-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="35752-104">SYNTAX</span></span>

### <span data-ttu-id="35752-105">ByVpnSiteName (standard)</span><span class="sxs-lookup"><span data-stu-id="35752-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35752-106">ByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="35752-106">ByVpnSiteObject</span></span>
```
Remove-AzVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35752-107">ByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="35752-107">ByVpnSiteResourceId</span></span>
```
Remove-AzVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35752-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="35752-108">DESCRIPTION</span></span>
<span data-ttu-id="35752-109">Tar bort en Azure VpnSite-resurs.</span><span class="sxs-lookup"><span data-stu-id="35752-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="35752-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="35752-110">EXAMPLES</span></span>

### <span data-ttu-id="35752-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="35752-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="35752-112">Ovanstående skapar en resurs grupp, virtuellt WAN i West-resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="35752-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="35752-113">Därefter skapas en VpnSite för att representera en kund gren och länkar den till den virtuella WAN-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="35752-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="35752-114">När webbplatsen har skapats tas den omedelbart bort med kommandot Remove-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="35752-114">Once the site is created, it is immediately removed using the Remove-AzVpnSite command.</span></span>

### <span data-ttu-id="35752-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="35752-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzVpnSite
```

<span data-ttu-id="35752-116">Samma som i exempel 1 men här tar borttagningen med piped från get-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="35752-116">Same as example 1 but here the removal happens using the piped output from Get-AzVpnSite.</span></span>

## <span data-ttu-id="35752-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="35752-117">PARAMETERS</span></span>

### <span data-ttu-id="35752-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35752-118">-DefaultProfile</span></span>
<span data-ttu-id="35752-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="35752-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35752-120">-Force</span><span class="sxs-lookup"><span data-stu-id="35752-120">-Force</span></span>
<span data-ttu-id="35752-121">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="35752-121">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35752-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35752-122">-InputObject</span></span>
<span data-ttu-id="35752-123">VpnSite-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="35752-123">The vpnSite object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnSiteObject
Aliases: VpnSite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35752-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="35752-124">-Name</span></span>
<span data-ttu-id="35752-125">VpnSite namn.</span><span class="sxs-lookup"><span data-stu-id="35752-125">The vpnSite name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteName
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35752-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35752-126">-PassThru</span></span>
<span data-ttu-id="35752-127">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="35752-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="35752-128">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="35752-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35752-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35752-129">-ResourceGroupName</span></span>
<span data-ttu-id="35752-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="35752-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35752-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35752-131">-ResourceId</span></span>
<span data-ttu-id="35752-132">Azure Resource ID för vpnSite ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="35752-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteResourceId
Aliases: VpnSiteId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35752-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="35752-133">-Confirm</span></span>
<span data-ttu-id="35752-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="35752-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35752-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35752-135">-WhatIf</span></span>
<span data-ttu-id="35752-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="35752-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35752-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="35752-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35752-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35752-138">CommonParameters</span></span>
<span data-ttu-id="35752-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35752-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35752-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35752-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35752-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="35752-141">INPUTS</span></span>

### <span data-ttu-id="35752-142">Microsoft. Azure. commands. Networks. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="35752-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="35752-143">System. String</span><span class="sxs-lookup"><span data-stu-id="35752-143">System.String</span></span>

## <span data-ttu-id="35752-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="35752-144">OUTPUTS</span></span>

### <span data-ttu-id="35752-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="35752-145">System.Boolean</span></span>

## <span data-ttu-id="35752-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="35752-146">NOTES</span></span>

## <span data-ttu-id="35752-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="35752-147">RELATED LINKS</span></span>

[<span data-ttu-id="35752-148">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="35752-148">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="35752-149">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="35752-149">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="35752-150">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="35752-150">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)