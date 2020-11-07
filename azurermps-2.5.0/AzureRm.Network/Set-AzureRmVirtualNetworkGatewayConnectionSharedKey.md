---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
ms.openlocfilehash: be59f9ec0728b60314f137dcc5a57c7883935e52
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930509"
---
# <span data-ttu-id="cdfb0-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="cdfb0-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="cdfb0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cdfb0-102">SYNOPSIS</span></span>
<span data-ttu-id="cdfb0-103">Konfigurerar den delade nyckeln för anslutningen för virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="cdfb0-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdfb0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cdfb0-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdfb0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cdfb0-105">DESCRIPTION</span></span>
<span data-ttu-id="cdfb0-106">Cmdleten **set-AzureRmVirtualNetworkGatewayConnectionSharedKey** konfigurerar den delade nyckeln för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="cdfb0-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="cdfb0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cdfb0-107">EXAMPLES</span></span>

### <span data-ttu-id="cdfb0-108">9.1</span><span class="sxs-lookup"><span data-stu-id="cdfb0-108">1:</span></span>
```

```

## <span data-ttu-id="cdfb0-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cdfb0-109">PARAMETERS</span></span>

### <span data-ttu-id="cdfb0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdfb0-110">-DefaultProfile</span></span>
<span data-ttu-id="cdfb0-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cdfb0-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdfb0-112">-Force</span><span class="sxs-lookup"><span data-stu-id="cdfb0-112">-Force</span></span>
<span data-ttu-id="cdfb0-113">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="cdfb0-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cdfb0-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="cdfb0-114">-Name</span></span>
<span data-ttu-id="cdfb0-115">Anger namnet på den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="cdfb0-115">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="cdfb0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdfb0-116">-ResourceGroupName</span></span>
<span data-ttu-id="cdfb0-117">Anger namnet på den resurs grupp som den virtuella Nätverksgatewayen</span><span class="sxs-lookup"><span data-stu-id="cdfb0-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="cdfb0-118">-Värde</span><span class="sxs-lookup"><span data-stu-id="cdfb0-118">-Value</span></span>
<span data-ttu-id="cdfb0-119">Anger värdet på den delade tangenten.</span><span class="sxs-lookup"><span data-stu-id="cdfb0-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="cdfb0-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cdfb0-120">-Confirm</span></span>
<span data-ttu-id="cdfb0-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cdfb0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdfb0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdfb0-122">-WhatIf</span></span>
<span data-ttu-id="cdfb0-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cdfb0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdfb0-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cdfb0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdfb0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdfb0-125">CommonParameters</span></span>
<span data-ttu-id="cdfb0-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdfb0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdfb0-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdfb0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdfb0-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cdfb0-128">INPUTS</span></span>

## <span data-ttu-id="cdfb0-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cdfb0-129">OUTPUTS</span></span>

### <span data-ttu-id="cdfb0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cdfb0-130">System.String</span></span>

## <span data-ttu-id="cdfb0-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cdfb0-131">NOTES</span></span>

## <span data-ttu-id="cdfb0-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cdfb0-132">RELATED LINKS</span></span>

[<span data-ttu-id="cdfb0-133">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="cdfb0-133">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="cdfb0-134">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="cdfb0-134">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


