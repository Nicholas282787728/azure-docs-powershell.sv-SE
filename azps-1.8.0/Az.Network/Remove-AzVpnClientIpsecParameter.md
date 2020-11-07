---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 5457f330409c760b0e249b99ae5b0d77cf67ffce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747818"
---
# <span data-ttu-id="cdce9-101">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="cdce9-101">Remove-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="cdce9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cdce9-102">SYNOPSIS</span></span>
<span data-ttu-id="cdce9-103">Tar bort anpassade IPSec-principinställningar för en virtuell nätverksgateway-resurs.</span><span class="sxs-lookup"><span data-stu-id="cdce9-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

## <span data-ttu-id="cdce9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cdce9-104">SYNTAX</span></span>

### <span data-ttu-id="cdce9-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="cdce9-105">ByFactoryName (Default)</span></span>
```
Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdce9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cdce9-106">ByFactoryObject</span></span>
```
Remove-AzVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdce9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cdce9-107">ByResourceId</span></span>
```
Remove-AzVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdce9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cdce9-108">DESCRIPTION</span></span>
<span data-ttu-id="cdce9-109">Den virtuella Nätverksgatewayen är det objekt som representerar din gateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="cdce9-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="cdce9-110">Cmdleten **Remove-AzVpnClientIpsecParameter** tar bort VPN-parametrarna som anges på din virtuella nätverksgateway, vilka i sin tur ställer in standard princip för VPN-IPSec på VPN gateway baserat på VirtualNetworkGateway namn och resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="cdce9-110">The **Remove-AzVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="cdce9-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cdce9-111">EXAMPLES</span></span>

### <span data-ttu-id="cdce9-112">1: tar bort den inställda VPN-parametrarna för IPSec på den virtuella Nätverksgatewayen</span><span class="sxs-lookup"><span data-stu-id="cdce9-112">1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```
PS C:\> $delete = Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="cdce9-113">Tar bort anpassade IPsec-parametrar för VPN i din virtuella nätverksgateway med namnet "Gateway" i resurs gruppen "myRG".</span><span class="sxs-lookup"><span data-stu-id="cdce9-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="cdce9-114">Det här kommandot returnerar bool-objekt som visar om borttagningen lyckades eller misslyckades.</span><span class="sxs-lookup"><span data-stu-id="cdce9-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="cdce9-115">Obs! det här kommer att resultera i att en standard-IPSec-princip anges på din virtuella nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="cdce9-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="cdce9-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cdce9-116">PARAMETERS</span></span>

### <span data-ttu-id="cdce9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdce9-117">-DefaultProfile</span></span>
<span data-ttu-id="cdce9-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cdce9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdce9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdce9-119">-InputObject</span></span>
<span data-ttu-id="cdce9-120">Objektet Gateaway virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="cdce9-120">The virtual network gateaway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdce9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdce9-121">-ResourceGroupName</span></span>
<span data-ttu-id="cdce9-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="cdce9-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdce9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cdce9-123">-ResourceId</span></span>
<span data-ttu-id="cdce9-124">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="cdce9-124">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdce9-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="cdce9-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="cdce9-126">Namnet på den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="cdce9-126">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdce9-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cdce9-127">-Confirm</span></span>
<span data-ttu-id="cdce9-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cdce9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdce9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdce9-129">-WhatIf</span></span>
<span data-ttu-id="cdce9-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cdce9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdce9-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cdce9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdce9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdce9-132">CommonParameters</span></span>
<span data-ttu-id="cdce9-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdce9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdce9-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdce9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdce9-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cdce9-135">INPUTS</span></span>

### <span data-ttu-id="cdce9-136">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cdce9-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="cdce9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="cdce9-137">System.String</span></span>

## <span data-ttu-id="cdce9-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cdce9-138">OUTPUTS</span></span>

### <span data-ttu-id="cdce9-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cdce9-139">System.Boolean</span></span>

## <span data-ttu-id="cdce9-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cdce9-140">NOTES</span></span>

## <span data-ttu-id="cdce9-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cdce9-141">RELATED LINKS</span></span>

[<span data-ttu-id="cdce9-142">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="cdce9-142">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="cdce9-143">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="cdce9-143">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="cdce9-144">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="cdce9-144">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)