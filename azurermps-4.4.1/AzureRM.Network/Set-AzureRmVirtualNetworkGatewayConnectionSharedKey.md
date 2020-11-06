---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 1c51d58d7732a3f9d07f1beba24a7584b35733b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577615"
---
# <span data-ttu-id="6cfa9-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6cfa9-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="6cfa9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6cfa9-102">SYNOPSIS</span></span>
<span data-ttu-id="6cfa9-103">Konfigurerar den delade nyckeln för anslutningen för virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="6cfa9-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cfa9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6cfa9-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cfa9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6cfa9-105">DESCRIPTION</span></span>
<span data-ttu-id="6cfa9-106">Cmdleten **set-AzureRmVirtualNetworkGatewayConnectionSharedKey** konfigurerar den delade nyckeln för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6cfa9-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="6cfa9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6cfa9-107">EXAMPLES</span></span>

## <span data-ttu-id="6cfa9-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6cfa9-108">PARAMETERS</span></span>

### <span data-ttu-id="6cfa9-109">-Force</span><span class="sxs-lookup"><span data-stu-id="6cfa9-109">-Force</span></span>
<span data-ttu-id="6cfa9-110">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6cfa9-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6cfa9-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="6cfa9-111">-Name</span></span>
<span data-ttu-id="6cfa9-112">Anger namnet på den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="6cfa9-112">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="6cfa9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cfa9-113">-ResourceGroupName</span></span>
<span data-ttu-id="6cfa9-114">Anger namnet på den resurs grupp som den virtuella Nätverksgatewayen</span><span class="sxs-lookup"><span data-stu-id="6cfa9-114">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="6cfa9-115">-Värde</span><span class="sxs-lookup"><span data-stu-id="6cfa9-115">-Value</span></span>
<span data-ttu-id="6cfa9-116">Anger värdet på den delade tangenten.</span><span class="sxs-lookup"><span data-stu-id="6cfa9-116">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="6cfa9-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6cfa9-117">-Confirm</span></span>
<span data-ttu-id="6cfa9-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6cfa9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cfa9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cfa9-119">-WhatIf</span></span>
<span data-ttu-id="6cfa9-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6cfa9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cfa9-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6cfa9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cfa9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cfa9-122">-DefaultProfile</span></span>
<span data-ttu-id="6cfa9-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6cfa9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cfa9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cfa9-124">CommonParameters</span></span>
<span data-ttu-id="6cfa9-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cfa9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cfa9-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cfa9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cfa9-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6cfa9-127">INPUTS</span></span>

## <span data-ttu-id="6cfa9-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6cfa9-128">OUTPUTS</span></span>

### <span data-ttu-id="6cfa9-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6cfa9-129">System.String</span></span>

## <span data-ttu-id="6cfa9-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6cfa9-130">NOTES</span></span>

## <span data-ttu-id="6cfa9-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6cfa9-131">RELATED LINKS</span></span>

[<span data-ttu-id="6cfa9-132">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6cfa9-132">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="6cfa9-133">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6cfa9-133">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


