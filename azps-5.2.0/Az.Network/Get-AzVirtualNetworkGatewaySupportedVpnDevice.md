---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: f643b280e0777f3251380ecf36f4fcc070b545c1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418048"
---
# <span data-ttu-id="ad184-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="ad184-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="ad184-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad184-102">SYNOPSIS</span></span>
<span data-ttu-id="ad184-103">Den här cmdleten returnerar en lista med kompatibla VPN-enheter, modeller och inbyggd program vara.</span><span class="sxs-lookup"><span data-stu-id="ad184-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="ad184-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad184-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad184-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad184-105">DESCRIPTION</span></span>
<span data-ttu-id="ad184-106">Den här cmdleten returnerar en lista med kompatibla VPN-enheter, modeller och inbyggd program vara.</span><span class="sxs-lookup"><span data-stu-id="ad184-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="ad184-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad184-107">EXAMPLES</span></span>

### <span data-ttu-id="ad184-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ad184-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway 
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>
```

<span data-ttu-id="ad184-109">Returnerar en lista med de VPN-enheter som stöds, modeller och inbyggd program vara:</span><span class="sxs-lookup"><span data-stu-id="ad184-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="ad184-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad184-110">PARAMETERS</span></span>

### <span data-ttu-id="ad184-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad184-111">-DefaultProfile</span></span>
<span data-ttu-id="ad184-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ad184-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad184-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="ad184-113">-Name</span></span>
<span data-ttu-id="ad184-114">Namnet på den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ad184-114">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad184-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad184-115">-ResourceGroupName</span></span>
<span data-ttu-id="ad184-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ad184-116">The resource group name.</span></span>

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

### <span data-ttu-id="ad184-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad184-117">CommonParameters</span></span>
<span data-ttu-id="ad184-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad184-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad184-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad184-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad184-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad184-120">INPUTS</span></span>

### <span data-ttu-id="ad184-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ad184-121">System.String</span></span>

## <span data-ttu-id="ad184-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad184-122">OUTPUTS</span></span>

### <span data-ttu-id="ad184-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ad184-123">System.String</span></span>

## <span data-ttu-id="ad184-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad184-124">NOTES</span></span>

## <span data-ttu-id="ad184-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad184-125">RELATED LINKS</span></span>
