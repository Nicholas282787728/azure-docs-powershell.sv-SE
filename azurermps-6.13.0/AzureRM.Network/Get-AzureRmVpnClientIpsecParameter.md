---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 539ae515d664aaeb01ca824603cd8ee3ed38f0fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576227"
---
# <span data-ttu-id="76879-101">Get-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="76879-101">Get-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="76879-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="76879-102">SYNOPSIS</span></span>
<span data-ttu-id="76879-103">Hämtar IPsec-parametrar för VPN i virtuell nätverksgateway för pekar på webbplats anslutningar.</span><span class="sxs-lookup"><span data-stu-id="76879-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76879-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="76879-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76879-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="76879-105">DESCRIPTION</span></span>
<span data-ttu-id="76879-106">Den virtuella Nätverksgatewayen är det objekt som representerar din gateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="76879-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="76879-107">Cmdleten **Get-AzureRmVpnClientIpsecParameter** returnerar objektet för dina VPN IPsec-parametrar inställda på gateway i Azure baserat på Gateway-namn och resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="76879-107">The **Get-AzureRmVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="76879-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="76879-108">EXAMPLES</span></span>

### <span data-ttu-id="76879-109">1: hämtar IPSec-parametrarna för VPN i virtuell nätverksgateway för pekar på webbplats anslutningar.</span><span class="sxs-lookup"><span data-stu-id="76879-109">1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```
PS C:\> $VpnClientIPsecParameters = Get-AzureRmVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="76879-110">Returnerar objektet för IPSec-parametrarna som anges på den virtuella Nätverksgatewayen med namnet "Gateway" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="76879-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="76879-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="76879-111">PARAMETERS</span></span>

### <span data-ttu-id="76879-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76879-112">-DefaultProfile</span></span>
<span data-ttu-id="76879-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="76879-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76879-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="76879-114">-Name</span></span>
<span data-ttu-id="76879-115">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="76879-115">The resource name.</span></span>

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

### <span data-ttu-id="76879-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76879-116">-ResourceGroupName</span></span>
<span data-ttu-id="76879-117">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="76879-117">The resource group name.</span></span>

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

### <span data-ttu-id="76879-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76879-118">CommonParameters</span></span>
<span data-ttu-id="76879-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76879-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76879-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76879-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76879-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="76879-121">INPUTS</span></span>

### <span data-ttu-id="76879-122">System. String</span><span class="sxs-lookup"><span data-stu-id="76879-122">System.String</span></span>

## <span data-ttu-id="76879-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="76879-123">OUTPUTS</span></span>

### <span data-ttu-id="76879-124">Microsoft. Azure. commands. Networks. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="76879-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="76879-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="76879-125">NOTES</span></span>

## <span data-ttu-id="76879-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="76879-126">RELATED LINKS</span></span>
