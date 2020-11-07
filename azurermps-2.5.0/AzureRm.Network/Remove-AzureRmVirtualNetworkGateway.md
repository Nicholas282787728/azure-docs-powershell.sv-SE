---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 958ddffb02aaa6c8ac81f413cca6453f7f87c3a9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930533"
---
# <span data-ttu-id="e2551-101">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e2551-101">Remove-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="e2551-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2551-102">SYNOPSIS</span></span>
<span data-ttu-id="e2551-103">Tar bort en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="e2551-103">Deletes a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2551-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2551-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2551-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2551-105">DESCRIPTION</span></span>
<span data-ttu-id="e2551-106">Den virtuella Nätverksgatewayen är det objekt som representerar din gateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="e2551-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="e2551-107">Cmdleten **Get-AzureRmVirtualNetworkGateway** returnerar gatewayens objekt i Azure baserat på namn-och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="e2551-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="e2551-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2551-108">EXAMPLES</span></span>

### <span data-ttu-id="e2551-109">1: ta bort en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="e2551-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="e2551-110">Tar bort objektet för den virtuella Nätverksgatewayen med namnet "Gateway" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="e2551-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

<span data-ttu-id="e2551-111">Obs! Du måste först ta bort alla anslutningar till den virtuella Nätverksgatewayen med cmdlet **Remove-AzureRmVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="e2551-111">Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="e2551-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2551-112">PARAMETERS</span></span>

### <span data-ttu-id="e2551-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2551-113">-AsJob</span></span>
<span data-ttu-id="e2551-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e2551-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2551-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2551-115">-DefaultProfile</span></span>
<span data-ttu-id="e2551-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e2551-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2551-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e2551-117">-Force</span></span>
<span data-ttu-id="e2551-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e2551-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e2551-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="e2551-119">-Name</span></span>
<span data-ttu-id="e2551-120">Anger namnet på den virtuella nätverksgateway som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="e2551-120">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e2551-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2551-121">-PassThru</span></span>
<span data-ttu-id="e2551-122">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="e2551-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e2551-123">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="e2551-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e2551-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2551-124">-ResourceGroupName</span></span>
<span data-ttu-id="e2551-125">Anger namnet på den resurs grupp som innehåller den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="e2551-125">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="e2551-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e2551-126">-Confirm</span></span>
<span data-ttu-id="e2551-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e2551-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2551-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2551-128">-WhatIf</span></span>
<span data-ttu-id="e2551-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e2551-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2551-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e2551-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2551-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2551-131">CommonParameters</span></span>
<span data-ttu-id="e2551-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2551-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2551-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2551-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2551-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2551-134">INPUTS</span></span>

## <span data-ttu-id="e2551-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2551-135">OUTPUTS</span></span>

## <span data-ttu-id="e2551-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2551-136">NOTES</span></span>

## <span data-ttu-id="e2551-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2551-137">RELATED LINKS</span></span>

