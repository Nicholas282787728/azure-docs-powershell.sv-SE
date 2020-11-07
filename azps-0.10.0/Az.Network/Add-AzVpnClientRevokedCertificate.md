---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 384d5b88ce9a52ad5f68c009c7b610610c695ce2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922349"
---
# <span data-ttu-id="bd0f1-101">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="bd0f1-101">Add-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="bd0f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd0f1-102">SYNOPSIS</span></span>
<span data-ttu-id="bd0f1-103">Lägger till en VPN-klient-åter kallelse intyg.</span><span class="sxs-lookup"><span data-stu-id="bd0f1-103">Adds a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="bd0f1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd0f1-104">SYNTAX</span></span>

```
Add-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd0f1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd0f1-105">DESCRIPTION</span></span>
<span data-ttu-id="bd0f1-106">Cmdleten **Add-AzVpnClientRevokedCertificate** tilldelar ett certifikat för klient åter kallelse till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="bd0f1-106">The **Add-AzVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="bd0f1-107">Certifikat för klient åter kallelse gör att klient datorer inte använder det angivna certifikatet för att verifiera.</span><span class="sxs-lookup"><span data-stu-id="bd0f1-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="bd0f1-108">Du måste ange både certifikat namnet och tumavtrycket för att använda denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd0f1-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="bd0f1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd0f1-109">EXAMPLES</span></span>

### <span data-ttu-id="bd0f1-110">Exempel 1: lägga till ett nytt klient certifikat för åter kallelse till en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="bd0f1-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="bd0f1-111">Det här kommandot lägger till ett nytt klient åter kallelse certifikat till den virtuella Nätverksgatewayen med namnet ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="bd0f1-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="bd0f1-112">För att lägga till certifikatet måste du ange både certifikatets namn och tumavtryck för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="bd0f1-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="bd0f1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd0f1-113">PARAMETERS</span></span>

### <span data-ttu-id="bd0f1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd0f1-114">-DefaultProfile</span></span>
<span data-ttu-id="bd0f1-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd0f1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd0f1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd0f1-116">-ResourceGroupName</span></span>
<span data-ttu-id="bd0f1-117">Anger namnet på den resurs grupp som den virtuella Nätverksgatewayen är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="bd0f1-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="bd0f1-118">Resurs grupper kategoriserar artiklar för att förenkla lager hantering och allmän Azure-administration.</span><span class="sxs-lookup"><span data-stu-id="bd0f1-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="bd0f1-119">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="bd0f1-119">-Thumbprint</span></span>
<span data-ttu-id="bd0f1-120">Anger unikt ID för det certifikat som läggs till.</span><span class="sxs-lookup"><span data-stu-id="bd0f1-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="bd0f1-121">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="bd0f1-121">For example:</span></span>

<span data-ttu-id="bd0f1-122">-Tumavtryck "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span><span class="sxs-lookup"><span data-stu-id="bd0f1-122">-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span></span>

<span data-ttu-id="bd0f1-123">Du kan få information om tumavtryck för dina certifikat genom att använda ett Windows PowerShell-kommando som liknar det `Get-ChildItem -Path Cert:\LocalMachine\Root` här:</span><span class="sxs-lookup"><span data-stu-id="bd0f1-123">You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>

<span data-ttu-id="bd0f1-124">Med föregående kommando hämtas information för alla lokala dator certifikat i rot certifikat arkivet.</span><span class="sxs-lookup"><span data-stu-id="bd0f1-124">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="bd0f1-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="bd0f1-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="bd0f1-126">Anger namnet på den virtuella nätverksgateway där certifikatet ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="bd0f1-126">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="bd0f1-127">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="bd0f1-127">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="bd0f1-128">Anger namnet på det VPN-klientcertifikat som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="bd0f1-128">Specifies the name of the VPN client certificate to be added.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0f1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd0f1-129">CommonParameters</span></span>
<span data-ttu-id="bd0f1-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd0f1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd0f1-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd0f1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd0f1-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd0f1-132">INPUTS</span></span>

## <span data-ttu-id="bd0f1-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd0f1-133">OUTPUTS</span></span>

### <span data-ttu-id="bd0f1-134">Microsoft. Azure. commands. Networks. Models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="bd0f1-134">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="bd0f1-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd0f1-135">NOTES</span></span>

## <span data-ttu-id="bd0f1-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd0f1-136">RELATED LINKS</span></span>

[<span data-ttu-id="bd0f1-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="bd0f1-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="bd0f1-138">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="bd0f1-138">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="bd0f1-139">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="bd0f1-139">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


