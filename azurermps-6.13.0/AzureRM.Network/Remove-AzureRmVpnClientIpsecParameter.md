---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: b88fff9775665f5b20f403d46f11bba89dc61220
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576161"
---
# <span data-ttu-id="5f330-101">Remove-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="5f330-101">Remove-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="5f330-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f330-102">SYNOPSIS</span></span>
<span data-ttu-id="5f330-103">Tar bort anpassade IPSec-principinställningar för en virtuell nätverksgateway-resurs.</span><span class="sxs-lookup"><span data-stu-id="5f330-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f330-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f330-104">SYNTAX</span></span>

### <span data-ttu-id="5f330-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="5f330-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f330-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5f330-106">ByFactoryObject</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f330-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5f330-107">ByResourceId</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f330-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f330-108">DESCRIPTION</span></span>
<span data-ttu-id="5f330-109">Den virtuella Nätverksgatewayen är det objekt som representerar din gateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="5f330-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="5f330-110">Cmdleten **Remove-AzureRmVpnClientIpsecParameter** tar bort VPN-parametrarna som anges på din virtuella nätverksgateway, vilka i sin tur ställer in standard princip för VPN-IPSec på VPN gateway baserat på VirtualNetworkGateway namn och resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="5f330-110">The **Remove-AzureRmVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="5f330-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f330-111">EXAMPLES</span></span>

### <span data-ttu-id="5f330-112">1: tar bort den inställda VPN-parametrarna för IPSec på den virtuella Nätverksgatewayen</span><span class="sxs-lookup"><span data-stu-id="5f330-112">1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```
PS C:\> $delete = Remove-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="5f330-113">Tar bort anpassade IPsec-parametrar för VPN i din virtuella nätverksgateway med namnet "Gateway" i resurs gruppen "myRG".</span><span class="sxs-lookup"><span data-stu-id="5f330-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="5f330-114">Det här kommandot returnerar bool-objekt som visar om borttagningen lyckades eller misslyckades.</span><span class="sxs-lookup"><span data-stu-id="5f330-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="5f330-115">Obs! det här kommer att resultera i att en standard-IPSec-princip anges på din virtuella nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="5f330-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="5f330-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f330-116">PARAMETERS</span></span>

### <span data-ttu-id="5f330-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f330-117">-DefaultProfile</span></span>
<span data-ttu-id="5f330-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5f330-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f330-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f330-119">-InputObject</span></span>
<span data-ttu-id="5f330-120">Objektet Gateaway virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="5f330-120">The virtual network gateaway object</span></span>

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

### <span data-ttu-id="5f330-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f330-121">-ResourceGroupName</span></span>
<span data-ttu-id="5f330-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="5f330-122">The resource group name.</span></span>

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

### <span data-ttu-id="5f330-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f330-123">-ResourceId</span></span>
<span data-ttu-id="5f330-124">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="5f330-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5f330-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="5f330-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="5f330-126">Namnet på den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="5f330-126">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="5f330-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5f330-127">-Confirm</span></span>
<span data-ttu-id="5f330-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5f330-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f330-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f330-129">-WhatIf</span></span>
<span data-ttu-id="5f330-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5f330-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f330-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5f330-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f330-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f330-132">CommonParameters</span></span>
<span data-ttu-id="5f330-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f330-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f330-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f330-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f330-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f330-135">INPUTS</span></span>

### <span data-ttu-id="5f330-136">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5f330-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="5f330-137">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5f330-137">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="5f330-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5f330-138">System.String</span></span>

## <span data-ttu-id="5f330-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f330-139">OUTPUTS</span></span>

### <span data-ttu-id="5f330-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5f330-140">System.Boolean</span></span>

## <span data-ttu-id="5f330-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f330-141">NOTES</span></span>

## <span data-ttu-id="5f330-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f330-142">RELATED LINKS</span></span>
