---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
ms.openlocfilehash: 880e079d5facec2edc20f38d7d1e1d4c9ba41e41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577612"
---
# <span data-ttu-id="892f7-101">Test-AzureRmPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="892f7-101">Test-AzureRmPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="892f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="892f7-102">SYNOPSIS</span></span>
<span data-ttu-id="892f7-103">Testa tillgängligheten för en privat IP-adress i ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="892f7-103">Test availability of a private IP address in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="892f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="892f7-104">SYNTAX</span></span>

### <span data-ttu-id="892f7-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="892f7-105">TestByResource</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="892f7-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="892f7-106">TestByResourceId</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="892f7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="892f7-107">DESCRIPTION</span></span>
<span data-ttu-id="892f7-108">**Test-AzureRmPrivateIPAddressAvailability** cmdlet testar om en angiven privat IP-adress är tillgänglig i ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="892f7-108">The **Test-AzureRmPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="892f7-109">Denna cmdlet returnerar en lista över tillgängliga privata IP-adresser om den begärda privata IP-adressen tas.</span><span class="sxs-lookup"><span data-stu-id="892f7-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="892f7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="892f7-110">EXAMPLES</span></span>

### <span data-ttu-id="892f7-111">Exempel 1: testa om en IP-adress är tillgänglig med pipelinen</span><span class="sxs-lookup"><span data-stu-id="892f7-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzureRmVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzureRmPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="892f7-112">Det här kommandot får ett virtuellt nätverk och använder operatören för att skicka det till **AzureRmPrivateIPAddressAvailability** , vilket testar om den angivna privata IP-adressen är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="892f7-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzureRmPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="892f7-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="892f7-113">PARAMETERS</span></span>

### <span data-ttu-id="892f7-114">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="892f7-114">-IPAddress</span></span>
<span data-ttu-id="892f7-115">Anger den IP-adress som ska testas.</span><span class="sxs-lookup"><span data-stu-id="892f7-115">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="892f7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="892f7-116">-ResourceGroupName</span></span>
<span data-ttu-id="892f7-117">Anger namnet på resurs gruppen för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="892f7-117">Specifies the name of the resource group for the virtual network.</span></span>

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

### <span data-ttu-id="892f7-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="892f7-118">-VirtualNetwork</span></span>
<span data-ttu-id="892f7-119">Anger ett **PSVirtualNetwork** -objekt.</span><span class="sxs-lookup"><span data-stu-id="892f7-119">Specifies a **PSVirtualNetwork** object.</span></span>

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

### <span data-ttu-id="892f7-120">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="892f7-120">-VirtualNetworkName</span></span>
<span data-ttu-id="892f7-121">Anger namnet på det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="892f7-121">Specifies the name of the virtual network.</span></span>

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

### <span data-ttu-id="892f7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="892f7-122">-DefaultProfile</span></span>
<span data-ttu-id="892f7-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="892f7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="892f7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="892f7-124">CommonParameters</span></span>
<span data-ttu-id="892f7-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="892f7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="892f7-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="892f7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="892f7-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="892f7-127">INPUTS</span></span>

### <span data-ttu-id="892f7-128">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="892f7-128">PSVirtualNetwork</span></span>
<span data-ttu-id="892f7-129">Parametern ' VirtualNetwork ' godkänner värdet av typen ' PSVirtualNetwork ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="892f7-129">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="892f7-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="892f7-130">OUTPUTS</span></span>

### <span data-ttu-id="892f7-131">Microsoft. Azure. commands. Networks. Models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="892f7-131">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="892f7-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="892f7-132">NOTES</span></span>

## <span data-ttu-id="892f7-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="892f7-133">RELATED LINKS</span></span>

[<span data-ttu-id="892f7-134">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="892f7-134">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)


