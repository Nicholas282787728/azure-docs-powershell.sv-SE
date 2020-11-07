---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 04bc51a7040cae1310fd3c4fe51fd45c425fad8e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926481"
---
# <span data-ttu-id="5f630-101">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="5f630-101">Get-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="5f630-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f630-102">SYNOPSIS</span></span>
<span data-ttu-id="5f630-103">Hämtar information om certifikat för återkallade klienter.</span><span class="sxs-lookup"><span data-stu-id="5f630-103">Gets information about VPN client-revocation certificates.</span></span>

## <span data-ttu-id="5f630-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f630-104">SYNTAX</span></span>

```
Get-AzVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f630-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f630-105">DESCRIPTION</span></span>
<span data-ttu-id="5f630-106">Cmdleten **Get-AzVpnClientRevokedCertificate** returnerar information om återkallade klient certifikat som har tilldelats till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="5f630-106">The **Get-AzVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="5f630-107">Certifikat för klient åter kallelse gör att klient datorer inte använder det angivna certifikatet för att verifiera.</span><span class="sxs-lookup"><span data-stu-id="5f630-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="5f630-108">**Get-AzVpnClientRevokedCertificate** gör att du kan returnera information om alla klient återkallnings certifikat på gatewayen eller genom att använda parametern *VpnClientRevokedCertificateName* för att få information om ett enda certifikat.</span><span class="sxs-lookup"><span data-stu-id="5f630-108">**Get-AzVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="5f630-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f630-109">EXAMPLES</span></span>

### <span data-ttu-id="5f630-110">Exempel 1: få information om alla certifikat för återkallning från klient</span><span class="sxs-lookup"><span data-stu-id="5f630-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="5f630-111">Det här kommandot får information om alla klient återkallnings certifikat som är kopplade till den virtuella Nätverksgatewayen med namnet ContosoVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="5f630-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="5f630-112">Exempel 2: få information om specifika certifikat för åter kallelse av klient</span><span class="sxs-lookup"><span data-stu-id="5f630-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="5f630-113">Det här kommandot är en variant av kommandot som visas i exempel 1.</span><span class="sxs-lookup"><span data-stu-id="5f630-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="5f630-114">I det här fallet används *VpnClientRevokedCertificateName* -parametern för att begränsa den returnerade informationen till ett specifikt klient-återkallat certifikat: certifikatet med namnet ContosoRevokedClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="5f630-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="5f630-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f630-115">PARAMETERS</span></span>

### <span data-ttu-id="5f630-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f630-116">-DefaultProfile</span></span>
<span data-ttu-id="5f630-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5f630-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f630-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f630-118">-ResourceGroupName</span></span>
<span data-ttu-id="5f630-119">Anger namnet på den resurs grupp som den virtuella Nätverksgatewayen är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="5f630-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="5f630-120">Resurs grupper kategoriserar artiklar för att förenkla lager hantering och allmän Azure-administration.</span><span class="sxs-lookup"><span data-stu-id="5f630-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f630-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="5f630-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="5f630-122">Anger namnet på den virtuella nätverksgateway där den återkallade certifikat informationen är tilldelad.</span><span class="sxs-lookup"><span data-stu-id="5f630-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f630-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="5f630-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="5f630-124">Anger namnet på det VPN-klient certifikat som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="5f630-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f630-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f630-125">CommonParameters</span></span>
<span data-ttu-id="5f630-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f630-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f630-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f630-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f630-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f630-128">INPUTS</span></span>

### <span data-ttu-id="5f630-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5f630-129">System.String</span></span>

## <span data-ttu-id="5f630-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f630-130">OUTPUTS</span></span>

### <span data-ttu-id="5f630-131">Microsoft. Azure. commands. Networks. Models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="5f630-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="5f630-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f630-132">NOTES</span></span>

## <span data-ttu-id="5f630-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f630-133">RELATED LINKS</span></span>

[<span data-ttu-id="5f630-134">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="5f630-134">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="5f630-135">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="5f630-135">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="5f630-136">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="5f630-136">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


