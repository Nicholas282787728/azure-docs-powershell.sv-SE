---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: decd715f11359a837247239e1659b41e30fdd21a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757557"
---
# <span data-ttu-id="fe159-101">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fe159-101">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="fe159-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe159-102">SYNOPSIS</span></span>
<span data-ttu-id="fe159-103">Tar bort en anslutning till en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="fe159-103">Deletes a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe159-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe159-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe159-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe159-105">DESCRIPTION</span></span>
<span data-ttu-id="fe159-106">Anslutningen för virtuell nätverksgateway är det objekt som representerar IPsec-tunneln (plats-till-plats eller VNet som är ansluten till din virtuella nätverksgateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="fe159-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="fe159-107">Cmdleten **Remove-AzureRmVirtualNetworkGatewayConnection** tar bort objektet i din anslutning baserat på namn-och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="fe159-107">The **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="fe159-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe159-108">EXAMPLES</span></span>

### <span data-ttu-id="fe159-109">1: ta bort en anslutning till en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="fe159-109">1: Delete a Virtual Network Gateway Connection</span></span>
```
Remove-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="fe159-110">Tar bort objektet för den virtuella Nätverksgatewayen med namnet "tunnel" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="fe159-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="fe159-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe159-111">PARAMETERS</span></span>

### <span data-ttu-id="fe159-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe159-112">-DefaultProfile</span></span>
<span data-ttu-id="fe159-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe159-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe159-114">-Force</span><span class="sxs-lookup"><span data-stu-id="fe159-114">-Force</span></span>
<span data-ttu-id="fe159-115">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="fe159-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fe159-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="fe159-116">-Name</span></span>
<span data-ttu-id="fe159-117">Anger namnet på den virtuella Nätverksgatewayen som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="fe159-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fe159-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe159-118">-PassThru</span></span>
<span data-ttu-id="fe159-119">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="fe159-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fe159-120">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="fe159-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fe159-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe159-121">-ResourceGroupName</span></span>
<span data-ttu-id="fe159-122">Anger namnet på den resurs grupp som innehåller anslutningen för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="fe159-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="fe159-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fe159-123">-Confirm</span></span>
<span data-ttu-id="fe159-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fe159-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe159-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe159-125">-WhatIf</span></span>
<span data-ttu-id="fe159-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fe159-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe159-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fe159-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe159-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe159-128">CommonParameters</span></span>
<span data-ttu-id="fe159-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe159-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe159-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe159-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe159-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe159-131">INPUTS</span></span>

### <span data-ttu-id="fe159-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fe159-132">System.String</span></span>

## <span data-ttu-id="fe159-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe159-133">OUTPUTS</span></span>

### <span data-ttu-id="fe159-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fe159-134">System.Boolean</span></span>

## <span data-ttu-id="fe159-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe159-135">NOTES</span></span>

## <span data-ttu-id="fe159-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe159-136">RELATED LINKS</span></span>

[<span data-ttu-id="fe159-137">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fe159-137">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="fe159-138">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fe159-138">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="fe159-139">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fe159-139">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)


