---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/Remove-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: 9833a2e66eb6471efb9aed021af7ae07e8e520c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757567"
---
# <span data-ttu-id="34fb0-101">Remove-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="34fb0-101">Remove-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="34fb0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="34fb0-102">SYNOPSIS</span></span>
<span data-ttu-id="34fb0-103">Tar bort en tryck konfiguration från angivet nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="34fb0-103">Removes a tap configuration from given network interface</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34fb0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="34fb0-104">SYNTAX</span></span>

### <span data-ttu-id="34fb0-105">RemoveByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="34fb0-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzureRmNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34fb0-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="34fb0-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzureRmNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34fb0-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34fb0-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzureRmNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34fb0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="34fb0-108">DESCRIPTION</span></span>
<span data-ttu-id="34fb0-109">Cmdleten **Remove-AzureRmNetworkInterfaceTapConfig** tar bort en Azure knackning-konfiguration från en lista med nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="34fb0-109">The **Remove-AzureRmNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="34fb0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="34fb0-110">EXAMPLES</span></span>

### <span data-ttu-id="34fb0-111">Exempel 1: ta bort en tryck konfiguration</span><span class="sxs-lookup"><span data-stu-id="34fb0-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzureRmNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="34fb0-112">Det här kommandot tar bort TapConfiguration från NetworkInterface1 i en resurs grupp ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="34fb0-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="34fb0-113">Eftersom *Force* -parametern inte används uppmanas användaren att bekräfta åtgärden.</span><span class="sxs-lookup"><span data-stu-id="34fb0-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="34fb0-114">Exempel 2: ta bort ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="34fb0-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzureRmNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="34fb0-115">Det här kommandot tar bort TapConfiguration från NetworkInterface1 i en resurs grupp ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="34fb0-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="34fb0-116">Eftersom *Force* -parametern används uppmanas användaren inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="34fb0-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="34fb0-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="34fb0-117">PARAMETERS</span></span>

### <span data-ttu-id="34fb0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34fb0-118">-DefaultProfile</span></span>
<span data-ttu-id="34fb0-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="34fb0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34fb0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="34fb0-120">-Force</span></span>
<span data-ttu-id="34fb0-121">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="34fb0-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="34fb0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34fb0-122">-InputObject</span></span>
<span data-ttu-id="34fb0-123">Referens till NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="34fb0-123">Reference to NetworkInterfaceTapConfig.</span></span>

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

### <span data-ttu-id="34fb0-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="34fb0-124">-Name</span></span>
<span data-ttu-id="34fb0-125">Namn på peering med virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="34fb0-125">The virtual network peering name.</span></span>

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

### <span data-ttu-id="34fb0-126">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="34fb0-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="34fb0-127">Det virtuella nätverks namnet.</span><span class="sxs-lookup"><span data-stu-id="34fb0-127">The virtual network name.</span></span>

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

### <span data-ttu-id="34fb0-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34fb0-128">-PassThru</span></span>
<span data-ttu-id="34fb0-129">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="34fb0-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="34fb0-130">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="34fb0-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="34fb0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34fb0-131">-ResourceGroupName</span></span>
<span data-ttu-id="34fb0-132">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="34fb0-132">The resource group name.</span></span>

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

### <span data-ttu-id="34fb0-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34fb0-133">-ResourceId</span></span>
<span data-ttu-id="34fb0-134">NetworkInterfaceTapConfig resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="34fb0-134">NetworkInterfaceTapConfig resource id.</span></span>

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

### <span data-ttu-id="34fb0-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="34fb0-135">-Confirm</span></span>
<span data-ttu-id="34fb0-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="34fb0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34fb0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34fb0-137">-WhatIf</span></span>
<span data-ttu-id="34fb0-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="34fb0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34fb0-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="34fb0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34fb0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34fb0-140">CommonParameters</span></span>
<span data-ttu-id="34fb0-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34fb0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34fb0-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34fb0-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34fb0-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="34fb0-143">INPUTS</span></span>

### <span data-ttu-id="34fb0-144">System. String</span><span class="sxs-lookup"><span data-stu-id="34fb0-144">System.String</span></span>

## <span data-ttu-id="34fb0-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="34fb0-145">OUTPUTS</span></span>

### <span data-ttu-id="34fb0-146">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="34fb0-146">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="34fb0-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="34fb0-147">NOTES</span></span>

## <span data-ttu-id="34fb0-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="34fb0-148">RELATED LINKS</span></span>
