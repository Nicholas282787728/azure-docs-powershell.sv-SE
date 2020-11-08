---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 54d3d5db9356badb5e9b28eeff8b51cf7b8ce504
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090247"
---
# <span data-ttu-id="817f6-101">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="817f6-101">Add-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="817f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="817f6-102">SYNOPSIS</span></span>
<span data-ttu-id="817f6-103">Lägger till en VPN-klient-åter kallelse intyg.</span><span class="sxs-lookup"><span data-stu-id="817f6-103">Adds a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="817f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="817f6-104">SYNTAX</span></span>

```
Add-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="817f6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="817f6-105">DESCRIPTION</span></span>
<span data-ttu-id="817f6-106">Cmdleten **Add-AzVpnClientRevokedCertificate** tilldelar ett certifikat för klient åter kallelse till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="817f6-106">The **Add-AzVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="817f6-107">Certifikat för klient åter kallelse gör att klient datorer inte använder det angivna certifikatet för att verifiera.</span><span class="sxs-lookup"><span data-stu-id="817f6-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="817f6-108">Du måste ange både certifikat namnet och tumavtrycket för att använda denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="817f6-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="817f6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="817f6-109">EXAMPLES</span></span>

### <span data-ttu-id="817f6-110">Exempel 1: lägga till ett nytt klient certifikat för åter kallelse till en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="817f6-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="817f6-111">Det här kommandot lägger till ett nytt klient åter kallelse certifikat till den virtuella Nätverksgatewayen med namnet ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="817f6-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="817f6-112">För att lägga till certifikatet måste du ange både certifikatets namn och tumavtryck för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="817f6-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="817f6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="817f6-113">PARAMETERS</span></span>

### <span data-ttu-id="817f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="817f6-114">-DefaultProfile</span></span>
<span data-ttu-id="817f6-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="817f6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="817f6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="817f6-116">-ResourceGroupName</span></span>
<span data-ttu-id="817f6-117">Anger namnet på den resurs grupp som den virtuella Nätverksgatewayen är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="817f6-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="817f6-118">Resurs grupper kategoriserar artiklar för att förenkla lager hantering och allmän Azure-administration.</span><span class="sxs-lookup"><span data-stu-id="817f6-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="817f6-119">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="817f6-119">-Thumbprint</span></span>
<span data-ttu-id="817f6-120">Anger unikt ID för det certifikat som läggs till.</span><span class="sxs-lookup"><span data-stu-id="817f6-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="817f6-121">Till exempel:-tumavtryck "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" du kan få tumavtryck för dina certifikat genom att använda ett Windows PowerShell-kommando som liknar det `Get-ChildItem -Path Cert:\LocalMachine\Root` här:</span><span class="sxs-lookup"><span data-stu-id="817f6-121">For example: -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>
<span data-ttu-id="817f6-122">Med föregående kommando hämtas information för alla lokala dator certifikat i rot certifikat arkivet.</span><span class="sxs-lookup"><span data-stu-id="817f6-122">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="817f6-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="817f6-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="817f6-124">Anger namnet på den virtuella nätverksgateway där certifikatet ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="817f6-124">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="817f6-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="817f6-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="817f6-126">Anger namnet på det VPN-klientcertifikat som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="817f6-126">Specifies the name of the VPN client certificate to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="817f6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="817f6-127">CommonParameters</span></span>
<span data-ttu-id="817f6-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="817f6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="817f6-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="817f6-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="817f6-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="817f6-130">INPUTS</span></span>

### <span data-ttu-id="817f6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="817f6-131">System.String</span></span>

## <span data-ttu-id="817f6-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="817f6-132">OUTPUTS</span></span>

### <span data-ttu-id="817f6-133">Microsoft. Azure. commands. Networks. Models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="817f6-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="817f6-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="817f6-134">NOTES</span></span>

## <span data-ttu-id="817f6-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="817f6-135">RELATED LINKS</span></span>

[<span data-ttu-id="817f6-136">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="817f6-136">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="817f6-137">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="817f6-137">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="817f6-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="817f6-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


