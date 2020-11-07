---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrevokedcertificate
schema: 2.0.0
ms.openlocfilehash: e2a2153ca9d75447603ce87c896720ece0f83a18
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931354"
---
# <span data-ttu-id="66889-101">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="66889-101">Add-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="66889-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66889-102">SYNOPSIS</span></span>
<span data-ttu-id="66889-103">Lägger till en VPN-klient-åter kallelse intyg.</span><span class="sxs-lookup"><span data-stu-id="66889-103">Adds a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66889-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66889-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66889-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66889-105">DESCRIPTION</span></span>
<span data-ttu-id="66889-106">Cmdleten **Add-AzureRmVpnClientRevokedCertificate** tilldelar ett certifikat för klient åter kallelse till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="66889-106">The **Add-AzureRmVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="66889-107">Certifikat för klient åter kallelse gör att klient datorer inte använder det angivna certifikatet för att verifiera.</span><span class="sxs-lookup"><span data-stu-id="66889-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="66889-108">Du måste ange både certifikat namnet och tumavtrycket för att använda denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66889-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="66889-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66889-109">EXAMPLES</span></span>

### <span data-ttu-id="66889-110">Exempel 1: lägga till ett nytt klient certifikat för åter kallelse till en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="66889-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="66889-111">Det här kommandot lägger till ett nytt klient åter kallelse certifikat till den virtuella Nätverksgatewayen med namnet ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="66889-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="66889-112">För att lägga till certifikatet måste du ange både certifikatets namn och tumavtryck för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="66889-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="66889-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66889-113">PARAMETERS</span></span>

### <span data-ttu-id="66889-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66889-114">-DefaultProfile</span></span>
<span data-ttu-id="66889-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="66889-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66889-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66889-116">-ResourceGroupName</span></span>
<span data-ttu-id="66889-117">Anger namnet på den resurs grupp som den virtuella Nätverksgatewayen är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="66889-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="66889-118">Resurs grupper kategoriserar artiklar för att förenkla lager hantering och allmän Azure-administration.</span><span class="sxs-lookup"><span data-stu-id="66889-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="66889-119">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="66889-119">-Thumbprint</span></span>
<span data-ttu-id="66889-120">Anger unikt ID för det certifikat som läggs till.</span><span class="sxs-lookup"><span data-stu-id="66889-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="66889-121">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="66889-121">For example:</span></span>

<span data-ttu-id="66889-122">-Tumavtryck "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span><span class="sxs-lookup"><span data-stu-id="66889-122">-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span></span>

<span data-ttu-id="66889-123">Du kan få information om tumavtryck för dina certifikat genom att använda ett Windows PowerShell-kommando som liknar det `Get-ChildItem -Path Cert:\LocalMachine\Root` här:</span><span class="sxs-lookup"><span data-stu-id="66889-123">You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>

<span data-ttu-id="66889-124">Med föregående kommando hämtas information för alla lokala dator certifikat i rot certifikat arkivet.</span><span class="sxs-lookup"><span data-stu-id="66889-124">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="66889-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="66889-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="66889-126">Anger namnet på den virtuella nätverksgateway där certifikatet ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="66889-126">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="66889-127">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="66889-127">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="66889-128">Anger namnet på det VPN-klientcertifikat som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="66889-128">Specifies the name of the VPN client certificate to be added.</span></span>

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

### <span data-ttu-id="66889-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66889-129">CommonParameters</span></span>
<span data-ttu-id="66889-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66889-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66889-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66889-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66889-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66889-132">INPUTS</span></span>

## <span data-ttu-id="66889-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66889-133">OUTPUTS</span></span>

### <span data-ttu-id="66889-134">Microsoft. Azure. commands. Networks. Models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="66889-134">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="66889-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66889-135">NOTES</span></span>

## <span data-ttu-id="66889-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66889-136">RELATED LINKS</span></span>

[<span data-ttu-id="66889-137">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="66889-137">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="66889-138">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="66889-138">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="66889-139">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="66889-139">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


