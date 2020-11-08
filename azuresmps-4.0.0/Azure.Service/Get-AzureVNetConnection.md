---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7B749B29-9820-4E23-B5AF-F5535251629A
online version: ''
schema: 2.0.0
ms.openlocfilehash: ec94df29fb23dd7c82d79304c2e48aab225ed224
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099517"
---
# <span data-ttu-id="a6601-101">Get-AzureVNetConnection</span><span class="sxs-lookup"><span data-stu-id="a6601-101">Get-AzureVNetConnection</span></span>

## <span data-ttu-id="a6601-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a6601-102">SYNOPSIS</span></span>
<span data-ttu-id="a6601-103">Ansluter till ett Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="a6601-103">Gets connections to an Azure virtual network.</span></span>

## <span data-ttu-id="a6601-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a6601-104">SYNTAX</span></span>

```
Get-AzureVNetConnection -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a6601-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a6601-105">DESCRIPTION</span></span>
<span data-ttu-id="a6601-106">Cmdleten **Get-AzureVNetConnection** returnerar ett objekt som anger alla aktiva anslutningar för virtuella privata nätverk (VPN) till ett virtuellt Azure-nätverk.</span><span class="sxs-lookup"><span data-stu-id="a6601-106">The **Get-AzureVNetConnection** cmdlet returns an object that specifies all active virtual private network (VPN) connections to an Azure virtual network.</span></span>
<span data-ttu-id="a6601-107">VPN-anslutningar inkluderar lokala VPN-anslutningar (Site-to-Site) och virtuella nätverk till virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="a6601-107">VPN connections include cross premises site-to-site VPNs and virtual network to virtual network connections.</span></span>

## <span data-ttu-id="a6601-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a6601-108">EXAMPLES</span></span>

## <span data-ttu-id="a6601-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a6601-109">PARAMETERS</span></span>

### <span data-ttu-id="a6601-110">-Profil</span><span class="sxs-lookup"><span data-stu-id="a6601-110">-Profile</span></span>
<span data-ttu-id="a6601-111">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="a6601-111">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a6601-112">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="a6601-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a6601-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="a6601-113">-VNetName</span></span>
<span data-ttu-id="a6601-114">Anger namnet på det virtuella nätverk som den här cmdleten returnerar anslutningar från.</span><span class="sxs-lookup"><span data-stu-id="a6601-114">Specifies the name of the virtual network from which this cmdlet returns connections.</span></span>

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

### <span data-ttu-id="a6601-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6601-115">CommonParameters</span></span>
<span data-ttu-id="a6601-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6601-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6601-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6601-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6601-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a6601-118">INPUTS</span></span>

## <span data-ttu-id="a6601-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a6601-119">OUTPUTS</span></span>

## <span data-ttu-id="a6601-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a6601-120">NOTES</span></span>

## <span data-ttu-id="a6601-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a6601-121">RELATED LINKS</span></span>

