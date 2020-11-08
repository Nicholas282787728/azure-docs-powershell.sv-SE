---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1AB168AA-F466-4C7C-9AD7-0BC7AEEBC932
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8daca2a335f063264fb2e6734948cc1353946e8a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099040"
---
# <span data-ttu-id="23fba-101">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="23fba-101">Set-AzureVNetGatewayKey</span></span>

## <span data-ttu-id="23fba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="23fba-102">SYNOPSIS</span></span>
<span data-ttu-id="23fba-103">Ställer in den fördelade nyckeln för anslutningen mellan en Azure VPN-gateway och en lokal nätverks webbplats.</span><span class="sxs-lookup"><span data-stu-id="23fba-103">Sets the pre-shared key for the connection between an Azure VPN gateway and a local network site.</span></span>

## <span data-ttu-id="23fba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="23fba-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="23fba-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="23fba-105">DESCRIPTION</span></span>
<span data-ttu-id="23fba-106">Cmdleten **set-AzureVNetGatewayKey** anger den fördelade nyckeln för anslutningen mellan en virtuell Azure-Gateway (VPN) och en lokal nätverks webbplats.</span><span class="sxs-lookup"><span data-stu-id="23fba-106">The **Set-AzureVNetGatewayKey** cmdlet sets the pre-shared key for the connection between an Azure virtual private network (VPN) gateway and an on-premises local network site.</span></span>
<span data-ttu-id="23fba-107">Nyckeln måste vara lika med nyckeln som har kon figurer ATS på den lokala nätverks platsens Gateway.</span><span class="sxs-lookup"><span data-stu-id="23fba-107">The key must be equal to the key configured on the gateway of the local network site.</span></span>
<span data-ttu-id="23fba-108">Om nycklarna inte matchar kan ingen anslutning upprättas.</span><span class="sxs-lookup"><span data-stu-id="23fba-108">If the keys do not match, a connection cannot establish.</span></span>

## <span data-ttu-id="23fba-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="23fba-109">EXAMPLES</span></span>

## <span data-ttu-id="23fba-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="23fba-110">PARAMETERS</span></span>

### <span data-ttu-id="23fba-111">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="23fba-111">-LocalNetworkSiteName</span></span>
<span data-ttu-id="23fba-112">Anger namnet på den lokala nätverks platsen som ansluter till den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="23fba-112">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="23fba-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="23fba-113">-Profile</span></span>
<span data-ttu-id="23fba-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="23fba-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="23fba-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="23fba-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="23fba-116">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="23fba-116">-SharedKey</span></span>
<span data-ttu-id="23fba-117">Anger den delade nyckeln som ska kopplas till VPN gateway.</span><span class="sxs-lookup"><span data-stu-id="23fba-117">Specifies the shared key to assign to the VPN gateway.</span></span>
<span data-ttu-id="23fba-118">Värdet måste vara en alpha-numerisk sträng som inte är längre än 128 tecken.</span><span class="sxs-lookup"><span data-stu-id="23fba-118">The value must be an alpha-numerical string no longer than 128 characters.</span></span>

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

### <span data-ttu-id="23fba-119">-VNetName</span><span class="sxs-lookup"><span data-stu-id="23fba-119">-VNetName</span></span>
<span data-ttu-id="23fba-120">Anger det virtuella nätverk som den här cmdleten ställer in den delade nycklar för.</span><span class="sxs-lookup"><span data-stu-id="23fba-120">Specifies the virtual network for which this cmdlet sets the shared key for the connection.</span></span>

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

### <span data-ttu-id="23fba-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23fba-121">CommonParameters</span></span>
<span data-ttu-id="23fba-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23fba-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23fba-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23fba-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23fba-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="23fba-124">INPUTS</span></span>

## <span data-ttu-id="23fba-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="23fba-125">OUTPUTS</span></span>

## <span data-ttu-id="23fba-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="23fba-126">NOTES</span></span>

## <span data-ttu-id="23fba-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="23fba-127">RELATED LINKS</span></span>

[<span data-ttu-id="23fba-128">Get-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="23fba-128">Get-AzureVNetGatewayKey</span></span>](./Get-AzureVNetGatewayKey.md)


