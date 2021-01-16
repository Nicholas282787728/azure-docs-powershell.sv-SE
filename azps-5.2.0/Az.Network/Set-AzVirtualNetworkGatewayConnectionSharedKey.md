---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: a35d659de6019d9d9451289716a7acac7e33a8b7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392288"
---
# <span data-ttu-id="e0d2c-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="e0d2c-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="e0d2c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0d2c-102">SYNOPSIS</span></span>
<span data-ttu-id="e0d2c-103">Konfigurerar den delade nyckeln för anslutningen för virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="e0d2c-103">Configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="e0d2c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0d2c-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0d2c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0d2c-105">DESCRIPTION</span></span>
<span data-ttu-id="e0d2c-106">Cmdleten **set-AzVirtualNetworkGatewayConnectionSharedKey** konfigurerar den delade nyckeln för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="e0d2c-106">The **Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="e0d2c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0d2c-107">EXAMPLES</span></span>

### <span data-ttu-id="e0d2c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e0d2c-108">Example 1</span></span>
```powershell
PS C:\Users\alzam> Set-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName VPNGatewayV3 -Name VNet1toVNet2 -Value abcd1234

Confirm
Are you sure you want to overwrite resource 'VNet1toVNet2'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
abcd1234
```

## <span data-ttu-id="e0d2c-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0d2c-109">PARAMETERS</span></span>

### <span data-ttu-id="e0d2c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0d2c-110">-DefaultProfile</span></span>
<span data-ttu-id="e0d2c-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e0d2c-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0d2c-112">-Force</span><span class="sxs-lookup"><span data-stu-id="e0d2c-112">-Force</span></span>
<span data-ttu-id="e0d2c-113">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e0d2c-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e0d2c-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="e0d2c-114">-Name</span></span>
<span data-ttu-id="e0d2c-115">Anger namnet på den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="e0d2c-115">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="e0d2c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0d2c-116">-ResourceGroupName</span></span>
<span data-ttu-id="e0d2c-117">Anger namnet på den resurs grupp som den virtuella Nätverksgatewayen</span><span class="sxs-lookup"><span data-stu-id="e0d2c-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="e0d2c-118">-Värde</span><span class="sxs-lookup"><span data-stu-id="e0d2c-118">-Value</span></span>
<span data-ttu-id="e0d2c-119">Anger värdet på den delade tangenten.</span><span class="sxs-lookup"><span data-stu-id="e0d2c-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="e0d2c-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e0d2c-120">-Confirm</span></span>
<span data-ttu-id="e0d2c-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e0d2c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0d2c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0d2c-122">-WhatIf</span></span>
<span data-ttu-id="e0d2c-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e0d2c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0d2c-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e0d2c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0d2c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0d2c-125">CommonParameters</span></span>
<span data-ttu-id="e0d2c-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0d2c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0d2c-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0d2c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0d2c-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0d2c-128">INPUTS</span></span>

### <span data-ttu-id="e0d2c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e0d2c-129">System.String</span></span>

## <span data-ttu-id="e0d2c-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0d2c-130">OUTPUTS</span></span>

### <span data-ttu-id="e0d2c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e0d2c-131">System.String</span></span>

## <span data-ttu-id="e0d2c-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0d2c-132">NOTES</span></span>

## <span data-ttu-id="e0d2c-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0d2c-133">RELATED LINKS</span></span>

[<span data-ttu-id="e0d2c-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="e0d2c-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="e0d2c-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="e0d2c-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)
