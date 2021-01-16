---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
ms.openlocfilehash: 5a6cbbc007c372d2e1765e4e2369d2f3d60d0a07
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395512"
---
# <span data-ttu-id="0fd9f-101">New-AzIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="0fd9f-101">New-AzIpsecPolicy</span></span>

## <span data-ttu-id="0fd9f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0fd9f-102">SYNOPSIS</span></span>
<span data-ttu-id="0fd9f-103">Skapar en IPSec-princip.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-103">Creates an IPSec Policy.</span></span>

## <span data-ttu-id="0fd9f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0fd9f-104">SYNTAX</span></span>

```
New-AzIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fd9f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0fd9f-105">DESCRIPTION</span></span>
<span data-ttu-id="0fd9f-106">New-AzIpsecPolicy-cmdleten skapar ett abonnemang för IPSec-principer som ska användas i en anslutning till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-106">The New-AzIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="0fd9f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0fd9f-107">EXAMPLES</span></span>

### <span data-ttu-id="0fd9f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0fd9f-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="0fd9f-109">Skapa en IPSec-princip som ska användas för en ny virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="0fd9f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0fd9f-110">PARAMETERS</span></span>

### <span data-ttu-id="0fd9f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fd9f-111">-DefaultProfile</span></span>
<span data-ttu-id="0fd9f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fd9f-113">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="0fd9f-113">-DhGroup</span></span>
<span data-ttu-id="0fd9f-114">DH-grupper som används i IKE fas 1 för inledande SA</span><span class="sxs-lookup"><span data-stu-id="0fd9f-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, DHGroup1, DHGroup14, DHGroup2, DHGroup2048, DHGroup24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fd9f-115">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="0fd9f-115">-IkeEncryption</span></span>
<span data-ttu-id="0fd9f-116">IKE-krypteringsalgoritmen (IKE-fas 1)</span><span class="sxs-lookup"><span data-stu-id="0fd9f-116">The IKE encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DES, DES3, AES128, AES192, AES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fd9f-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="0fd9f-117">-IkeIntegrity</span></span>
<span data-ttu-id="0fd9f-118">IKE-integritetsalgoritmen (IKE-fas 1)</span><span class="sxs-lookup"><span data-stu-id="0fd9f-118">The IKE integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MD5, SHA1, SHA256, SHA384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fd9f-119">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="0fd9f-119">-IpsecEncryption</span></span>
<span data-ttu-id="0fd9f-120">IPSec-krypteringsalgoritmen (IKE fas 2)</span><span class="sxs-lookup"><span data-stu-id="0fd9f-120">The IPSec encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, DES, DES3, AES128, AES192, AES256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fd9f-121">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="0fd9f-121">-IpsecIntegrity</span></span>
<span data-ttu-id="0fd9f-122">IPSec-integritetsalgoritm (IKE-fas 2)</span><span class="sxs-lookup"><span data-stu-id="0fd9f-122">The IPSec integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MD5, SHA1, SHA256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fd9f-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="0fd9f-123">-PfsGroup</span></span>
<span data-ttu-id="0fd9f-124">DH-grupper som används i IKE fas 2 för ny underordnad SA</span><span class="sxs-lookup"><span data-stu-id="0fd9f-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, PFS1, PFS2, PFS2048, PFS24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fd9f-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="0fd9f-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="0fd9f-126">Säkerhets Association för IPSec (kallas även för en nytto Last i KB för snabb-eller fas 2)</span><span class="sxs-lookup"><span data-stu-id="0fd9f-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fd9f-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="0fd9f-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="0fd9f-128">Säkerhets Association för IPSec (kallas även för snabb läge eller fas 2 SA) i sekunder</span><span class="sxs-lookup"><span data-stu-id="0fd9f-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fd9f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fd9f-129">CommonParameters</span></span>
<span data-ttu-id="0fd9f-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fd9f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fd9f-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fd9f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fd9f-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0fd9f-132">INPUTS</span></span>

### <span data-ttu-id="0fd9f-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="0fd9f-133">None</span></span>

## <span data-ttu-id="0fd9f-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0fd9f-134">OUTPUTS</span></span>

### <span data-ttu-id="0fd9f-135">Microsoft. Azure. commands. Networks. Models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="0fd9f-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="0fd9f-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0fd9f-136">NOTES</span></span>

## <span data-ttu-id="0fd9f-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0fd9f-137">RELATED LINKS</span></span>
