---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: B4102F33-979B-4649-99F4-96A295EAE43C
online version: ''
schema: 2.0.0
ms.openlocfilehash: ddb0ac79f5164fb5c953dd1cf1efeff8391d30fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093191"
---
# <span data-ttu-id="c70d6-101">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="c70d6-101">Reset-AzureVNetGateway</span></span>

## <span data-ttu-id="c70d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c70d6-102">SYNOPSIS</span></span>
<span data-ttu-id="c70d6-103">Återställer en VPN-gateway för virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="c70d6-103">Resets a virtual network VPN gateway.</span></span>

## <span data-ttu-id="c70d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c70d6-104">SYNTAX</span></span>

```
Reset-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c70d6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c70d6-105">DESCRIPTION</span></span>
<span data-ttu-id="c70d6-106">Cmdleten **Reset-AzureVNetGateway** återställer och startar om en virtuell gateway för virtuella privata nätverk (VPN).</span><span class="sxs-lookup"><span data-stu-id="c70d6-106">The **Reset-AzureVNetGateway** cmdlet resets and restarts a virtual private network (VPN) virtual network gateway.</span></span>

## <span data-ttu-id="c70d6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c70d6-107">EXAMPLES</span></span>

### <span data-ttu-id="c70d6-108">Exempel 1: Återställ en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="c70d6-108">Example 1: Reset a virtual network gateway</span></span>
```
PS C:\> Reset-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="c70d6-109">Det här kommandot återställer den virtuella Nätverksgatewayen från det virtuella nätverket med namnet ContosoVN07.</span><span class="sxs-lookup"><span data-stu-id="c70d6-109">This command resets the virtual network gateway from the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="c70d6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c70d6-110">PARAMETERS</span></span>

### <span data-ttu-id="c70d6-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="c70d6-111">-Profile</span></span>
<span data-ttu-id="c70d6-112">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c70d6-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c70d6-113">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c70d6-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c70d6-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="c70d6-114">-VNetName</span></span>
<span data-ttu-id="c70d6-115">Anger det virtuella nätverk som innehåller den virtuella Nätverksgatewayen som denna cmdlet återställer.</span><span class="sxs-lookup"><span data-stu-id="c70d6-115">Specifies the virtual network that contains the virtual network gateway that this cmdlet resets.</span></span>

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

### <span data-ttu-id="c70d6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c70d6-116">CommonParameters</span></span>
<span data-ttu-id="c70d6-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c70d6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c70d6-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c70d6-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c70d6-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c70d6-119">INPUTS</span></span>

## <span data-ttu-id="c70d6-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c70d6-120">OUTPUTS</span></span>

## <span data-ttu-id="c70d6-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c70d6-121">NOTES</span></span>

## <span data-ttu-id="c70d6-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c70d6-122">RELATED LINKS</span></span>

[<span data-ttu-id="c70d6-123">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="c70d6-123">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="c70d6-124">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="c70d6-124">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="c70d6-125">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="c70d6-125">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="c70d6-126">Ändra storlek – AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="c70d6-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="c70d6-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="c70d6-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


