---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: f5ea9c291d23c6378170946ee6b605ec02742ed8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405419"
---
# <span data-ttu-id="0f48e-101">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0f48e-101">Remove-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="0f48e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0f48e-102">SYNOPSIS</span></span>
<span data-ttu-id="0f48e-103">Tar bort en anslutning till en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="0f48e-103">Deletes a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="0f48e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0f48e-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f48e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0f48e-105">DESCRIPTION</span></span>
<span data-ttu-id="0f48e-106">Anslutningen för virtuell nätverksgateway är det objekt som representerar IPsec-tunneln (plats-till-plats eller VNet som är ansluten till din virtuella nätverksgateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="0f48e-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="0f48e-107">Cmdleten **Remove-AzVirtualNetworkGatewayConnection** tar bort objektet i din anslutning baserat på namn-och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="0f48e-107">The **Remove-AzVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="0f48e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0f48e-108">EXAMPLES</span></span>

### <span data-ttu-id="0f48e-109">Exempel 1: ta bort en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="0f48e-109">Example 1: Delete a Virtual Network Gateway Connection</span></span>
```powershell
Remove-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="0f48e-110">Tar bort objektet för den virtuella Nätverksgatewayen med namnet "tunnel" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="0f48e-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="0f48e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0f48e-111">PARAMETERS</span></span>

### <span data-ttu-id="0f48e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f48e-112">-DefaultProfile</span></span>
<span data-ttu-id="0f48e-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0f48e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f48e-114">-Force</span><span class="sxs-lookup"><span data-stu-id="0f48e-114">-Force</span></span>
<span data-ttu-id="0f48e-115">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="0f48e-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0f48e-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="0f48e-116">-Name</span></span>
<span data-ttu-id="0f48e-117">Anger namnet på den virtuella Nätverksgatewayen som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="0f48e-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f48e-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f48e-118">-PassThru</span></span>
<span data-ttu-id="0f48e-119">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="0f48e-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0f48e-120">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="0f48e-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0f48e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f48e-121">-ResourceGroupName</span></span>
<span data-ttu-id="0f48e-122">Anger namnet på den resurs grupp som innehåller anslutningen för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="0f48e-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f48e-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0f48e-123">-Confirm</span></span>
<span data-ttu-id="0f48e-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0f48e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f48e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f48e-125">-WhatIf</span></span>
<span data-ttu-id="0f48e-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0f48e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f48e-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0f48e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f48e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f48e-128">CommonParameters</span></span>
<span data-ttu-id="0f48e-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f48e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f48e-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f48e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f48e-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0f48e-131">INPUTS</span></span>

### <span data-ttu-id="0f48e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0f48e-132">System.String</span></span>

## <span data-ttu-id="0f48e-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0f48e-133">OUTPUTS</span></span>

### <span data-ttu-id="0f48e-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0f48e-134">System.Boolean</span></span>

## <span data-ttu-id="0f48e-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0f48e-135">NOTES</span></span>

## <span data-ttu-id="0f48e-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0f48e-136">RELATED LINKS</span></span>

[<span data-ttu-id="0f48e-137">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0f48e-137">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="0f48e-138">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0f48e-138">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="0f48e-139">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0f48e-139">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
