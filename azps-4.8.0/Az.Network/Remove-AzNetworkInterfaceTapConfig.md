---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 52fc2a3c84c70d52c173bc256ca2b0d952307e91
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258188"
---
# <span data-ttu-id="e18f6-101">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e18f6-101">Remove-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="e18f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e18f6-102">SYNOPSIS</span></span>
<span data-ttu-id="e18f6-103">Tar bort en tryck konfiguration från angivet nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="e18f6-103">Removes a tap configuration from given network interface</span></span>

## <span data-ttu-id="e18f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e18f6-104">SYNTAX</span></span>

### <span data-ttu-id="e18f6-105">RemoveByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e18f6-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e18f6-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e18f6-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e18f6-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e18f6-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e18f6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e18f6-108">DESCRIPTION</span></span>
<span data-ttu-id="e18f6-109">Cmdleten **Remove-AzNetworkInterfaceTapConfig** tar bort en Azure knackning-konfiguration från en lista med nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="e18f6-109">The **Remove-AzNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="e18f6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e18f6-110">EXAMPLES</span></span>

### <span data-ttu-id="e18f6-111">Exempel 1: ta bort en tryck konfiguration</span><span class="sxs-lookup"><span data-stu-id="e18f6-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="e18f6-112">Det här kommandot tar bort TapConfiguration från NetworkInterface1 i en resurs grupp ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="e18f6-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="e18f6-113">Eftersom *Force* -parametern inte används uppmanas användaren att bekräfta åtgärden.</span><span class="sxs-lookup"><span data-stu-id="e18f6-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="e18f6-114">Exempel 2: ta bort ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="e18f6-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="e18f6-115">Det här kommandot tar bort TapConfiguration från NetworkInterface1 i en resurs grupp ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="e18f6-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="e18f6-116">Eftersom *Force* -parametern används uppmanas användaren inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="e18f6-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="e18f6-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e18f6-117">PARAMETERS</span></span>

### <span data-ttu-id="e18f6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e18f6-118">-DefaultProfile</span></span>
<span data-ttu-id="e18f6-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e18f6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e18f6-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e18f6-120">-Force</span></span>
<span data-ttu-id="e18f6-121">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e18f6-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e18f6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e18f6-122">-InputObject</span></span>
<span data-ttu-id="e18f6-123">Referens till NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="e18f6-123">Reference to NetworkInterfaceTapConfig.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e18f6-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="e18f6-124">-Name</span></span>
<span data-ttu-id="e18f6-125">Namn på peering med virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="e18f6-125">The virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e18f6-126">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="e18f6-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="e18f6-127">Det virtuella nätverks namnet.</span><span class="sxs-lookup"><span data-stu-id="e18f6-127">The virtual network name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e18f6-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e18f6-128">-PassThru</span></span>
<span data-ttu-id="e18f6-129">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="e18f6-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e18f6-130">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="e18f6-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e18f6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e18f6-131">-ResourceGroupName</span></span>
<span data-ttu-id="e18f6-132">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="e18f6-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e18f6-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e18f6-133">-ResourceId</span></span>
<span data-ttu-id="e18f6-134">NetworkInterfaceTapConfig resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="e18f6-134">NetworkInterfaceTapConfig resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e18f6-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e18f6-135">-Confirm</span></span>
<span data-ttu-id="e18f6-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e18f6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e18f6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e18f6-137">-WhatIf</span></span>
<span data-ttu-id="e18f6-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e18f6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e18f6-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e18f6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e18f6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e18f6-140">CommonParameters</span></span>
<span data-ttu-id="e18f6-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e18f6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e18f6-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e18f6-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e18f6-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e18f6-143">INPUTS</span></span>

### <span data-ttu-id="e18f6-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e18f6-144">System.String</span></span>

### <span data-ttu-id="e18f6-145">Microsoft. Azure. commands. Networks. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="e18f6-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="e18f6-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e18f6-146">OUTPUTS</span></span>

### <span data-ttu-id="e18f6-147">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e18f6-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="e18f6-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e18f6-148">NOTES</span></span>

## <span data-ttu-id="e18f6-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e18f6-149">RELATED LINKS</span></span>

[<span data-ttu-id="e18f6-150">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e18f6-150">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="e18f6-151">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e18f6-151">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="e18f6-152">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e18f6-152">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)