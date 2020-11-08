---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8AD101BA-9275-4B2B-BB31-99FC34B8D1E8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1ac1d91bc084c9e1b17debf154b2a44c144ce312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099505"
---
# <span data-ttu-id="32be6-101">Get-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="32be6-101">Get-AzureVNetGatewayKey</span></span>

## <span data-ttu-id="32be6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="32be6-102">SYNOPSIS</span></span>
<span data-ttu-id="32be6-103">Hämtar den fördelade nyckeln för anslutningen mellan en virtuell nätverksgateway och en lokal nätverks webbplats.</span><span class="sxs-lookup"><span data-stu-id="32be6-103">Gets the pre-shared key for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="32be6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="32be6-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="32be6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="32be6-105">DESCRIPTION</span></span>
<span data-ttu-id="32be6-106">Cmdleten **Get-AzureVNetGatewayKey** får den fördelade nyckeln för anslutningen mellan en virtuell nätverksgateway och en lokal nätverks webbplats.</span><span class="sxs-lookup"><span data-stu-id="32be6-106">The **Get-AzureVNetGatewayKey** cmdlet gets the pre-shared key for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="32be6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="32be6-107">EXAMPLES</span></span>

## <span data-ttu-id="32be6-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="32be6-108">PARAMETERS</span></span>

### <span data-ttu-id="32be6-109">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="32be6-109">-LocalNetworkSiteName</span></span>
<span data-ttu-id="32be6-110">Anger namnet på den lokala nätverks platsen som ansluter till den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="32be6-110">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="32be6-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="32be6-111">-Profile</span></span>
<span data-ttu-id="32be6-112">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="32be6-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="32be6-113">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="32be6-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="32be6-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="32be6-114">-VNetName</span></span>
<span data-ttu-id="32be6-115">Anger det virtuella nätverk för vilket den här cmdleten får den delade knappen för anslutningar.</span><span class="sxs-lookup"><span data-stu-id="32be6-115">Specifies the virtual network for which this cmdlet gets the shared key for connections.</span></span>

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

### <span data-ttu-id="32be6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32be6-116">CommonParameters</span></span>
<span data-ttu-id="32be6-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32be6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32be6-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32be6-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32be6-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="32be6-119">INPUTS</span></span>

## <span data-ttu-id="32be6-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="32be6-120">OUTPUTS</span></span>

## <span data-ttu-id="32be6-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="32be6-121">NOTES</span></span>

## <span data-ttu-id="32be6-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="32be6-122">RELATED LINKS</span></span>

[<span data-ttu-id="32be6-123">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="32be6-123">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


