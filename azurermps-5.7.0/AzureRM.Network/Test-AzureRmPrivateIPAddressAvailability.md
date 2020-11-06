---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
ms.openlocfilehash: 769f8a5f8f95e5a97af8a495e0edbaba6b75a5d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577125"
---
# <span data-ttu-id="0f2ad-101">Test-AzureRmPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="0f2ad-101">Test-AzureRmPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="0f2ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0f2ad-102">SYNOPSIS</span></span>
<span data-ttu-id="0f2ad-103">Testa tillgängligheten för en privat IP-adress i ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-103">Test availability of a private IP address in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f2ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0f2ad-104">SYNTAX</span></span>

### <span data-ttu-id="0f2ad-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="0f2ad-105">TestByResource</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f2ad-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="0f2ad-106">TestByResourceId</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f2ad-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0f2ad-107">DESCRIPTION</span></span>
<span data-ttu-id="0f2ad-108">**Test-AzureRmPrivateIPAddressAvailability** cmdlet testar om en angiven privat IP-adress är tillgänglig i ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-108">The **Test-AzureRmPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="0f2ad-109">Denna cmdlet returnerar en lista över tillgängliga privata IP-adresser om den begärda privata IP-adressen tas.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="0f2ad-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0f2ad-110">EXAMPLES</span></span>

### <span data-ttu-id="0f2ad-111">Exempel 1: testa om en IP-adress är tillgänglig med pipelinen</span><span class="sxs-lookup"><span data-stu-id="0f2ad-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzureRmVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzureRmPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="0f2ad-112">Det här kommandot får ett virtuellt nätverk och använder operatören för att skicka det till **AzureRmPrivateIPAddressAvailability** , vilket testar om den angivna privata IP-adressen är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzureRmPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="0f2ad-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0f2ad-113">PARAMETERS</span></span>

### <span data-ttu-id="0f2ad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f2ad-114">-DefaultProfile</span></span>
<span data-ttu-id="0f2ad-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f2ad-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="0f2ad-116">-IPAddress</span></span>
<span data-ttu-id="0f2ad-117">Anger den IP-adress som ska testas.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="0f2ad-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f2ad-118">-ResourceGroupName</span></span>
<span data-ttu-id="0f2ad-119">Anger namnet på resurs gruppen för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-119">Specifies the name of the resource group for the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f2ad-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0f2ad-120">-VirtualNetwork</span></span>
<span data-ttu-id="0f2ad-121">Anger ett **PSVirtualNetwork** -objekt.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-121">Specifies a **PSVirtualNetwork** object.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: TestByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f2ad-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="0f2ad-122">-VirtualNetworkName</span></span>
<span data-ttu-id="0f2ad-123">Anger namnet på det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-123">Specifies the name of the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f2ad-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f2ad-124">CommonParameters</span></span>
<span data-ttu-id="0f2ad-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f2ad-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f2ad-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f2ad-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0f2ad-127">INPUTS</span></span>

### <span data-ttu-id="0f2ad-128">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0f2ad-128">PSVirtualNetwork</span></span>
<span data-ttu-id="0f2ad-129">Parametern ' VirtualNetwork ' godkänner värdet av typen ' PSVirtualNetwork ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="0f2ad-129">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="0f2ad-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0f2ad-130">OUTPUTS</span></span>

### <span data-ttu-id="0f2ad-131">Microsoft. Azure. commands. Networks. Models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="0f2ad-131">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="0f2ad-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0f2ad-132">NOTES</span></span>

## <span data-ttu-id="0f2ad-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0f2ad-133">RELATED LINKS</span></span>

[<span data-ttu-id="0f2ad-134">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0f2ad-134">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)


