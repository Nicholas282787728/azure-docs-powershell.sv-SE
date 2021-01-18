---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: 7708202630b5c7797d9ec3eda77475c82e1c358a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527599"
---
# <span data-ttu-id="7b3cc-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7b3cc-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="7b3cc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7b3cc-102">SYNOPSIS</span></span>
<span data-ttu-id="7b3cc-103">Tar bort en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="7b3cc-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="7b3cc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7b3cc-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b3cc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7b3cc-105">DESCRIPTION</span></span>
<span data-ttu-id="7b3cc-106">Den virtuella Nätverksgatewayen är det objekt som representerar din gateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="7b3cc-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="7b3cc-107">Cmdleten **Get-AzVirtualNetworkGateway** returnerar gatewayens objekt i Azure baserat på namn-och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="7b3cc-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="7b3cc-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7b3cc-108">EXAMPLES</span></span>

### <span data-ttu-id="7b3cc-109">Exempel 1: ta bort en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="7b3cc-109">Example 1: Delete a Virtual Network Gateway</span></span>
```powershell
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="7b3cc-110">Tar bort objektet för den virtuella Nätverksgatewayen med namnet "Gateway" i resurs gruppen "myRG" Obs! Du måste först ta bort alla anslutningar till den virtuella Nätverksgatewayen med cmdlet **Remove-AzVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="7b3cc-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="7b3cc-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7b3cc-111">PARAMETERS</span></span>

### <span data-ttu-id="7b3cc-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b3cc-112">-AsJob</span></span>
<span data-ttu-id="7b3cc-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7b3cc-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b3cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b3cc-114">-DefaultProfile</span></span>
<span data-ttu-id="7b3cc-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7b3cc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b3cc-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7b3cc-116">-Force</span></span>
<span data-ttu-id="7b3cc-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="7b3cc-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7b3cc-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="7b3cc-118">-Name</span></span>
<span data-ttu-id="7b3cc-119">Anger namnet på den virtuella nätverksgateway som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="7b3cc-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7b3cc-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b3cc-120">-PassThru</span></span>
<span data-ttu-id="7b3cc-121">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="7b3cc-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7b3cc-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="7b3cc-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7b3cc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b3cc-123">-ResourceGroupName</span></span>
<span data-ttu-id="7b3cc-124">Anger namnet på den resurs grupp som innehåller den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="7b3cc-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="7b3cc-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7b3cc-125">-Confirm</span></span>
<span data-ttu-id="7b3cc-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7b3cc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b3cc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b3cc-127">-WhatIf</span></span>
<span data-ttu-id="7b3cc-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7b3cc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b3cc-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7b3cc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b3cc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b3cc-130">CommonParameters</span></span>
<span data-ttu-id="7b3cc-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b3cc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b3cc-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b3cc-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b3cc-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7b3cc-133">INPUTS</span></span>

### <span data-ttu-id="7b3cc-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7b3cc-134">System.String</span></span>

## <span data-ttu-id="7b3cc-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7b3cc-135">OUTPUTS</span></span>

### <span data-ttu-id="7b3cc-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7b3cc-136">System.Boolean</span></span>

## <span data-ttu-id="7b3cc-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7b3cc-137">NOTES</span></span>

## <span data-ttu-id="7b3cc-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7b3cc-138">RELATED LINKS</span></span>

[<span data-ttu-id="7b3cc-139">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7b3cc-139">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="7b3cc-140">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7b3cc-140">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="7b3cc-141">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7b3cc-141">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="7b3cc-142">Ändra storlek – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7b3cc-142">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="7b3cc-143">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7b3cc-143">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
