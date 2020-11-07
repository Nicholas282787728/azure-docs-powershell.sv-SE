---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: af5e1591e0d5c497b0cfe854235536d7edf404c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926486"
---
# <span data-ttu-id="5d32c-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="5d32c-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="5d32c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5d32c-102">SYNOPSIS</span></span>
<span data-ttu-id="5d32c-103">Testa tillgängligheten för en privat IP-adress i ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="5d32c-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="5d32c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5d32c-104">SYNTAX</span></span>

### <span data-ttu-id="5d32c-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="5d32c-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d32c-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="5d32c-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d32c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5d32c-107">DESCRIPTION</span></span>
<span data-ttu-id="5d32c-108">**Test-AzPrivateIPAddressAvailability** cmdlet testar om en angiven privat IP-adress är tillgänglig i ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="5d32c-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="5d32c-109">Denna cmdlet returnerar en lista över tillgängliga privata IP-adresser om den begärda privata IP-adressen tas.</span><span class="sxs-lookup"><span data-stu-id="5d32c-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="5d32c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5d32c-110">EXAMPLES</span></span>

### <span data-ttu-id="5d32c-111">Exempel 1: testa om en IP-adress är tillgänglig med pipelinen</span><span class="sxs-lookup"><span data-stu-id="5d32c-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="5d32c-112">Det här kommandot får ett virtuellt nätverk och använder operatören för att skicka det till **AzPrivateIPAddressAvailability** , vilket testar om den angivna privata IP-adressen är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="5d32c-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="5d32c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5d32c-113">PARAMETERS</span></span>

### <span data-ttu-id="5d32c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d32c-114">-DefaultProfile</span></span>
<span data-ttu-id="5d32c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5d32c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d32c-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="5d32c-116">-IPAddress</span></span>
<span data-ttu-id="5d32c-117">Anger den IP-adress som ska testas.</span><span class="sxs-lookup"><span data-stu-id="5d32c-117">Specifies the IP address to test.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d32c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d32c-118">-ResourceGroupName</span></span>
<span data-ttu-id="5d32c-119">Anger namnet på resurs gruppen för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="5d32c-119">Specifies the name of the resource group for the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d32c-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5d32c-120">-VirtualNetwork</span></span>
<span data-ttu-id="5d32c-121">Anger ett **PSVirtualNetwork** -objekt.</span><span class="sxs-lookup"><span data-stu-id="5d32c-121">Specifies a **PSVirtualNetwork** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: TestByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d32c-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="5d32c-122">-VirtualNetworkName</span></span>
<span data-ttu-id="5d32c-123">Anger namnet på det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="5d32c-123">Specifies the name of the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d32c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d32c-124">CommonParameters</span></span>
<span data-ttu-id="5d32c-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d32c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d32c-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d32c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d32c-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5d32c-127">INPUTS</span></span>

### <span data-ttu-id="5d32c-128">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5d32c-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="5d32c-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5d32c-129">OUTPUTS</span></span>

### <span data-ttu-id="5d32c-130">Microsoft. Azure. commands. Networks. Models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="5d32c-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="5d32c-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5d32c-131">NOTES</span></span>

## <span data-ttu-id="5d32c-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5d32c-132">RELATED LINKS</span></span>

[<span data-ttu-id="5d32c-133">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5d32c-133">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


