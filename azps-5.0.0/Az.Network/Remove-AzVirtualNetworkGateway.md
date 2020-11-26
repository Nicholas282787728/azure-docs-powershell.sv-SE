---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: 7708202630b5c7797d9ec3eda77475c82e1c358a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325799"
---
# <span data-ttu-id="d514d-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d514d-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="d514d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d514d-102">SYNOPSIS</span></span>
<span data-ttu-id="d514d-103">Tar bort en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="d514d-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="d514d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d514d-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d514d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d514d-105">DESCRIPTION</span></span>
<span data-ttu-id="d514d-106">Den virtuella Nätverksgatewayen är det objekt som representerar din gateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="d514d-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="d514d-107">Cmdleten **Get-AzVirtualNetworkGateway** returnerar gatewayens objekt i Azure baserat på namn-och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="d514d-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="d514d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d514d-108">EXAMPLES</span></span>

### <span data-ttu-id="d514d-109">Exempel 1: ta bort en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="d514d-109">Example 1: Delete a Virtual Network Gateway</span></span>
```powershell
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="d514d-110">Tar bort objektet för den virtuella Nätverksgatewayen med namnet "Gateway" i resurs gruppen "myRG" Obs! Du måste först ta bort alla anslutningar till den virtuella Nätverksgatewayen med cmdlet **Remove-AzVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="d514d-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="d514d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d514d-111">PARAMETERS</span></span>

### <span data-ttu-id="d514d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d514d-112">-AsJob</span></span>
<span data-ttu-id="d514d-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d514d-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d514d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d514d-114">-DefaultProfile</span></span>
<span data-ttu-id="d514d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d514d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d514d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d514d-116">-Force</span></span>
<span data-ttu-id="d514d-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d514d-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d514d-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="d514d-118">-Name</span></span>
<span data-ttu-id="d514d-119">Anger namnet på den virtuella nätverksgateway som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="d514d-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d514d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d514d-120">-PassThru</span></span>
<span data-ttu-id="d514d-121">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="d514d-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d514d-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="d514d-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d514d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d514d-123">-ResourceGroupName</span></span>
<span data-ttu-id="d514d-124">Anger namnet på den resurs grupp som innehåller den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="d514d-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="d514d-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d514d-125">-Confirm</span></span>
<span data-ttu-id="d514d-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d514d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d514d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d514d-127">-WhatIf</span></span>
<span data-ttu-id="d514d-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d514d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d514d-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d514d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d514d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d514d-130">CommonParameters</span></span>
<span data-ttu-id="d514d-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d514d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d514d-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d514d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d514d-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d514d-133">INPUTS</span></span>

### <span data-ttu-id="d514d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d514d-134">System.String</span></span>

## <span data-ttu-id="d514d-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d514d-135">OUTPUTS</span></span>

### <span data-ttu-id="d514d-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d514d-136">System.Boolean</span></span>

## <span data-ttu-id="d514d-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d514d-137">NOTES</span></span>

## <span data-ttu-id="d514d-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d514d-138">RELATED LINKS</span></span>

[<span data-ttu-id="d514d-139">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d514d-139">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d514d-140">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d514d-140">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d514d-141">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d514d-141">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d514d-142">Ändra storlek – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d514d-142">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d514d-143">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d514d-143">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)