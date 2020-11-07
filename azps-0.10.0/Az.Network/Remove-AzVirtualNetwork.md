---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetwork.md
ms.openlocfilehash: b65fcbc132923f18c0a70187403e4c4ba2cef52a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924346"
---
# <span data-ttu-id="38d6e-101">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="38d6e-101">Remove-AzVirtualNetwork</span></span>

## <span data-ttu-id="38d6e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="38d6e-102">SYNOPSIS</span></span>
<span data-ttu-id="38d6e-103">Tar bort ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="38d6e-103">Removes a virtual network.</span></span>

## <span data-ttu-id="38d6e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="38d6e-104">SYNTAX</span></span>

```
Remove-AzVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38d6e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="38d6e-105">DESCRIPTION</span></span>
<span data-ttu-id="38d6e-106">Cmdleten **Remove-AzVirtualNetwork** tar bort ett Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="38d6e-106">The **Remove-AzVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="38d6e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="38d6e-107">EXAMPLES</span></span>

### <span data-ttu-id="38d6e-108">1: skapa och ta bort ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="38d6e-108">1: Create and delete a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="38d6e-109">I det här exemplet skapas ett virtuellt nätverk i en resurs grupp och sedan tas det omedelbart bort.</span><span class="sxs-lookup"><span data-stu-id="38d6e-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="38d6e-110">Om du inte vill att meddelandet ska visas när det virtuella nätverket tas bort använder du flaggan-Force.</span><span class="sxs-lookup"><span data-stu-id="38d6e-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="38d6e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="38d6e-111">PARAMETERS</span></span>

### <span data-ttu-id="38d6e-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38d6e-112">-AsJob</span></span>
<span data-ttu-id="38d6e-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="38d6e-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38d6e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d6e-114">-DefaultProfile</span></span>
<span data-ttu-id="38d6e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="38d6e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38d6e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="38d6e-116">-Force</span></span>
<span data-ttu-id="38d6e-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="38d6e-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="38d6e-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="38d6e-118">-Name</span></span>
<span data-ttu-id="38d6e-119">Anger namnet på det virtuella nätverk som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="38d6e-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="38d6e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38d6e-120">-PassThru</span></span>
<span data-ttu-id="38d6e-121">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="38d6e-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="38d6e-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="38d6e-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="38d6e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38d6e-123">-ResourceGroupName</span></span>
<span data-ttu-id="38d6e-124">Anger namnet på den resurs grupp som innehåller det virtuella nätverk som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="38d6e-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="38d6e-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="38d6e-125">-Confirm</span></span>
<span data-ttu-id="38d6e-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="38d6e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38d6e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38d6e-127">-WhatIf</span></span>
<span data-ttu-id="38d6e-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="38d6e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38d6e-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="38d6e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38d6e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d6e-130">CommonParameters</span></span>
<span data-ttu-id="38d6e-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38d6e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d6e-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38d6e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d6e-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="38d6e-133">INPUTS</span></span>

## <span data-ttu-id="38d6e-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="38d6e-134">OUTPUTS</span></span>

## <span data-ttu-id="38d6e-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="38d6e-135">NOTES</span></span>

## <span data-ttu-id="38d6e-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="38d6e-136">RELATED LINKS</span></span>

[<span data-ttu-id="38d6e-137">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="38d6e-137">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="38d6e-138">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="38d6e-138">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="38d6e-139">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="38d6e-139">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


