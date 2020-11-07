---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientrevokedcertificate
schema: 2.0.0
ms.openlocfilehash: 62fc89cefadc91445a64850d6a0e5ee23d6163f0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929757"
---
# <span data-ttu-id="7a880-101">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="7a880-101">Get-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="7a880-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7a880-102">SYNOPSIS</span></span>
<span data-ttu-id="7a880-103">Hämtar information om certifikat för återkallade klienter.</span><span class="sxs-lookup"><span data-stu-id="7a880-103">Gets information about VPN client-revocation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a880-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7a880-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a880-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7a880-105">DESCRIPTION</span></span>
<span data-ttu-id="7a880-106">Cmdleten **Get-AzureRmVpnClientRevokedCertificate** returnerar information om återkallade klient certifikat som har tilldelats till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="7a880-106">The **Get-AzureRmVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="7a880-107">Certifikat för klient åter kallelse gör att klient datorer inte använder det angivna certifikatet för att verifiera.</span><span class="sxs-lookup"><span data-stu-id="7a880-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="7a880-108">**Get-AzureRmVpnClientRevokedCertificate** gör att du kan returnera information om alla klient återkallnings certifikat på gatewayen eller genom att använda parametern *VpnClientRevokedCertificateName* för att få information om ett enda certifikat.</span><span class="sxs-lookup"><span data-stu-id="7a880-108">**Get-AzureRmVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="7a880-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7a880-109">EXAMPLES</span></span>

### <span data-ttu-id="7a880-110">Exempel 1: få information om alla certifikat för återkallning från klient</span><span class="sxs-lookup"><span data-stu-id="7a880-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="7a880-111">Det här kommandot får information om alla klient återkallnings certifikat som är kopplade till den virtuella Nätverksgatewayen med namnet ContosoVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="7a880-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="7a880-112">Exempel 2: få information om specifika certifikat för åter kallelse av klient</span><span class="sxs-lookup"><span data-stu-id="7a880-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="7a880-113">Det här kommandot är en variant av kommandot som visas i exempel 1.</span><span class="sxs-lookup"><span data-stu-id="7a880-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="7a880-114">I det här fallet används *VpnClientRevokedCertificateName* -parametern för att begränsa den returnerade informationen till ett specifikt klient-återkallat certifikat: certifikatet med namnet ContosoRevokedClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="7a880-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="7a880-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7a880-115">PARAMETERS</span></span>

### <span data-ttu-id="7a880-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a880-116">-DefaultProfile</span></span>
<span data-ttu-id="7a880-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7a880-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a880-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a880-118">-ResourceGroupName</span></span>
<span data-ttu-id="7a880-119">Anger namnet på den resurs grupp som den virtuella Nätverksgatewayen är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="7a880-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="7a880-120">Resurs grupper kategoriserar artiklar för att förenkla lager hantering och allmän Azure-administration.</span><span class="sxs-lookup"><span data-stu-id="7a880-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a880-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="7a880-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="7a880-122">Anger namnet på den virtuella nätverksgateway där den återkallade certifikat informationen är tilldelad.</span><span class="sxs-lookup"><span data-stu-id="7a880-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a880-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="7a880-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="7a880-124">Anger namnet på det VPN-klient certifikat som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="7a880-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a880-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a880-125">CommonParameters</span></span>
<span data-ttu-id="7a880-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a880-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a880-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a880-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a880-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7a880-128">INPUTS</span></span>

## <span data-ttu-id="7a880-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7a880-129">OUTPUTS</span></span>

###  
<span data-ttu-id="7a880-130">**Get-AzureRmVpnClientRevokedCertificate** returnerar instanser av **Microsoft. Azure. commands. Network. Models. PSVpnClientRevokedCertificate** .</span><span class="sxs-lookup"><span data-stu-id="7a880-130">**Get-AzureRmVpnClientRevokedCertificate** returns instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate** object.</span></span>

## <span data-ttu-id="7a880-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7a880-131">NOTES</span></span>

## <span data-ttu-id="7a880-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7a880-132">RELATED LINKS</span></span>

[<span data-ttu-id="7a880-133">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="7a880-133">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="7a880-134">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="7a880-134">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="7a880-135">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="7a880-135">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


