---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 8ad89a0f5fad61fea2ba898ea17f63b6f935ae84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747871"
---
# <span data-ttu-id="aaa1e-101">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="aaa1e-101">Remove-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="aaa1e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aaa1e-102">SYNOPSIS</span></span>
<span data-ttu-id="aaa1e-103">Tar bort en tryck konfiguration från angivet nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="aaa1e-103">Removes a tap configuration from given network interface</span></span>

## <span data-ttu-id="aaa1e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aaa1e-104">SYNTAX</span></span>

### <span data-ttu-id="aaa1e-105">RemoveByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="aaa1e-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaa1e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aaa1e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaa1e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aaa1e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaa1e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aaa1e-108">DESCRIPTION</span></span>
<span data-ttu-id="aaa1e-109">Cmdleten **Remove-AzNetworkInterfaceTapConfig** tar bort en Azure knackning-konfiguration från en lista med nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-109">The **Remove-AzNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="aaa1e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aaa1e-110">EXAMPLES</span></span>

### <span data-ttu-id="aaa1e-111">Exempel 1: ta bort en tryck konfiguration</span><span class="sxs-lookup"><span data-stu-id="aaa1e-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="aaa1e-112">Det här kommandot tar bort TapConfiguration från NetworkInterface1 i en resurs grupp ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="aaa1e-113">Eftersom *Force* -parametern inte används uppmanas användaren att bekräfta åtgärden.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="aaa1e-114">Exempel 2: ta bort ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="aaa1e-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="aaa1e-115">Det här kommandot tar bort TapConfiguration från NetworkInterface1 i en resurs grupp ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="aaa1e-116">Eftersom *Force* -parametern används uppmanas användaren inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="aaa1e-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aaa1e-117">PARAMETERS</span></span>

### <span data-ttu-id="aaa1e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaa1e-118">-DefaultProfile</span></span>
<span data-ttu-id="aaa1e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaa1e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="aaa1e-120">-Force</span></span>
<span data-ttu-id="aaa1e-121">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="aaa1e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aaa1e-122">-InputObject</span></span>
<span data-ttu-id="aaa1e-123">Referens till NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-123">Reference to NetworkInterfaceTapConfig.</span></span>

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

### <span data-ttu-id="aaa1e-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="aaa1e-124">-Name</span></span>
<span data-ttu-id="aaa1e-125">Namn på peering med virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-125">The virtual network peering name.</span></span>

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

### <span data-ttu-id="aaa1e-126">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="aaa1e-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="aaa1e-127">Det virtuella nätverks namnet.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-127">The virtual network name.</span></span>

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

### <span data-ttu-id="aaa1e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aaa1e-128">-PassThru</span></span>
<span data-ttu-id="aaa1e-129">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="aaa1e-130">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="aaa1e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaa1e-131">-ResourceGroupName</span></span>
<span data-ttu-id="aaa1e-132">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-132">The resource group name.</span></span>

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

### <span data-ttu-id="aaa1e-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aaa1e-133">-ResourceId</span></span>
<span data-ttu-id="aaa1e-134">NetworkInterfaceTapConfig resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-134">NetworkInterfaceTapConfig resource id.</span></span>

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

### <span data-ttu-id="aaa1e-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="aaa1e-135">-Confirm</span></span>
<span data-ttu-id="aaa1e-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaa1e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaa1e-137">-WhatIf</span></span>
<span data-ttu-id="aaa1e-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaa1e-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaa1e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaa1e-140">CommonParameters</span></span>
<span data-ttu-id="aaa1e-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaa1e-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaa1e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaa1e-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aaa1e-143">INPUTS</span></span>

### <span data-ttu-id="aaa1e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="aaa1e-144">System.String</span></span>

### <span data-ttu-id="aaa1e-145">Microsoft. Azure. commands. Networks. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="aaa1e-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="aaa1e-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aaa1e-146">OUTPUTS</span></span>

### <span data-ttu-id="aaa1e-147">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="aaa1e-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="aaa1e-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aaa1e-148">NOTES</span></span>

## <span data-ttu-id="aaa1e-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aaa1e-149">RELATED LINKS</span></span>

[<span data-ttu-id="aaa1e-150">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="aaa1e-150">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="aaa1e-151">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="aaa1e-151">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="aaa1e-152">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="aaa1e-152">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
