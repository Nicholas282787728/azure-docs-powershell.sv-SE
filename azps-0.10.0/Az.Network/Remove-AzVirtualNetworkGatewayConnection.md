---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 70d110e9a539661d780c2dbce7fb8166a8f4ba97
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924341"
---
# <span data-ttu-id="b7a34-101">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b7a34-101">Remove-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="b7a34-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b7a34-102">SYNOPSIS</span></span>
<span data-ttu-id="b7a34-103">Tar bort en anslutning till en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="b7a34-103">Deletes a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="b7a34-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b7a34-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7a34-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b7a34-105">DESCRIPTION</span></span>
<span data-ttu-id="b7a34-106">Anslutningen för virtuell nätverksgateway är det objekt som representerar IPsec-tunneln (plats-till-plats eller VNet som är ansluten till din virtuella nätverksgateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="b7a34-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="b7a34-107">Cmdleten **Remove-AzVirtualNetworkGatewayConnection** tar bort objektet i din anslutning baserat på namn-och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="b7a34-107">The **Remove-AzVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="b7a34-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b7a34-108">EXAMPLES</span></span>

### <span data-ttu-id="b7a34-109">1: ta bort en anslutning till en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="b7a34-109">1: Delete a Virtual Network Gateway Connection</span></span>
```
Remove-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="b7a34-110">Tar bort objektet för den virtuella Nätverksgatewayen med namnet "tunnel" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="b7a34-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="b7a34-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b7a34-111">PARAMETERS</span></span>

### <span data-ttu-id="b7a34-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7a34-112">-DefaultProfile</span></span>
<span data-ttu-id="b7a34-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b7a34-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a34-114">-Force</span><span class="sxs-lookup"><span data-stu-id="b7a34-114">-Force</span></span>
<span data-ttu-id="b7a34-115">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b7a34-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b7a34-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="b7a34-116">-Name</span></span>
<span data-ttu-id="b7a34-117">Anger namnet på den virtuella Nätverksgatewayen som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="b7a34-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a34-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7a34-118">-PassThru</span></span>
<span data-ttu-id="b7a34-119">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="b7a34-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b7a34-120">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="b7a34-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b7a34-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7a34-121">-ResourceGroupName</span></span>
<span data-ttu-id="b7a34-122">Anger namnet på den resurs grupp som innehåller anslutningen för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="b7a34-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a34-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b7a34-123">-Confirm</span></span>
<span data-ttu-id="b7a34-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b7a34-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a34-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7a34-125">-WhatIf</span></span>
<span data-ttu-id="b7a34-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b7a34-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7a34-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b7a34-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a34-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7a34-128">CommonParameters</span></span>
<span data-ttu-id="b7a34-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7a34-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7a34-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7a34-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7a34-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b7a34-131">INPUTS</span></span>

## <span data-ttu-id="b7a34-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b7a34-132">OUTPUTS</span></span>

## <span data-ttu-id="b7a34-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b7a34-133">NOTES</span></span>

## <span data-ttu-id="b7a34-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b7a34-134">RELATED LINKS</span></span>

[<span data-ttu-id="b7a34-135">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b7a34-135">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="b7a34-136">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b7a34-136">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="b7a34-137">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b7a34-137">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)


