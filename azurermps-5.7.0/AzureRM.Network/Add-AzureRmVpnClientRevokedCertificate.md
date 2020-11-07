---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 8f1c81dbfb3d8c42b359464ce33a0053fdc25143
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757670"
---
# <span data-ttu-id="2a479-101">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="2a479-101">Add-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="2a479-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a479-102">SYNOPSIS</span></span>
<span data-ttu-id="2a479-103">Lägger till en VPN-klient-åter kallelse intyg.</span><span class="sxs-lookup"><span data-stu-id="2a479-103">Adds a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a479-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a479-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a479-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a479-105">DESCRIPTION</span></span>
<span data-ttu-id="2a479-106">Cmdleten **Add-AzureRmVpnClientRevokedCertificate** tilldelar ett certifikat för klient åter kallelse till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="2a479-106">The **Add-AzureRmVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="2a479-107">Certifikat för klient åter kallelse gör att klient datorer inte använder det angivna certifikatet för att verifiera.</span><span class="sxs-lookup"><span data-stu-id="2a479-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="2a479-108">Du måste ange både certifikat namnet och tumavtrycket för att använda denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a479-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="2a479-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a479-109">EXAMPLES</span></span>

### <span data-ttu-id="2a479-110">Exempel 1: lägga till ett nytt klient certifikat för åter kallelse till en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="2a479-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="2a479-111">Det här kommandot lägger till ett nytt klient åter kallelse certifikat till den virtuella Nätverksgatewayen med namnet ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="2a479-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="2a479-112">För att lägga till certifikatet måste du ange både certifikatets namn och tumavtryck för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="2a479-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="2a479-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a479-113">PARAMETERS</span></span>

### <span data-ttu-id="2a479-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a479-114">-DefaultProfile</span></span>
<span data-ttu-id="2a479-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2a479-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a479-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a479-116">-ResourceGroupName</span></span>
<span data-ttu-id="2a479-117">Anger namnet på den resurs grupp som den virtuella Nätverksgatewayen är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="2a479-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="2a479-118">Resurs grupper kategoriserar artiklar för att förenkla lager hantering och allmän Azure-administration.</span><span class="sxs-lookup"><span data-stu-id="2a479-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="2a479-119">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="2a479-119">-Thumbprint</span></span>
<span data-ttu-id="2a479-120">Anger unikt ID för det certifikat som läggs till.</span><span class="sxs-lookup"><span data-stu-id="2a479-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="2a479-121">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="2a479-121">For example:</span></span>

<span data-ttu-id="2a479-122">-Tumavtryck "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span><span class="sxs-lookup"><span data-stu-id="2a479-122">-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span></span>

<span data-ttu-id="2a479-123">Du kan få information om tumavtryck för dina certifikat genom att använda ett Windows PowerShell-kommando som liknar det `Get-ChildItem -Path Cert:\LocalMachine\Root` här:</span><span class="sxs-lookup"><span data-stu-id="2a479-123">You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>

<span data-ttu-id="2a479-124">Med föregående kommando hämtas information för alla lokala dator certifikat i rot certifikat arkivet.</span><span class="sxs-lookup"><span data-stu-id="2a479-124">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="2a479-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="2a479-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="2a479-126">Anger namnet på den virtuella nätverksgateway där certifikatet ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="2a479-126">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="2a479-127">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="2a479-127">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="2a479-128">Anger namnet på det VPN-klientcertifikat som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="2a479-128">Specifies the name of the VPN client certificate to be added.</span></span>

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

### <span data-ttu-id="2a479-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a479-129">CommonParameters</span></span>
<span data-ttu-id="2a479-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a479-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a479-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a479-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a479-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a479-132">INPUTS</span></span>

### <span data-ttu-id="2a479-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="2a479-133">None</span></span>
<span data-ttu-id="2a479-134">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="2a479-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2a479-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a479-135">OUTPUTS</span></span>

### <span data-ttu-id="2a479-136">Microsoft. Azure. commands. Networks. Models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="2a479-136">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="2a479-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a479-137">NOTES</span></span>

## <span data-ttu-id="2a479-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a479-138">RELATED LINKS</span></span>

[<span data-ttu-id="2a479-139">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="2a479-139">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="2a479-140">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="2a479-140">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="2a479-141">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="2a479-141">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


