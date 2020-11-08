---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 70899AAC-BF64-4FFA-9DAF-92E859D0B271
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3b30172f947c1c8bf39a8be84039d9166d6ea290
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099644"
---
# <span data-ttu-id="255f3-101">Set-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="255f3-101">Set-AzureVNetGateway</span></span>

## <span data-ttu-id="255f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="255f3-102">SYNOPSIS</span></span>
<span data-ttu-id="255f3-103">Aktiverar eller inaktiverar en VPN-gateway för ett Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="255f3-103">Enables or disables a VPN gateway for an Azure virtual network.</span></span>

## <span data-ttu-id="255f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="255f3-104">SYNTAX</span></span>

### <span data-ttu-id="255f3-105">Anslut (standard)</span><span class="sxs-lookup"><span data-stu-id="255f3-105">Connect (Default)</span></span>
```
Set-AzureVNetGateway [-Connect] -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="255f3-106">Koppla ner</span><span class="sxs-lookup"><span data-stu-id="255f3-106">Disconnect</span></span>
```
Set-AzureVNetGateway [-Disconnect] -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="255f3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="255f3-107">DESCRIPTION</span></span>
<span data-ttu-id="255f3-108">Cmdleten **set-AzureVNetGateway** aktiverar eller inaktiverar ett virtuellt privat nätverk (VPN) för ett Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="255f3-108">The **Set-AzureVNetGateway** cmdlet enables or disables a virtual private network (VPN) gateway for an Azure virtual network.</span></span>
<span data-ttu-id="255f3-109">En virtuell nätverksgateway är en VPN-slutpunkt för att ansluta till ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="255f3-109">A virtual network gateway is a VPN endpoint for connecting to a virtual network.</span></span>
<span data-ttu-id="255f3-110">Ange parametern *Connect* eller *Connect* för att aktivera eller inaktivera VPN-anslutningen mellan en lokal nätverks webbplats och ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="255f3-110">Specify the *Connect* or *Disconnect* parameter to enable or disable the VPN connection between an on-premises local network site and a virtual network.</span></span>

## <span data-ttu-id="255f3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="255f3-111">EXAMPLES</span></span>

### <span data-ttu-id="255f3-112">Exempel 1: Aktivera en virtuell nätverksgateway för ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="255f3-112">Example 1: Enable a virtual network gateway for a virtual network</span></span>
```
PS C:\> Set-AzureVNetGateway -Connect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

<span data-ttu-id="255f3-113">Det här kommandot aktiverar den virtuella Nätverksgatewayen mellan det virtuella Azure-nätverket med namnet ContosoProdNet och VPN-enheten för den lokala nätverks platsen med namnet ContosoBranchOffice.</span><span class="sxs-lookup"><span data-stu-id="255f3-113">This command enables the virtual network gateway between the Azure virtual network named ContosoProdNet and the VPN device for the local network site named ContosoBranchOffice.</span></span>

### <span data-ttu-id="255f3-114">Exempel 2: inaktivera en virtuell nätverksgateway för ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="255f3-114">Example 2: Disable a virtual network gateway for a virtual network</span></span>
```
PS C:\> Set-AzureVNetGateway -Disconnect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

<span data-ttu-id="255f3-115">Det här kommandot inaktiverar den virtuella Nätverksgatewayen mellan det virtuella Azure-nätverket som heter ContosoProdNet och VPN-enheten för den lokala nätverks platsen med namnet ContosoBranchOffice.</span><span class="sxs-lookup"><span data-stu-id="255f3-115">This command disables the virtual network gateway between the Azure virtual network named ContosoProdNet and the VPN device for the local network site named ContosoBranchOffice.</span></span>

## <span data-ttu-id="255f3-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="255f3-116">PARAMETERS</span></span>

### <span data-ttu-id="255f3-117">-Anslut</span><span class="sxs-lookup"><span data-stu-id="255f3-117">-Connect</span></span>
<span data-ttu-id="255f3-118">Anger att denna cmdlet aktiverar VPN-anslutningen mellan ett virtuellt nätverk och en lokal nätverks webbplats.</span><span class="sxs-lookup"><span data-stu-id="255f3-118">Indicates that this cmdlet enables the VPN connection between a virtual network and a local network site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Connect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="255f3-119">-Koppla ner</span><span class="sxs-lookup"><span data-stu-id="255f3-119">-Disconnect</span></span>
<span data-ttu-id="255f3-120">Anger att denna cmdlet inaktiverar VPN-anslutningen mellan ett virtuellt nätverk och en lokal nätverks webbplats.</span><span class="sxs-lookup"><span data-stu-id="255f3-120">Indicates that this cmdlet disables the VPN connection between a virtual network and a local network site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disconnect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="255f3-121">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="255f3-121">-LocalNetworkSiteName</span></span>
<span data-ttu-id="255f3-122">Anger namnet på den lokala nätverks platsen där denna cmdlet aktiverar eller inaktiverar VPN-anslutningen.</span><span class="sxs-lookup"><span data-stu-id="255f3-122">Specifies the name of the on-premises local network site for which this cmdlet enables or disables the VPN connection.</span></span>

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

### <span data-ttu-id="255f3-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="255f3-123">-Profile</span></span>
<span data-ttu-id="255f3-124">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="255f3-124">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="255f3-125">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="255f3-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="255f3-126">-VNetName</span><span class="sxs-lookup"><span data-stu-id="255f3-126">-VNetName</span></span>
<span data-ttu-id="255f3-127">Anger det virtuella nätverk som denna cmdlet aktiverar eller inaktiverar VPN-anslutningen för.</span><span class="sxs-lookup"><span data-stu-id="255f3-127">Specifies the virtual network for which this cmdlet enables or disables the VPN connection.</span></span>

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

### <span data-ttu-id="255f3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="255f3-128">CommonParameters</span></span>
<span data-ttu-id="255f3-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="255f3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="255f3-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="255f3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="255f3-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="255f3-131">INPUTS</span></span>

## <span data-ttu-id="255f3-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="255f3-132">OUTPUTS</span></span>

## <span data-ttu-id="255f3-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="255f3-133">NOTES</span></span>

## <span data-ttu-id="255f3-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="255f3-134">RELATED LINKS</span></span>

[<span data-ttu-id="255f3-135">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="255f3-135">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="255f3-136">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="255f3-136">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="255f3-137">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="255f3-137">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="255f3-138">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="255f3-138">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="255f3-139">Ändra storlek – AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="255f3-139">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)


