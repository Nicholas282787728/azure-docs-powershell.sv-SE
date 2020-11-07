---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 2683af757bc1b0b58ebb6865a1cfd1edeef580e3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924134"
---
# <span data-ttu-id="b5d7e-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b5d7e-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="b5d7e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5d7e-102">SYNOPSIS</span></span>
<span data-ttu-id="b5d7e-103">Konfigurerar den delade nyckeln för anslutningen för virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-103">Configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="b5d7e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5d7e-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5d7e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5d7e-105">DESCRIPTION</span></span>
<span data-ttu-id="b5d7e-106">Cmdleten **set-AzVirtualNetworkGatewayConnectionSharedKey** konfigurerar den delade nyckeln för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-106">The **Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="b5d7e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5d7e-107">EXAMPLES</span></span>

### <span data-ttu-id="b5d7e-108">9.1</span><span class="sxs-lookup"><span data-stu-id="b5d7e-108">1:</span></span>
```

```

## <span data-ttu-id="b5d7e-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5d7e-109">PARAMETERS</span></span>

### <span data-ttu-id="b5d7e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5d7e-110">-DefaultProfile</span></span>
<span data-ttu-id="b5d7e-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5d7e-112">-Force</span><span class="sxs-lookup"><span data-stu-id="b5d7e-112">-Force</span></span>
<span data-ttu-id="b5d7e-113">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b5d7e-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="b5d7e-114">-Name</span></span>
<span data-ttu-id="b5d7e-115">Anger namnet på den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-115">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="b5d7e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5d7e-116">-ResourceGroupName</span></span>
<span data-ttu-id="b5d7e-117">Anger namnet på den resurs grupp som den virtuella Nätverksgatewayen</span><span class="sxs-lookup"><span data-stu-id="b5d7e-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="b5d7e-118">-Värde</span><span class="sxs-lookup"><span data-stu-id="b5d7e-118">-Value</span></span>
<span data-ttu-id="b5d7e-119">Anger värdet på den delade tangenten.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="b5d7e-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b5d7e-120">-Confirm</span></span>
<span data-ttu-id="b5d7e-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5d7e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5d7e-122">-WhatIf</span></span>
<span data-ttu-id="b5d7e-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5d7e-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5d7e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5d7e-125">CommonParameters</span></span>
<span data-ttu-id="b5d7e-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5d7e-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5d7e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5d7e-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5d7e-128">INPUTS</span></span>

## <span data-ttu-id="b5d7e-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5d7e-129">OUTPUTS</span></span>

### <span data-ttu-id="b5d7e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b5d7e-130">System.String</span></span>

## <span data-ttu-id="b5d7e-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5d7e-131">NOTES</span></span>

## <span data-ttu-id="b5d7e-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5d7e-132">RELATED LINKS</span></span>

[<span data-ttu-id="b5d7e-133">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b5d7e-133">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="b5d7e-134">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b5d7e-134">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)


