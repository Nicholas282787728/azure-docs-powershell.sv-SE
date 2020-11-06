---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientPackage.md
ms.openlocfilehash: 0f6f9adfb75034dc106ba27f63de1ff826f5ab09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586475"
---
# <span data-ttu-id="ed35c-101">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="ed35c-101">Get-AzureRmVpnClientPackage</span></span>

## <span data-ttu-id="ed35c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed35c-102">SYNOPSIS</span></span>
<span data-ttu-id="ed35c-103">Hämtar information om ett VPN-klient paket.</span><span class="sxs-lookup"><span data-stu-id="ed35c-103">Gets information about a VPN client package.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed35c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed35c-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed35c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed35c-105">DESCRIPTION</span></span>
<span data-ttu-id="ed35c-106">Cmdleten **Get-AzureRmVpnClientPackage** hämtar information om de VPN-klient paket som är tillgängliga från en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="ed35c-106">The **Get-AzureRmVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.</span></span>
<span data-ttu-id="ed35c-107">Klient paket innehåller konfigurations data som gör att en klient dator kan göra en VPN-anslutning till ett virtuellt Azure-nätverk. klient datorerna måste ha rätt konfigurations paket installerat för att kunna ringa en VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="ed35c-107">Client packages contain configuration data that enable a client computer to make a VPN connection to an Azure virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.</span></span>
<span data-ttu-id="ed35c-108">Olika konfigurations paket finns tillgängliga baserat på klient datorns version av Windows (till exempel Windows 7 eller Windows 10) och på klient datorns processor arkitektur (AMD64 eller x86).</span><span class="sxs-lookup"><span data-stu-id="ed35c-108">Different configuration packages are available based on the client computer's version of Windows (for example, Windows 7 or Windows 10) and on the client computer's processor architecture (AMD64 or x86).</span></span>
<span data-ttu-id="ed35c-109">Du måste ange arkitektur typen när du kör **Get-AzureRmVpnClientPackage**.</span><span class="sxs-lookup"><span data-stu-id="ed35c-109">You must specify the architecture type when running **Get-AzureRmVpnClientPackage**.</span></span>

## <span data-ttu-id="ed35c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed35c-110">EXAMPLES</span></span>

### <span data-ttu-id="ed35c-111">Exempel 1: Hämta information om ett processor arkitektur för VPN-klienter</span><span class="sxs-lookup"><span data-stu-id="ed35c-111">Example 1: Get information about a processor architecture VPN client package</span></span>
```
PS C:\>Get-AzureRmVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

<span data-ttu-id="ed35c-112">Med det här kommandot får du information om de AMD64 VPN-klient paket som lagras på den virtuella Nätverksgatewayen med namnet ContosoVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="ed35c-112">This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>
<span data-ttu-id="ed35c-113">Om du vill ha information om x86-klient paketen ställer du in värdet på *processorArchitecture* -parametern till x86.</span><span class="sxs-lookup"><span data-stu-id="ed35c-113">To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.</span></span>

## <span data-ttu-id="ed35c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed35c-114">PARAMETERS</span></span>

### <span data-ttu-id="ed35c-115">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="ed35c-115">-ProcessorArchitecture</span></span>
<span data-ttu-id="ed35c-116">Anger vilken typ av CPU-arkitektur som klient paketet är avsett för.</span><span class="sxs-lookup"><span data-stu-id="ed35c-116">Specifies the type of CPU architecture that the client package is designed for.</span></span>
<span data-ttu-id="ed35c-117">Giltiga värden är amd64 och x86.</span><span class="sxs-lookup"><span data-stu-id="ed35c-117">Valid values are Amd64 and X86.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed35c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed35c-118">-ResourceGroupName</span></span>
<span data-ttu-id="ed35c-119">Anger namnet på den resurs grupp som den virtuella Nätverksgatewayen är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="ed35c-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="ed35c-120">Resurs grupper kategoriserar artiklar för att förenkla lager hantering och allmän Azure-administration.</span><span class="sxs-lookup"><span data-stu-id="ed35c-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed35c-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="ed35c-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="ed35c-122">Anger namnet på den virtuella nätverksgateway där klient paket informationen lagras.</span><span class="sxs-lookup"><span data-stu-id="ed35c-122">Specifies the name of the virtual network gateway where the client package information is stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed35c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed35c-123">-DefaultProfile</span></span>
<span data-ttu-id="ed35c-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed35c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed35c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed35c-125">CommonParameters</span></span>
<span data-ttu-id="ed35c-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed35c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed35c-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed35c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed35c-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed35c-128">INPUTS</span></span>

### <span data-ttu-id="ed35c-129">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="ed35c-129">String</span></span>
<span data-ttu-id="ed35c-130">Parametern ' ResourceGroupName ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="ed35c-130">Parameter 'ResourceGroupName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="ed35c-131">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="ed35c-131">String</span></span>
<span data-ttu-id="ed35c-132">Parametern ' VirtualNetworkGatewayName ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="ed35c-132">Parameter 'VirtualNetworkGatewayName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="ed35c-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed35c-133">OUTPUTS</span></span>

###  
<span data-ttu-id="ed35c-134">**Get-AzureRmVpnClientPackage** returnerar instanser av objektet system. String.</span><span class="sxs-lookup"><span data-stu-id="ed35c-134">**Get-AzureRmVpnClientPackage** returns instances of the System.String object.</span></span>

## <span data-ttu-id="ed35c-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed35c-135">NOTES</span></span>

## <span data-ttu-id="ed35c-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed35c-136">RELATED LINKS</span></span>

[<span data-ttu-id="ed35c-137">Ändra storlek – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed35c-137">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="ed35c-138">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="ed35c-138">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


