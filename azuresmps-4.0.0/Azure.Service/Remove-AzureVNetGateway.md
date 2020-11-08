---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E6EF9B8-9709-4E59-A1E5-78CDA4EAAE1B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88dcd2f4bad149396d58948d3d656defdf055104
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093216"
---
# <span data-ttu-id="69d5e-101">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="69d5e-101">Remove-AzureVNetGateway</span></span>

## <span data-ttu-id="69d5e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69d5e-102">SYNOPSIS</span></span>
<span data-ttu-id="69d5e-103">Tar bort en VPN-gateway.</span><span class="sxs-lookup"><span data-stu-id="69d5e-103">Deletes a VPN gateway.</span></span>

## <span data-ttu-id="69d5e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69d5e-104">SYNTAX</span></span>

```
Remove-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="69d5e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69d5e-105">DESCRIPTION</span></span>
<span data-ttu-id="69d5e-106">Cmdleten **Remove-AzureVNetGateway** tar bort ett befintligt virtuellt privat nätverk (VPN) för ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="69d5e-106">The **Remove-AzureVNetGateway** cmdlet deletes an existing virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="69d5e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69d5e-107">EXAMPLES</span></span>

### <span data-ttu-id="69d5e-108">Exempel 1: ta bort en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="69d5e-108">Example 1: Remove a virtual network gateway</span></span>
```
PS C:\> Remove-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="69d5e-109">Det här kommandot tar bort den virtuella Nätverksgatewayen från det virtuella nätverket med namnet ContosoVN07.</span><span class="sxs-lookup"><span data-stu-id="69d5e-109">This command removes the virtual network gateway from the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="69d5e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69d5e-110">PARAMETERS</span></span>

### <span data-ttu-id="69d5e-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="69d5e-111">-Profile</span></span>
<span data-ttu-id="69d5e-112">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="69d5e-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="69d5e-113">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="69d5e-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="69d5e-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="69d5e-114">-VNetName</span></span>
<span data-ttu-id="69d5e-115">Anger det virtuella nätverk där denna cmdlet tar bort VPN gatewayen.</span><span class="sxs-lookup"><span data-stu-id="69d5e-115">Specifies the virtual network in which this cmdlet deletes the VPN gateway.</span></span>

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

### <span data-ttu-id="69d5e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69d5e-116">CommonParameters</span></span>
<span data-ttu-id="69d5e-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69d5e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69d5e-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69d5e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69d5e-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69d5e-119">INPUTS</span></span>

## <span data-ttu-id="69d5e-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69d5e-120">OUTPUTS</span></span>

## <span data-ttu-id="69d5e-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69d5e-121">NOTES</span></span>

## <span data-ttu-id="69d5e-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69d5e-122">RELATED LINKS</span></span>

[<span data-ttu-id="69d5e-123">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="69d5e-123">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="69d5e-124">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="69d5e-124">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="69d5e-125">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="69d5e-125">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="69d5e-126">Ändra storlek – AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="69d5e-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="69d5e-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="69d5e-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


