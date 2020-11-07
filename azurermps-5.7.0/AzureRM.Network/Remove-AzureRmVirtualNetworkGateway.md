---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 533eb9482c2e872c0b41552a5c59842a07fa0216
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757926"
---
# <span data-ttu-id="4eddd-101">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4eddd-101">Remove-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="4eddd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4eddd-102">SYNOPSIS</span></span>
<span data-ttu-id="4eddd-103">Tar bort en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="4eddd-103">Deletes a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4eddd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4eddd-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eddd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4eddd-105">DESCRIPTION</span></span>
<span data-ttu-id="4eddd-106">Den virtuella Nätverksgatewayen är det objekt som representerar din gateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="4eddd-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="4eddd-107">Cmdleten **Get-AzureRmVirtualNetworkGateway** returnerar gatewayens objekt i Azure baserat på namn-och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="4eddd-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="4eddd-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4eddd-108">EXAMPLES</span></span>

### <span data-ttu-id="4eddd-109">1: ta bort en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="4eddd-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="4eddd-110">Tar bort objektet för den virtuella Nätverksgatewayen med namnet "Gateway" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="4eddd-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

<span data-ttu-id="4eddd-111">Obs! Du måste först ta bort alla anslutningar till den virtuella Nätverksgatewayen med cmdlet **Remove-AzureRmVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="4eddd-111">Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="4eddd-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4eddd-112">PARAMETERS</span></span>

### <span data-ttu-id="4eddd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4eddd-113">-AsJob</span></span>
<span data-ttu-id="4eddd-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4eddd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4eddd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eddd-115">-DefaultProfile</span></span>
<span data-ttu-id="4eddd-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4eddd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4eddd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4eddd-117">-Force</span></span>
<span data-ttu-id="4eddd-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4eddd-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4eddd-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="4eddd-119">-Name</span></span>
<span data-ttu-id="4eddd-120">Anger namnet på den virtuella nätverksgateway som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="4eddd-120">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4eddd-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4eddd-121">-PassThru</span></span>
<span data-ttu-id="4eddd-122">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="4eddd-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4eddd-123">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="4eddd-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4eddd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eddd-124">-ResourceGroupName</span></span>
<span data-ttu-id="4eddd-125">Anger namnet på den resurs grupp som innehåller den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="4eddd-125">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="4eddd-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4eddd-126">-Confirm</span></span>
<span data-ttu-id="4eddd-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4eddd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eddd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eddd-128">-WhatIf</span></span>
<span data-ttu-id="4eddd-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4eddd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eddd-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4eddd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eddd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eddd-131">CommonParameters</span></span>
<span data-ttu-id="4eddd-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eddd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eddd-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eddd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eddd-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4eddd-134">INPUTS</span></span>

### <span data-ttu-id="4eddd-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="4eddd-135">None</span></span>
<span data-ttu-id="4eddd-136">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4eddd-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4eddd-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4eddd-137">OUTPUTS</span></span>

## <span data-ttu-id="4eddd-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4eddd-138">NOTES</span></span>

## <span data-ttu-id="4eddd-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4eddd-139">RELATED LINKS</span></span>

