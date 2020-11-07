---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
ms.openlocfilehash: 945f1d8d12b4a493ca361c04ae14cd899f91956f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757927"
---
# <span data-ttu-id="2b42a-101">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2b42a-101">Remove-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="2b42a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2b42a-102">SYNOPSIS</span></span>
<span data-ttu-id="2b42a-103">Tar bort ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="2b42a-103">Removes a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b42a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2b42a-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b42a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2b42a-105">DESCRIPTION</span></span>
<span data-ttu-id="2b42a-106">Cmdleten **Remove-AzureRmVirtualNetwork** tar bort ett Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="2b42a-106">The **Remove-AzureRmVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="2b42a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2b42a-107">EXAMPLES</span></span>

### <span data-ttu-id="2b42a-108">1: skapa och ta bort ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="2b42a-108">1: Create and delete a virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="2b42a-109">I det här exemplet skapas ett virtuellt nätverk i en resurs grupp och sedan tas det omedelbart bort.</span><span class="sxs-lookup"><span data-stu-id="2b42a-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="2b42a-110">Om du inte vill att meddelandet ska visas när det virtuella nätverket tas bort använder du flaggan-Force.</span><span class="sxs-lookup"><span data-stu-id="2b42a-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="2b42a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2b42a-111">PARAMETERS</span></span>

### <span data-ttu-id="2b42a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b42a-112">-AsJob</span></span>
<span data-ttu-id="2b42a-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2b42a-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b42a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b42a-114">-DefaultProfile</span></span>
<span data-ttu-id="2b42a-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2b42a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b42a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2b42a-116">-Force</span></span>
<span data-ttu-id="2b42a-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="2b42a-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2b42a-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="2b42a-118">-Name</span></span>
<span data-ttu-id="2b42a-119">Anger namnet på det virtuella nätverk som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="2b42a-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2b42a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b42a-120">-PassThru</span></span>
<span data-ttu-id="2b42a-121">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="2b42a-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2b42a-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="2b42a-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2b42a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b42a-123">-ResourceGroupName</span></span>
<span data-ttu-id="2b42a-124">Anger namnet på den resurs grupp som innehåller det virtuella nätverk som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="2b42a-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2b42a-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2b42a-125">-Confirm</span></span>
<span data-ttu-id="2b42a-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2b42a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b42a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b42a-127">-WhatIf</span></span>
<span data-ttu-id="2b42a-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2b42a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b42a-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2b42a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b42a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b42a-130">CommonParameters</span></span>
<span data-ttu-id="2b42a-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b42a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b42a-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b42a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b42a-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2b42a-133">INPUTS</span></span>

### <span data-ttu-id="2b42a-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="2b42a-134">None</span></span>
<span data-ttu-id="2b42a-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="2b42a-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2b42a-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2b42a-136">OUTPUTS</span></span>

## <span data-ttu-id="2b42a-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2b42a-137">NOTES</span></span>

## <span data-ttu-id="2b42a-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2b42a-138">RELATED LINKS</span></span>

[<span data-ttu-id="2b42a-139">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2b42a-139">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="2b42a-140">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2b42a-140">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="2b42a-141">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2b42a-141">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


