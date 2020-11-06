---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: f66765d69cb6d9d626322446223aa5f94ff94eac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574596"
---
# <span data-ttu-id="c6d8b-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="c6d8b-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="c6d8b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c6d8b-102">SYNOPSIS</span></span>
<span data-ttu-id="c6d8b-103">Den här cmdleten returnerar en lista med kompatibla VPN-enheter, modeller och inbyggd program vara.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6d8b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c6d8b-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6d8b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c6d8b-105">DESCRIPTION</span></span>
<span data-ttu-id="c6d8b-106">Den här cmdleten returnerar en lista med kompatibla VPN-enheter, modeller och inbyggd program vara.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="c6d8b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c6d8b-107">EXAMPLES</span></span>

### <span data-ttu-id="c6d8b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c6d8b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway 
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>
```

<span data-ttu-id="c6d8b-109">Returnerar en lista med de VPN-enheter som stöds, modeller och inbyggd program vara:</span><span class="sxs-lookup"><span data-stu-id="c6d8b-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="c6d8b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c6d8b-110">PARAMETERS</span></span>

### <span data-ttu-id="c6d8b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6d8b-111">-DefaultProfile</span></span>
<span data-ttu-id="c6d8b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6d8b-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="c6d8b-113">-Name</span></span>
<span data-ttu-id="c6d8b-114">Namnet på den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="c6d8b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6d8b-115">-ResourceGroupName</span></span>
<span data-ttu-id="c6d8b-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-116">The resource group name.</span></span>

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

### <span data-ttu-id="c6d8b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6d8b-117">CommonParameters</span></span>
<span data-ttu-id="c6d8b-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6d8b-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6d8b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6d8b-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c6d8b-120">INPUTS</span></span>

### <span data-ttu-id="c6d8b-121">System. String</span><span class="sxs-lookup"><span data-stu-id="c6d8b-121">System.String</span></span>

## <span data-ttu-id="c6d8b-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c6d8b-122">OUTPUTS</span></span>

### <span data-ttu-id="c6d8b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c6d8b-123">System.String</span></span>

## <span data-ttu-id="c6d8b-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c6d8b-124">NOTES</span></span>

## <span data-ttu-id="c6d8b-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c6d8b-125">RELATED LINKS</span></span>

