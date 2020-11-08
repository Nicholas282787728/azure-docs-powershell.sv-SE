---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A34A2B01-A658-410E-8B68-98A6427DFC33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 345d9048ea729b6fe954d2da5e01310be42c79ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099643"
---
# <span data-ttu-id="be8bf-101">Set-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="be8bf-101">Set-AzureVNetGatewayDefaultSite</span></span>

## <span data-ttu-id="be8bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="be8bf-102">SYNOPSIS</span></span>
<span data-ttu-id="be8bf-103">Anger standard webbplatsen för tvingande tunnel trafik.</span><span class="sxs-lookup"><span data-stu-id="be8bf-103">Sets the default site for forced tunneling traffic.</span></span>

## <span data-ttu-id="be8bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="be8bf-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayDefaultSite -VNetName <String> -DefaultSite <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="be8bf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="be8bf-105">DESCRIPTION</span></span>
<span data-ttu-id="be8bf-106">Cmdleten **set-AzureVNetGatewayDefaultSite** anger standard vägen till den lokala webbplatsen för tvingande tunnel trafik.</span><span class="sxs-lookup"><span data-stu-id="be8bf-106">The **Set-AzureVNetGatewayDefaultSite** cmdlet sets the default route to the on-premises site for forced tunneling traffic.</span></span>
<span data-ttu-id="be8bf-107">Det här kommandot ställer in vägen på en Azure Virtual Private Network (VPN) Gateway för ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="be8bf-107">This command sets the route on an Azure virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="be8bf-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="be8bf-108">EXAMPLES</span></span>

## <span data-ttu-id="be8bf-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="be8bf-109">PARAMETERS</span></span>

### <span data-ttu-id="be8bf-110">-DefaultSite</span><span class="sxs-lookup"><span data-stu-id="be8bf-110">-DefaultSite</span></span>
<span data-ttu-id="be8bf-111">Anger namnet på den lokala nätverks platsen för tvingande tunnel trafik.</span><span class="sxs-lookup"><span data-stu-id="be8bf-111">Specifies the name of the on-premises local network site for forced tunneling traffic.</span></span>

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

### <span data-ttu-id="be8bf-112">-Profil</span><span class="sxs-lookup"><span data-stu-id="be8bf-112">-Profile</span></span>
<span data-ttu-id="be8bf-113">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="be8bf-113">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="be8bf-114">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="be8bf-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="be8bf-115">-VNetName</span><span class="sxs-lookup"><span data-stu-id="be8bf-115">-VNetName</span></span>
<span data-ttu-id="be8bf-116">Anger ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="be8bf-116">Specifies a virtual network.</span></span>
<span data-ttu-id="be8bf-117">Denna cmdlet anger standard vägen för VPN-gateway för tvingande tunnel trafik för det virtuella nätverk som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="be8bf-117">This cmdlet sets the default route of the VPN gateway for forced tunneling traffic for the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="be8bf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be8bf-118">CommonParameters</span></span>
<span data-ttu-id="be8bf-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be8bf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be8bf-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be8bf-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be8bf-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="be8bf-121">INPUTS</span></span>

## <span data-ttu-id="be8bf-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="be8bf-122">OUTPUTS</span></span>

## <span data-ttu-id="be8bf-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="be8bf-123">NOTES</span></span>

## <span data-ttu-id="be8bf-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="be8bf-124">RELATED LINKS</span></span>

[<span data-ttu-id="be8bf-125">Remove-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="be8bf-125">Remove-AzureVNetGatewayDefaultSite</span></span>](./Remove-AzureVNetGatewayDefaultSite.md)
