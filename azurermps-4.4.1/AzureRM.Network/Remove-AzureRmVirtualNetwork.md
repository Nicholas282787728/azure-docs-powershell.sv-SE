---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
ms.openlocfilehash: 1ab783b4b5a49793b4f4c91f2f7bc9f5410e5ddd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574575"
---
# <span data-ttu-id="54ea7-101">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="54ea7-101">Remove-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="54ea7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54ea7-102">SYNOPSIS</span></span>
<span data-ttu-id="54ea7-103">Tar bort ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="54ea7-103">Removes a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54ea7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54ea7-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54ea7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54ea7-105">DESCRIPTION</span></span>
<span data-ttu-id="54ea7-106">Cmdleten **Remove-AzureRmVirtualNetwork** tar bort ett Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="54ea7-106">The **Remove-AzureRmVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="54ea7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54ea7-107">EXAMPLES</span></span>

### <span data-ttu-id="54ea7-108">1: skapa och ta bort ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="54ea7-108">1: Create and delete a virtual network</span></span>
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

<span data-ttu-id="54ea7-109">I det här exemplet skapas ett virtuellt nätverk i en resurs grupp och sedan tas det omedelbart bort.</span><span class="sxs-lookup"><span data-stu-id="54ea7-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="54ea7-110">Om du inte vill att meddelandet ska visas när det virtuella nätverket tas bort använder du flaggan-Force.</span><span class="sxs-lookup"><span data-stu-id="54ea7-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="54ea7-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54ea7-111">PARAMETERS</span></span>

### <span data-ttu-id="54ea7-112">-Force</span><span class="sxs-lookup"><span data-stu-id="54ea7-112">-Force</span></span>
<span data-ttu-id="54ea7-113">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="54ea7-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="54ea7-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="54ea7-114">-Name</span></span>
<span data-ttu-id="54ea7-115">Anger namnet på det virtuella nätverk som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="54ea7-115">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="54ea7-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54ea7-116">-PassThru</span></span>
<span data-ttu-id="54ea7-117">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="54ea7-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="54ea7-118">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="54ea7-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="54ea7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54ea7-119">-ResourceGroupName</span></span>
<span data-ttu-id="54ea7-120">Anger namnet på den resurs grupp som innehåller det virtuella nätverk som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="54ea7-120">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="54ea7-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="54ea7-121">-Confirm</span></span>
<span data-ttu-id="54ea7-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="54ea7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54ea7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54ea7-123">-WhatIf</span></span>
<span data-ttu-id="54ea7-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="54ea7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54ea7-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="54ea7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54ea7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54ea7-126">-DefaultProfile</span></span>
<span data-ttu-id="54ea7-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="54ea7-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54ea7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54ea7-128">CommonParameters</span></span>
<span data-ttu-id="54ea7-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54ea7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54ea7-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54ea7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54ea7-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54ea7-131">INPUTS</span></span>

## <span data-ttu-id="54ea7-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54ea7-132">OUTPUTS</span></span>

## <span data-ttu-id="54ea7-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54ea7-133">NOTES</span></span>

## <span data-ttu-id="54ea7-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54ea7-134">RELATED LINKS</span></span>

[<span data-ttu-id="54ea7-135">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="54ea7-135">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="54ea7-136">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="54ea7-136">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="54ea7-137">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="54ea7-137">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


