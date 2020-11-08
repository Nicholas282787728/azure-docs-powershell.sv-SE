---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipconfigurationbgppeeringaddressobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
ms.openlocfilehash: 2a31aa9db3264dd24c6d77bdad7b10d6ecad10b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259301"
---
# <span data-ttu-id="50a7b-101">New-AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="50a7b-101">New-AzIpConfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="50a7b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50a7b-102">SYNOPSIS</span></span>
<span data-ttu-id="50a7b-103">skapar en ny IpconfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="50a7b-103">creates a new IpconfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="50a7b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50a7b-104">SYNTAX</span></span>

### <span data-ttu-id="50a7b-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="50a7b-105">Default (Default)</span></span>
```
New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId <String>
 -CustomAddress <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```
## <span data-ttu-id="50a7b-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50a7b-106">DESCRIPTION</span></span>
<span data-ttu-id="50a7b-107">**New-AzIpConfigurationBgpPeeringAddressObject** skapar ett IpConfigurationBgpPeeringAddressObject-objekt som representerar BgpPeeringAddresses-egenskapen i din virtuella nätverksgateway bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="50a7b-107">The **New-AzIpConfigurationBgpPeeringAddressObject** creates a IpConfigurationBgpPeeringAddressObject object which represents BgpPeeringAddresses property in your virtual network gateway bgpsettings.</span></span>

## <span data-ttu-id="50a7b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50a7b-108">EXAMPLES</span></span>

### <span data-ttu-id="50a7b-109">1: skapa en AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="50a7b-109">1: Create a AzIpConfigurationBgpPeeringAddressObject</span></span>
```
$ipconfigurationId1 = '/subscriptions/c886bc58-0000-4e01-993f-e01ba3702aaf/resourceGroups/testRg/providers/Microsoft.Network/virtualNetworkGateways/gw1/ipConfigurations/default'
$addresslist1 = @('169.254.21.5')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddresses -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
```

<span data-ttu-id="50a7b-110">Ovanstående skapar en IpConfigurationBgpPeeringAddressObject. Detta nya objekt kommer att vara till gw1ipconfBgp1.</span><span class="sxs-lookup"><span data-stu-id="50a7b-110">The above will create a IpConfigurationBgpPeeringAddressObject.This new object will be to gw1ipconfBgp1.</span></span>

## <span data-ttu-id="50a7b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50a7b-111">PARAMETERS</span></span>

### <span data-ttu-id="50a7b-112">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="50a7b-112">-Confirm</span></span>
<span data-ttu-id="50a7b-113">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50a7b-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50a7b-114">-CustomAddress</span><span class="sxs-lookup"><span data-stu-id="50a7b-114">-CustomAddress</span></span>
<span data-ttu-id="50a7b-115">Den virtuella Nätverksgatewayen CustomAddress listan för BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="50a7b-115">The virtual network gateway CustomAddress List for BgpPeeringAddresses.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50a7b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50a7b-116">-DefaultProfile</span></span>
<span data-ttu-id="50a7b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="50a7b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50a7b-118">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="50a7b-118">-IpConfigurationId</span></span>
<span data-ttu-id="50a7b-119">Den virtuella Nätverksgatewayen IpConfigurationId för BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="50a7b-119">The virtual network gateway IpConfigurationId for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="50a7b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50a7b-120">-WhatIf</span></span>
<span data-ttu-id="50a7b-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="50a7b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50a7b-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="50a7b-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50a7b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50a7b-123">CommonParameters</span></span>
<span data-ttu-id="50a7b-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50a7b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50a7b-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50a7b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50a7b-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50a7b-126">INPUTS</span></span>

### <span data-ttu-id="50a7b-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="50a7b-127">None</span></span>

## <span data-ttu-id="50a7b-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50a7b-128">OUTPUTS</span></span>

### <span data-ttu-id="50a7b-129">Microsoft. Azure. commands. Networks. Models. PSIpConfigurationBgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="50a7b-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span></span>

## <span data-ttu-id="50a7b-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50a7b-130">NOTES</span></span>

## <span data-ttu-id="50a7b-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50a7b-131">RELATED LINKS</span></span>
