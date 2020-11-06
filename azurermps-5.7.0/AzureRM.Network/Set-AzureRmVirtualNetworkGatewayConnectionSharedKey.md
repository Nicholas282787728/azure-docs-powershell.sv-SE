---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 2f6af6dbbe8a7241cb25e1715859a68bec24598c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575606"
---
# <span data-ttu-id="4ea34-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="4ea34-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="4ea34-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ea34-102">SYNOPSIS</span></span>
<span data-ttu-id="4ea34-103">Konfigurerar den delade nyckeln för anslutningen för virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="4ea34-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ea34-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ea34-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ea34-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ea34-105">DESCRIPTION</span></span>
<span data-ttu-id="4ea34-106">Cmdleten **set-AzureRmVirtualNetworkGatewayConnectionSharedKey** konfigurerar den delade nyckeln för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="4ea34-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="4ea34-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ea34-107">EXAMPLES</span></span>

## <span data-ttu-id="4ea34-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ea34-108">PARAMETERS</span></span>

### <span data-ttu-id="4ea34-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea34-109">-DefaultProfile</span></span>
<span data-ttu-id="4ea34-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea34-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ea34-111">-Force</span><span class="sxs-lookup"><span data-stu-id="4ea34-111">-Force</span></span>
<span data-ttu-id="4ea34-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4ea34-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4ea34-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="4ea34-113">-Name</span></span>
<span data-ttu-id="4ea34-114">Anger namnet på den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="4ea34-114">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="4ea34-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ea34-115">-ResourceGroupName</span></span>
<span data-ttu-id="4ea34-116">Anger namnet på den resurs grupp som den virtuella Nätverksgatewayen</span><span class="sxs-lookup"><span data-stu-id="4ea34-116">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="4ea34-117">-Värde</span><span class="sxs-lookup"><span data-stu-id="4ea34-117">-Value</span></span>
<span data-ttu-id="4ea34-118">Anger värdet på den delade tangenten.</span><span class="sxs-lookup"><span data-stu-id="4ea34-118">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="4ea34-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4ea34-119">-Confirm</span></span>
<span data-ttu-id="4ea34-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4ea34-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ea34-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ea34-121">-WhatIf</span></span>
<span data-ttu-id="4ea34-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4ea34-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ea34-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4ea34-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ea34-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea34-124">CommonParameters</span></span>
<span data-ttu-id="4ea34-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ea34-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea34-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ea34-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea34-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ea34-127">INPUTS</span></span>

### <span data-ttu-id="4ea34-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="4ea34-128">None</span></span>
<span data-ttu-id="4ea34-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4ea34-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4ea34-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ea34-130">OUTPUTS</span></span>

### <span data-ttu-id="4ea34-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4ea34-131">System.String</span></span>

## <span data-ttu-id="4ea34-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ea34-132">NOTES</span></span>

## <span data-ttu-id="4ea34-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ea34-133">RELATED LINKS</span></span>

[<span data-ttu-id="4ea34-134">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="4ea34-134">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="4ea34-135">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="4ea34-135">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


