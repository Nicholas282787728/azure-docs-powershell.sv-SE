---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: 8c3741f7e1a3e25dfbc3a3b6f7fb655e5db19fe8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412776"
---
# <span data-ttu-id="55934-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="55934-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="55934-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="55934-102">SYNOPSIS</span></span>
<span data-ttu-id="55934-103">Tar bort en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="55934-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="55934-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="55934-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55934-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="55934-105">DESCRIPTION</span></span>
<span data-ttu-id="55934-106">Den lokala Nätverksgatewayen är det objekt som representerar din privata VPN-enhet.</span><span class="sxs-lookup"><span data-stu-id="55934-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="55934-107">Cmdleten **Remove-AzLocalNetworkGateway** tar bort objektet som representerar din lokala-gateway baserat på namn och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="55934-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="55934-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="55934-108">EXAMPLES</span></span>

### <span data-ttu-id="55934-109">Exempel 1: ta bort en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="55934-109">Example 1: Delete a Local Network Gateway</span></span>
```powershell
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="55934-110">Tar bort objektet för den lokala Nätverksgatewayen med namnet "myLocalGW" i resurs gruppen "myRG" Obs! Du måste först ta bort alla anslutningar till den lokala Nätverksgatewayen med cmdlet **Remove-AzVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="55934-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="55934-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="55934-111">PARAMETERS</span></span>

### <span data-ttu-id="55934-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55934-112">-AsJob</span></span>
<span data-ttu-id="55934-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="55934-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55934-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55934-114">-DefaultProfile</span></span>
<span data-ttu-id="55934-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="55934-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55934-116">-Force</span><span class="sxs-lookup"><span data-stu-id="55934-116">-Force</span></span>
<span data-ttu-id="55934-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="55934-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="55934-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="55934-118">-Name</span></span>
<span data-ttu-id="55934-119">Anger namnet på den lokala nätverksgateway som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="55934-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="55934-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55934-120">-PassThru</span></span>
<span data-ttu-id="55934-121">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="55934-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="55934-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="55934-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="55934-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55934-123">-ResourceGroupName</span></span>
<span data-ttu-id="55934-124">Anger namnet på den resurs grupp som innehåller den lokala Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="55934-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="55934-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="55934-125">-Confirm</span></span>
<span data-ttu-id="55934-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="55934-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55934-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55934-127">-WhatIf</span></span>
<span data-ttu-id="55934-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="55934-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55934-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="55934-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55934-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55934-130">CommonParameters</span></span>
<span data-ttu-id="55934-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55934-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55934-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55934-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55934-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="55934-133">INPUTS</span></span>

### <span data-ttu-id="55934-134">System. String</span><span class="sxs-lookup"><span data-stu-id="55934-134">System.String</span></span>

## <span data-ttu-id="55934-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="55934-135">OUTPUTS</span></span>

### <span data-ttu-id="55934-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="55934-136">System.Boolean</span></span>

## <span data-ttu-id="55934-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="55934-137">NOTES</span></span>

## <span data-ttu-id="55934-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="55934-138">RELATED LINKS</span></span>

[<span data-ttu-id="55934-139">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="55934-139">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="55934-140">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="55934-140">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="55934-141">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="55934-141">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
