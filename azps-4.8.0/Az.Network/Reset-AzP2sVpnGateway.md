---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
ms.openlocfilehash: 736e9abe12b00420a4d494510f2cd0d737ae3e02
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102089"
---
# <span data-ttu-id="2572d-101">Reset-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2572d-101">Reset-AzP2sVpnGateway</span></span>

## <span data-ttu-id="2572d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2572d-102">SYNOPSIS</span></span>
<span data-ttu-id="2572d-103">Återställer den skalbara P2S VPN-gateway.</span><span class="sxs-lookup"><span data-stu-id="2572d-103">Resets the scalable P2S VPN gateway.</span></span>

## <span data-ttu-id="2572d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2572d-104">SYNTAX</span></span>

```
Reset-AzP2sVpnGateway -P2SVpnGateway <PSP2SVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2572d-105">ByP2SVpnGatewayName (standard)</span><span class="sxs-lookup"><span data-stu-id="2572d-105">ByP2SVpnGatewayName (Default)</span></span>
```
Reset-- -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2572d-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="2572d-106">ByP2SVpnGatewayObject</span></span>
```
Reset-- -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2572d-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="2572d-107">ByP2SVpnGatewayResourceId</span></span>
```
Reset-- -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2572d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2572d-108">DESCRIPTION</span></span>
<span data-ttu-id="2572d-109">Återställer P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2572d-109">Resets the P2SVpnGateway</span></span>

## <span data-ttu-id="2572d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2572d-110">EXAMPLES</span></span>

### <span data-ttu-id="2572d-111">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="2572d-111">Example 1:</span></span>
```
$Gateway = Get-AzVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzP2sVpnGateway -P2SVpnGateway $Gateway
```

## <span data-ttu-id="2572d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2572d-112">PARAMETERS</span></span>

### <span data-ttu-id="2572d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2572d-113">-AsJob</span></span>
<span data-ttu-id="2572d-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2572d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2572d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2572d-115">-DefaultProfile</span></span>
<span data-ttu-id="2572d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2572d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2572d-117">-P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2572d-117">-P2SVpnGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2572d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2572d-118">CommonParameters</span></span>
<span data-ttu-id="2572d-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2572d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2572d-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2572d-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2572d-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2572d-121">INPUTS</span></span>

### <span data-ttu-id="2572d-122">Microsoft. Azure. commands. Networks. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2572d-122">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

### <span data-ttu-id="2572d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2572d-123">System.String</span></span>

## <span data-ttu-id="2572d-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2572d-124">OUTPUTS</span></span>

### <span data-ttu-id="2572d-125">Microsoft. Azure. commands. Networks. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2572d-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="2572d-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2572d-126">NOTES</span></span>

## <span data-ttu-id="2572d-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2572d-127">RELATED LINKS</span></span>

[<span data-ttu-id="2572d-128">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2572d-128">Get-AzP2sVpnGateway</span></span>](./Get-AzP2sVpnGateway.md)

[<span data-ttu-id="2572d-129">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2572d-129">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="2572d-130">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2572d-130">Remove-AzP2sVpnGateway</span></span>](./Remove-AzP2sVpnGateway.md)

[<span data-ttu-id="2572d-131">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2572d-131">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)
