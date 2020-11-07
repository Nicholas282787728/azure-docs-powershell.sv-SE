---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 794f432b06c693d6758603975a98ca6b2f5e3511
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922202"
---
# <span data-ttu-id="2bc56-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="2bc56-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="2bc56-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2bc56-102">SYNOPSIS</span></span>
<span data-ttu-id="2bc56-103">Den här cmdleten returnerar en lista med kompatibla VPN-enheter, modeller och inbyggd program vara.</span><span class="sxs-lookup"><span data-stu-id="2bc56-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="2bc56-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2bc56-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bc56-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2bc56-105">DESCRIPTION</span></span>
<span data-ttu-id="2bc56-106">Den här cmdleten returnerar en lista med kompatibla VPN-enheter, modeller och inbyggd program vara.</span><span class="sxs-lookup"><span data-stu-id="2bc56-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="2bc56-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2bc56-107">EXAMPLES</span></span>

### <span data-ttu-id="2bc56-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2bc56-108">Example 1</span></span>
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

<span data-ttu-id="2bc56-109">Returnerar en lista med de VPN-enheter som stöds, modeller och inbyggd program vara:</span><span class="sxs-lookup"><span data-stu-id="2bc56-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="2bc56-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2bc56-110">PARAMETERS</span></span>

### <span data-ttu-id="2bc56-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bc56-111">-DefaultProfile</span></span>
<span data-ttu-id="2bc56-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2bc56-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bc56-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="2bc56-113">-Name</span></span>
<span data-ttu-id="2bc56-114">Namnet på den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="2bc56-114">The virtual network gateway name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bc56-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bc56-115">-ResourceGroupName</span></span>
<span data-ttu-id="2bc56-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="2bc56-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bc56-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bc56-117">CommonParameters</span></span>
<span data-ttu-id="2bc56-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bc56-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bc56-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bc56-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bc56-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2bc56-120">INPUTS</span></span>

### <span data-ttu-id="2bc56-121">System. String</span><span class="sxs-lookup"><span data-stu-id="2bc56-121">System.String</span></span>

## <span data-ttu-id="2bc56-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2bc56-122">OUTPUTS</span></span>

### <span data-ttu-id="2bc56-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2bc56-123">System.String</span></span>

## <span data-ttu-id="2bc56-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2bc56-124">NOTES</span></span>

## <span data-ttu-id="2bc56-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2bc56-125">RELATED LINKS</span></span>

