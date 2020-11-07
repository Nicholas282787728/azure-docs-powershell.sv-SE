---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 1ff3e4f4a69309d2dfa5655fefac3d1c5a0e933f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927293"
---
# <span data-ttu-id="b2447-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="b2447-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="b2447-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b2447-102">SYNOPSIS</span></span>
<span data-ttu-id="b2447-103">Hämtar IPsec-parametrar för VPN i virtuell nätverksgateway för pekar på webbplats anslutningar.</span><span class="sxs-lookup"><span data-stu-id="b2447-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="b2447-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b2447-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2447-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b2447-105">DESCRIPTION</span></span>
<span data-ttu-id="b2447-106">Den virtuella Nätverksgatewayen är det objekt som representerar din gateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="b2447-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="b2447-107">Cmdleten **Get-AzVpnClientIpsecParameter** returnerar objektet för dina VPN IPsec-parametrar inställda på gateway i Azure baserat på Gateway-namn och resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b2447-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="b2447-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b2447-108">EXAMPLES</span></span>

### <span data-ttu-id="b2447-109">1: hämtar IPSec-parametrarna för VPN i virtuell nätverksgateway för pekar på webbplats anslutningar.</span><span class="sxs-lookup"><span data-stu-id="b2447-109">1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="b2447-110">Returnerar objektet för IPSec-parametrarna som anges på den virtuella Nätverksgatewayen med namnet "Gateway" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="b2447-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="b2447-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b2447-111">PARAMETERS</span></span>

### <span data-ttu-id="b2447-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2447-112">-DefaultProfile</span></span>
<span data-ttu-id="b2447-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b2447-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2447-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="b2447-114">-Name</span></span>
<span data-ttu-id="b2447-115">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="b2447-115">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2447-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2447-116">-ResourceGroupName</span></span>
<span data-ttu-id="b2447-117">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b2447-117">The resource group name.</span></span>

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

### <span data-ttu-id="b2447-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2447-118">CommonParameters</span></span>
<span data-ttu-id="b2447-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2447-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2447-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2447-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2447-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b2447-121">INPUTS</span></span>

### <span data-ttu-id="b2447-122">System. String</span><span class="sxs-lookup"><span data-stu-id="b2447-122">System.String</span></span>

## <span data-ttu-id="b2447-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b2447-123">OUTPUTS</span></span>

### <span data-ttu-id="b2447-124">Microsoft. Azure. commands. Networks. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="b2447-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="b2447-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b2447-125">NOTES</span></span>

## <span data-ttu-id="b2447-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b2447-126">RELATED LINKS</span></span>

[<span data-ttu-id="b2447-127">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="b2447-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="b2447-128">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="b2447-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="b2447-129">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="b2447-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
