---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
ms.openlocfilehash: 0215a05db7e18dad9aeb26476d7076bdc556b021
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747809"
---
# <span data-ttu-id="bcbf4-101">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="bcbf4-101">Remove-AzVpnSite</span></span>

## <span data-ttu-id="bcbf4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bcbf4-102">SYNOPSIS</span></span>
<span data-ttu-id="bcbf4-103">Tar bort en Azure VpnSite-resurs.</span><span class="sxs-lookup"><span data-stu-id="bcbf4-103">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="bcbf4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bcbf4-104">SYNTAX</span></span>

### <span data-ttu-id="bcbf4-105">ByVpnSiteName (standard)</span><span class="sxs-lookup"><span data-stu-id="bcbf4-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcbf4-106">ByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="bcbf4-106">ByVpnSiteObject</span></span>
```
Remove-AzVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcbf4-107">ByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="bcbf4-107">ByVpnSiteResourceId</span></span>
```
Remove-AzVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcbf4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bcbf4-108">DESCRIPTION</span></span>
<span data-ttu-id="bcbf4-109">Tar bort en Azure VpnSite-resurs.</span><span class="sxs-lookup"><span data-stu-id="bcbf4-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="bcbf4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bcbf4-110">EXAMPLES</span></span>

### <span data-ttu-id="bcbf4-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bcbf4-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="bcbf4-112">Ovanstående skapar en resurs grupp, virtuellt WAN i West-resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="bcbf4-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="bcbf4-113">Därefter skapas en VpnSite för att representera en kund gren och länkar den till den virtuella WAN-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bcbf4-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="bcbf4-114">När webbplatsen har skapats tas den omedelbart bort med kommandot Remove-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="bcbf4-114">Once the site is created, it is immediately removed using the Remove-AzVpnSite command.</span></span>

### <span data-ttu-id="bcbf4-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="bcbf4-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzVpnSite
```

<span data-ttu-id="bcbf4-116">Samma som i exempel 1 men här tar borttagningen med piped från get-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="bcbf4-116">Same as example 1 but here the removal happens using the piped output from Get-AzVpnSite.</span></span>

## <span data-ttu-id="bcbf4-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bcbf4-117">PARAMETERS</span></span>

### <span data-ttu-id="bcbf4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcbf4-118">-DefaultProfile</span></span>
<span data-ttu-id="bcbf4-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bcbf4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcbf4-120">-Force</span><span class="sxs-lookup"><span data-stu-id="bcbf4-120">-Force</span></span>
<span data-ttu-id="bcbf4-121">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="bcbf4-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bcbf4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcbf4-122">-InputObject</span></span>
<span data-ttu-id="bcbf4-123">VpnSite-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="bcbf4-123">The vpnSite object to be deleted.</span></span>

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

### <span data-ttu-id="bcbf4-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="bcbf4-124">-Name</span></span>
<span data-ttu-id="bcbf4-125">VpnSite namn.</span><span class="sxs-lookup"><span data-stu-id="bcbf4-125">The vpnSite name.</span></span>

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

### <span data-ttu-id="bcbf4-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bcbf4-126">-PassThru</span></span>
<span data-ttu-id="bcbf4-127">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="bcbf4-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="bcbf4-128">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="bcbf4-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bcbf4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcbf4-129">-ResourceGroupName</span></span>
<span data-ttu-id="bcbf4-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="bcbf4-130">The resource group name.</span></span>

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

### <span data-ttu-id="bcbf4-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcbf4-131">-ResourceId</span></span>
<span data-ttu-id="bcbf4-132">Azure Resource ID för vpnSite ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="bcbf4-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

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

### <span data-ttu-id="bcbf4-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bcbf4-133">-Confirm</span></span>
<span data-ttu-id="bcbf4-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bcbf4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcbf4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcbf4-135">-WhatIf</span></span>
<span data-ttu-id="bcbf4-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bcbf4-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bcbf4-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bcbf4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcbf4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcbf4-138">CommonParameters</span></span>
<span data-ttu-id="bcbf4-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcbf4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcbf4-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcbf4-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcbf4-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bcbf4-141">INPUTS</span></span>

### <span data-ttu-id="bcbf4-142">Microsoft. Azure. commands. Networks. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="bcbf4-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="bcbf4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="bcbf4-143">System.String</span></span>

## <span data-ttu-id="bcbf4-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bcbf4-144">OUTPUTS</span></span>

### <span data-ttu-id="bcbf4-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bcbf4-145">System.Boolean</span></span>

## <span data-ttu-id="bcbf4-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bcbf4-146">NOTES</span></span>

## <span data-ttu-id="bcbf4-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bcbf4-147">RELATED LINKS</span></span>

[<span data-ttu-id="bcbf4-148">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="bcbf4-148">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="bcbf4-149">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="bcbf4-149">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="bcbf4-150">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="bcbf4-150">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
