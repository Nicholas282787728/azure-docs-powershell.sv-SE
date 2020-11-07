---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: 3130aec4a5032fd62423aa35dec73d7acd6e14b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919430"
---
# <span data-ttu-id="cc84e-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="cc84e-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="cc84e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cc84e-102">SYNOPSIS</span></span>
<span data-ttu-id="cc84e-103">Testa tillgängligheten för en privat IP-adress i ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="cc84e-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="cc84e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cc84e-104">SYNTAX</span></span>

### <span data-ttu-id="cc84e-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="cc84e-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc84e-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="cc84e-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc84e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cc84e-107">DESCRIPTION</span></span>
<span data-ttu-id="cc84e-108">**Test-AzPrivateIPAddressAvailability** cmdlet testar om en angiven privat IP-adress är tillgänglig i ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="cc84e-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="cc84e-109">Denna cmdlet returnerar en lista över tillgängliga privata IP-adresser om den begärda privata IP-adressen tas.</span><span class="sxs-lookup"><span data-stu-id="cc84e-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="cc84e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cc84e-110">EXAMPLES</span></span>

### <span data-ttu-id="cc84e-111">Exempel 1: testa om en IP-adress är tillgänglig med pipelinen</span><span class="sxs-lookup"><span data-stu-id="cc84e-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="cc84e-112">Det här kommandot får ett virtuellt nätverk och använder operatören för att skicka det till **AzPrivateIPAddressAvailability** , vilket testar om den angivna privata IP-adressen är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="cc84e-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="cc84e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cc84e-113">PARAMETERS</span></span>

### <span data-ttu-id="cc84e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc84e-114">-DefaultProfile</span></span>
<span data-ttu-id="cc84e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cc84e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc84e-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="cc84e-116">-IPAddress</span></span>
<span data-ttu-id="cc84e-117">Anger den IP-adress som ska testas.</span><span class="sxs-lookup"><span data-stu-id="cc84e-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="cc84e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc84e-118">-ResourceGroupName</span></span>
<span data-ttu-id="cc84e-119">Anger namnet på resurs gruppen för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="cc84e-119">Specifies the name of the resource group for the virtual network.</span></span>

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

### <span data-ttu-id="cc84e-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cc84e-120">-VirtualNetwork</span></span>
<span data-ttu-id="cc84e-121">Anger ett **PSVirtualNetwork** -objekt.</span><span class="sxs-lookup"><span data-stu-id="cc84e-121">Specifies a **PSVirtualNetwork** object.</span></span>

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

### <span data-ttu-id="cc84e-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="cc84e-122">-VirtualNetworkName</span></span>
<span data-ttu-id="cc84e-123">Anger namnet på det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="cc84e-123">Specifies the name of the virtual network.</span></span>

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

### <span data-ttu-id="cc84e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc84e-124">CommonParameters</span></span>
<span data-ttu-id="cc84e-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc84e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc84e-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc84e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc84e-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cc84e-127">INPUTS</span></span>

### <span data-ttu-id="cc84e-128">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cc84e-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="cc84e-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cc84e-129">OUTPUTS</span></span>

### <span data-ttu-id="cc84e-130">Microsoft. Azure. commands. Networks. Models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="cc84e-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="cc84e-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cc84e-131">NOTES</span></span>

## <span data-ttu-id="cc84e-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cc84e-132">RELATED LINKS</span></span>

[<span data-ttu-id="cc84e-133">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cc84e-133">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


