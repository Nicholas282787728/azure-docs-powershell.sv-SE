---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: B7E2561D-0FE8-4B34-9188-E89AA0B5C9DD
online version: ''
schema: 2.0.0
ms.openlocfilehash: dce79fc891018c3100140581e89639dbc76b543d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099506"
---
# <span data-ttu-id="fdc80-101">Get-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="fdc80-101">Get-AzureVNetGatewayIPsecParameters</span></span>

## <span data-ttu-id="fdc80-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fdc80-102">SYNOPSIS</span></span>
<span data-ttu-id="fdc80-103">Hämtar IPsec-parametrar för anslutningen mellan en virtuell nätverksgateway och en lokal nätverks webbplats.</span><span class="sxs-lookup"><span data-stu-id="fdc80-103">Gets IPsec parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="fdc80-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fdc80-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayIPsecParameters -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fdc80-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fdc80-105">DESCRIPTION</span></span>
<span data-ttu-id="fdc80-106">Cmdleten **Get-AzureVNetGatewayIPsecParameters** hämtar aktuella IPSec-(Internet Protocol Security) och IKE-parametrar (Internet Key Exchange) för anslutningen mellan en virtuell nätverksgateway och en lokal nätverks webbplats.</span><span class="sxs-lookup"><span data-stu-id="fdc80-106">The **Get-AzureVNetGatewayIPsecParameters** cmdlet gets current Internet Protocol security (IPsec) and Internet Key Exchange (IKE) parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="fdc80-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fdc80-107">EXAMPLES</span></span>

## <span data-ttu-id="fdc80-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fdc80-108">PARAMETERS</span></span>

### <span data-ttu-id="fdc80-109">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="fdc80-109">-LocalNetworkSiteName</span></span>
<span data-ttu-id="fdc80-110">Anger namnet på den lokala nätverks platsen som ansluter till den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="fdc80-110">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdc80-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="fdc80-111">-Profile</span></span>
<span data-ttu-id="fdc80-112">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="fdc80-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="fdc80-113">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="fdc80-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdc80-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="fdc80-114">-VNetName</span></span>
<span data-ttu-id="fdc80-115">Anger det virtuella nätverk som denna cmdlet hämtar IPsec-parametrar för anslutningen till.</span><span class="sxs-lookup"><span data-stu-id="fdc80-115">Specifies the virtual network for which this cmdlet gets IPsec parameters for the connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdc80-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdc80-116">CommonParameters</span></span>
<span data-ttu-id="fdc80-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdc80-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdc80-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdc80-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdc80-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fdc80-119">INPUTS</span></span>

## <span data-ttu-id="fdc80-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fdc80-120">OUTPUTS</span></span>

## <span data-ttu-id="fdc80-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fdc80-121">NOTES</span></span>

## <span data-ttu-id="fdc80-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fdc80-122">RELATED LINKS</span></span>

[<span data-ttu-id="fdc80-123">Set-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="fdc80-123">Set-AzureVNetGatewayIPsecParameters</span></span>](./Set-AzureVNetGatewayIPsecParameters.md)


