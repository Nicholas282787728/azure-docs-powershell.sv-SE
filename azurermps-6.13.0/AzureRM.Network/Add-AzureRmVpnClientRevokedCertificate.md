---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: c770bc2bb7c3fde9475ee844e12b8ed8c457dd56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757576"
---
# <span data-ttu-id="62f21-101">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="62f21-101">Add-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="62f21-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62f21-102">SYNOPSIS</span></span>
<span data-ttu-id="62f21-103">Lägger till en VPN-klient-åter kallelse intyg.</span><span class="sxs-lookup"><span data-stu-id="62f21-103">Adds a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62f21-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62f21-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62f21-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62f21-105">DESCRIPTION</span></span>
<span data-ttu-id="62f21-106">Cmdleten **Add-AzureRmVpnClientRevokedCertificate** tilldelar ett certifikat för klient åter kallelse till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="62f21-106">The **Add-AzureRmVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="62f21-107">Certifikat för klient åter kallelse gör att klient datorer inte använder det angivna certifikatet för att verifiera.</span><span class="sxs-lookup"><span data-stu-id="62f21-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="62f21-108">Du måste ange både certifikat namnet och tumavtrycket för att använda denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62f21-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="62f21-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62f21-109">EXAMPLES</span></span>

### <span data-ttu-id="62f21-110">Exempel 1: lägga till ett nytt klient certifikat för åter kallelse till en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="62f21-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="62f21-111">Det här kommandot lägger till ett nytt klient åter kallelse certifikat till den virtuella Nätverksgatewayen med namnet ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="62f21-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="62f21-112">För att lägga till certifikatet måste du ange både certifikatets namn och tumavtryck för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="62f21-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="62f21-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62f21-113">PARAMETERS</span></span>

### <span data-ttu-id="62f21-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62f21-114">-DefaultProfile</span></span>
<span data-ttu-id="62f21-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="62f21-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62f21-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62f21-116">-ResourceGroupName</span></span>
<span data-ttu-id="62f21-117">Anger namnet på den resurs grupp som den virtuella Nätverksgatewayen är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="62f21-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="62f21-118">Resurs grupper kategoriserar artiklar för att förenkla lager hantering och allmän Azure-administration.</span><span class="sxs-lookup"><span data-stu-id="62f21-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="62f21-119">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="62f21-119">-Thumbprint</span></span>
<span data-ttu-id="62f21-120">Anger unikt ID för det certifikat som läggs till.</span><span class="sxs-lookup"><span data-stu-id="62f21-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="62f21-121">Till exempel:-tumavtryck "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" du kan få tumavtryck för dina certifikat genom att använda ett Windows PowerShell-kommando som liknar det `Get-ChildItem -Path Cert:\LocalMachine\Root` här:</span><span class="sxs-lookup"><span data-stu-id="62f21-121">For example: -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>
<span data-ttu-id="62f21-122">Med föregående kommando hämtas information för alla lokala dator certifikat i rot certifikat arkivet.</span><span class="sxs-lookup"><span data-stu-id="62f21-122">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="62f21-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="62f21-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="62f21-124">Anger namnet på den virtuella nätverksgateway där certifikatet ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="62f21-124">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="62f21-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="62f21-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="62f21-126">Anger namnet på det VPN-klientcertifikat som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="62f21-126">Specifies the name of the VPN client certificate to be added.</span></span>

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

### <span data-ttu-id="62f21-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62f21-127">CommonParameters</span></span>
<span data-ttu-id="62f21-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62f21-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62f21-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62f21-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62f21-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62f21-130">INPUTS</span></span>

### <span data-ttu-id="62f21-131">System. String</span><span class="sxs-lookup"><span data-stu-id="62f21-131">System.String</span></span>

## <span data-ttu-id="62f21-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62f21-132">OUTPUTS</span></span>

### <span data-ttu-id="62f21-133">Microsoft. Azure. commands. Networks. Models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="62f21-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="62f21-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62f21-134">NOTES</span></span>

## <span data-ttu-id="62f21-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62f21-135">RELATED LINKS</span></span>

[<span data-ttu-id="62f21-136">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="62f21-136">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="62f21-137">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="62f21-137">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="62f21-138">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="62f21-138">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


