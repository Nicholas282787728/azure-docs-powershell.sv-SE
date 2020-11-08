---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLocalNetworkGateway.md
ms.openlocfilehash: ac93b104a8ccc1afbeb41bcd11910b76f7d4039f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261794"
---
# <span data-ttu-id="1bac6-101">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1bac6-101">Set-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="1bac6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1bac6-102">SYNOPSIS</span></span>
<span data-ttu-id="1bac6-103">Ändrar en lokal nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="1bac6-103">Modifies a local network gateway.</span></span>

## <span data-ttu-id="1bac6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1bac6-104">SYNTAX</span></span>

```
Set-AzLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway> [-AddressPrefix <String[]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bac6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1bac6-105">DESCRIPTION</span></span>
<span data-ttu-id="1bac6-106">Cmdleten **set-AzLocalNetworkGateway** ändrar en lokal nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="1bac6-106">The **Set-AzLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="1bac6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1bac6-107">EXAMPLES</span></span>

### <span data-ttu-id="1bac6-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1bac6-108">Example 1</span></span>
<span data-ttu-id="1bac6-109">Ange konfiguration för en befintlig gateway</span><span class="sxs-lookup"><span data-stu-id="1bac6-109">Set configuration for an existing gateway</span></span>


```
$lgw = Get-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
Set-AzLocalNetworkGateway -LocalNetworkGateway $lgw

Name                     : myLocalGW
ResourceGroupName        : TestRG1
Location                 : westus
Id                       : /subscriptions/81ab786c-56eb-4a4d-bb5f-f60329772466/resourceGroups/TestRG1/providers/Microso
                           ft.Network/localNetworkGateways/myLocalGW
Etag                     : W/"d2de6968-315e-411d-a4b8-a8c335abe61b"
ResourceGuid             : 393acf8b-dbb8-4b08-a9ea-c714570710e1
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : 1.2.3.4
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

## <span data-ttu-id="1bac6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1bac6-110">PARAMETERS</span></span>

### <span data-ttu-id="1bac6-111">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1bac6-111">-AddressPrefix</span></span>
```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bac6-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1bac6-112">-AsJob</span></span>
<span data-ttu-id="1bac6-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1bac6-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bac6-114">-ASN</span><span class="sxs-lookup"><span data-stu-id="1bac6-114">-Asn</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bac6-115">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="1bac6-115">-BgpPeeringAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bac6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bac6-116">-DefaultProfile</span></span>
<span data-ttu-id="1bac6-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1bac6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bac6-118">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1bac6-118">-LocalNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1bac6-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="1bac6-119">-PeerWeight</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bac6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bac6-120">CommonParameters</span></span>
<span data-ttu-id="1bac6-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bac6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bac6-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bac6-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bac6-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1bac6-123">INPUTS</span></span>

### <span data-ttu-id="1bac6-124">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1bac6-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="1bac6-125">System. string []</span><span class="sxs-lookup"><span data-stu-id="1bac6-125">System.String[]</span></span>

### <span data-ttu-id="1bac6-126">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="1bac6-126">System.UInt32</span></span>

### <span data-ttu-id="1bac6-127">System. String</span><span class="sxs-lookup"><span data-stu-id="1bac6-127">System.String</span></span>

### <span data-ttu-id="1bac6-128">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1bac6-128">System.Int32</span></span>

## <span data-ttu-id="1bac6-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1bac6-129">OUTPUTS</span></span>

### <span data-ttu-id="1bac6-130">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1bac6-130">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="1bac6-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1bac6-131">NOTES</span></span>

## <span data-ttu-id="1bac6-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1bac6-132">RELATED LINKS</span></span>

[<span data-ttu-id="1bac6-133">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1bac6-133">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="1bac6-134">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1bac6-134">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="1bac6-135">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1bac6-135">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)
