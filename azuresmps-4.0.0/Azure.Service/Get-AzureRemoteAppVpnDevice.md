---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DF95285F-97F4-4064-8E27-EE6E93843E55
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0a14865c986bf6439df833a38f87835792a6e3c5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093352"
---
# <span data-ttu-id="e17a0-101">Get-AzureRemoteAppVpnDevice</span><span class="sxs-lookup"><span data-stu-id="e17a0-101">Get-AzureRemoteAppVpnDevice</span></span>

## <span data-ttu-id="e17a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e17a0-102">SYNOPSIS</span></span>
<span data-ttu-id="e17a0-103">Hämtar information om en VPN-enhet.</span><span class="sxs-lookup"><span data-stu-id="e17a0-103">Retrieves information about a VPN device.</span></span>

## <span data-ttu-id="e17a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e17a0-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVpnDevice [-VNetName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e17a0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e17a0-105">DESCRIPTION</span></span>
<span data-ttu-id="e17a0-106">Cmdleten **Get-AzureRemoteAppVpnDevice** hämtar information om en VPN-enhet (virtuellt privat nätverk).</span><span class="sxs-lookup"><span data-stu-id="e17a0-106">The **Get-AzureRemoteAppVpnDevice** cmdlet retrieves information about a virtual private network (VPN) device.</span></span>

## <span data-ttu-id="e17a0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e17a0-107">EXAMPLES</span></span>

### <span data-ttu-id="e17a0-108">Exempel 1: returnera tillgängliga VPN-enheter för ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="e17a0-108">Example 1: Return the available VPN device configurations for a virtual network</span></span>
```
PS C:\> Get-AzureRemoteVpnDevice -VNetName "ContosoVNet"


Name                   Platforms

----                   ---------

Cisco Systems, Inc.    {ASA 5500 Series Adaptive Security Appliances, ASR 1000 Series Aggregation Services Routers, ASR 1000 Series Aggregation Services Routers - Dynamic Routing, ISR Series Integrated Services Routers...} 

Juniper Networks, Inc. {SRX Series Routers, SRX Series Routers - Dynamic Routing, J Series Routers, J Series Routers - Dynamic Routing...} 

Microsoft Corporation  {RRAS}
```

<span data-ttu-id="e17a0-109">Det här kommandot returnerar de tillgängliga VPN-enhetsobjektet för det angivna virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="e17a0-109">This command returns the available VPN device configurations for the specified virtual network.</span></span>

## <span data-ttu-id="e17a0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e17a0-110">PARAMETERS</span></span>

### <span data-ttu-id="e17a0-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="e17a0-111">-Profile</span></span>
<span data-ttu-id="e17a0-112">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e17a0-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e17a0-113">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e17a0-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e17a0-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="e17a0-114">-VNetName</span></span>
<span data-ttu-id="e17a0-115">Anger namnet på det virtuella Azure RemoteApp-nätverket.</span><span class="sxs-lookup"><span data-stu-id="e17a0-115">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e17a0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e17a0-116">CommonParameters</span></span>
<span data-ttu-id="e17a0-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e17a0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e17a0-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e17a0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e17a0-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e17a0-119">INPUTS</span></span>

## <span data-ttu-id="e17a0-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e17a0-120">OUTPUTS</span></span>

### <span data-ttu-id="e17a0-121">System. String</span><span class="sxs-lookup"><span data-stu-id="e17a0-121">System.String</span></span>

## <span data-ttu-id="e17a0-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e17a0-122">NOTES</span></span>

## <span data-ttu-id="e17a0-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e17a0-123">RELATED LINKS</span></span>

[<span data-ttu-id="e17a0-124">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="e17a0-124">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="e17a0-125">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="e17a0-125">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>](./Get-AzureRemoteAppVpnDeviceConfigScript.md)


