---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
ms.openlocfilehash: a594e23505b9db1004a086ff4e0c168353c6bc28
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413075"
---
# <span data-ttu-id="75887-101">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="75887-101">Set-AzPrivateLinkService</span></span>

## <span data-ttu-id="75887-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75887-102">SYNOPSIS</span></span>
<span data-ttu-id="75887-103">Uppdaterar en privat länk tjänst.</span><span class="sxs-lookup"><span data-stu-id="75887-103">Updates a private link service.</span></span>

## <span data-ttu-id="75887-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75887-104">SYNTAX</span></span>

```
Set-AzPrivateLinkService -PrivateLinkService <PSPrivateLinkService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75887-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75887-105">DESCRIPTION</span></span>
<span data-ttu-id="75887-106">Cmdleten **set-AzPrivateLinkService** uppdaterar en privat länk tjänst.</span><span class="sxs-lookup"><span data-stu-id="75887-106">The **Set-AzPrivateLinkService** cmdlet updates a private link service.</span></span>

## <span data-ttu-id="75887-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75887-107">EXAMPLES</span></span>

### <span data-ttu-id="75887-108">1: skapar en privat länk tjänst och uppdaterar dess</span><span class="sxs-lookup"><span data-stu-id="75887-108">1: Creates a private link service and update its</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
$privateLinkService = New-AzPrivateLinkService -ServiceName "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig

$newIPConfig = New-AzPrivateLinkServiceIpConfig -Name "New-IP-Config" -Subnet $vnet.subnets[0] 
$privateLinkService.IpConfigurations[0] = $newIPConfig
$privateLinkService | Set-AzPrivateLinkService
```

<span data-ttu-id="75887-109">I det här exemplet skapas en privat länk tjänst som heter mypls.</span><span class="sxs-lookup"><span data-stu-id="75887-109">This example creates a private link service called mypls.</span></span> <span data-ttu-id="75887-110">Sedan ersätter det dess ipConfigurations från ipConfiguratiuon-objektet i minnet.</span><span class="sxs-lookup"><span data-stu-id="75887-110">Then it replace its ipConfigurations from the in-memory ipConfiguratiuon object.</span></span> <span data-ttu-id="75887-111">Set-AzPrivateLinkService-cmdleten används sedan för att skriva den ändrade statusen för den privata länk tjänsten på tjänst sidan.</span><span class="sxs-lookup"><span data-stu-id="75887-111">The Set-AzPrivateLinkService cmdlet is then used to write the modified private link service state on the service side.</span></span> 

## <span data-ttu-id="75887-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75887-112">PARAMETERS</span></span>

### <span data-ttu-id="75887-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75887-113">-AsJob</span></span>
<span data-ttu-id="75887-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="75887-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75887-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75887-115">-DefaultProfile</span></span>
<span data-ttu-id="75887-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75887-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75887-117">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="75887-117">-PrivateLinkService</span></span>
<span data-ttu-id="75887-118">Anger ett objekt för Private Link service som representerar tillståndet som den privata länk tjänsten ska ställas in för.</span><span class="sxs-lookup"><span data-stu-id="75887-118">Specifies a private link service object representing the state to which the private link service should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75887-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75887-119">CommonParameters</span></span>
<span data-ttu-id="75887-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75887-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75887-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75887-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75887-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75887-122">INPUTS</span></span>

### <span data-ttu-id="75887-123">Microsoft. Azure. commands. Networks. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="75887-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="75887-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75887-124">OUTPUTS</span></span>

### <span data-ttu-id="75887-125">Microsoft. Azure. commands. Networks. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="75887-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="75887-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75887-126">NOTES</span></span>

## <span data-ttu-id="75887-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75887-127">RELATED LINKS</span></span>

[<span data-ttu-id="75887-128">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="75887-128">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="75887-129">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="75887-129">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)

[<span data-ttu-id="75887-130">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="75887-130">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)


