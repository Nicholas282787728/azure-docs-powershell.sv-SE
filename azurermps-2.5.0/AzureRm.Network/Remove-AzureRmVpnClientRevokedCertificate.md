---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientrevokedcertificate
schema: 2.0.0
ms.openlocfilehash: ce4d2c61feb20c750d908b6f235d89dafa713e62
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931189"
---
# <span data-ttu-id="a15f6-101">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a15f6-101">Remove-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="a15f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a15f6-102">SYNOPSIS</span></span>
<span data-ttu-id="a15f6-103">Tar bort en VPN-klient-åter kallelse intyg.</span><span class="sxs-lookup"><span data-stu-id="a15f6-103">Removes a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a15f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a15f6-104">SYNTAX</span></span>

```
Remove-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a15f6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a15f6-105">DESCRIPTION</span></span>
<span data-ttu-id="a15f6-106">Cmdleten **Remove-AzureRmVpnClientRevokedCertificate** tar bort ett certifikat för klient åter kallelse från en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="a15f6-106">The **Remove-AzureRmVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="a15f6-107">Certifikat för klient åter kallelse gör att klient datorer inte använder det angivna certifikatet för att verifiera.</span><span class="sxs-lookup"><span data-stu-id="a15f6-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="a15f6-108">Om du tar bort klient datorer för klient åter kallelse kan du använda det tidigare blockerade certifikatet för att skapa en anslutning till ett virtuellt privat nätverk (VPN).</span><span class="sxs-lookup"><span data-stu-id="a15f6-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="a15f6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a15f6-109">EXAMPLES</span></span>

### <span data-ttu-id="a15f6-110">Exempel 1: ta bort ett certifikat för klient åter kallelse från en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="a15f6-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```
PS C:\>Remove-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="a15f6-111">Det här kommandot tar bort ett certifikat för klient åter kallelse från en virtuell nätverksgateway som heter ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="a15f6-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="a15f6-112">Om du vill ta bort ett certifikat för klient åter kallelse måste du ange både certifikatets namn och tumavtryck för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="a15f6-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="a15f6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a15f6-113">PARAMETERS</span></span>

### <span data-ttu-id="a15f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a15f6-114">-DefaultProfile</span></span>
<span data-ttu-id="a15f6-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a15f6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a15f6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a15f6-116">-ResourceGroupName</span></span>
<span data-ttu-id="a15f6-117">Anger namnet på den resurs grupp som den virtuella Nätverksgatewayen är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="a15f6-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="a15f6-118">Resurs grupper kategoriserar artiklar för att förenkla lager hantering och allmän Azure-administration.</span><span class="sxs-lookup"><span data-stu-id="a15f6-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="a15f6-119">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="a15f6-119">-Thumbprint</span></span>
<span data-ttu-id="a15f6-120">Anger unik identifierare för det certifikat som tas bort.</span><span class="sxs-lookup"><span data-stu-id="a15f6-120">Specifies the unique identifier of the certificate being removed.</span></span>

<span data-ttu-id="a15f6-121">Du kan returnera tumavtryck för dina certifikat genom att använda ett Windows PowerShell-kommando som liknar det här:</span><span class="sxs-lookup"><span data-stu-id="a15f6-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this:</span></span>

`Get-ChildItem -Path "Cert:\LocalMachine\Root"`

<span data-ttu-id="a15f6-122">Föregående kommando returnerar information för alla lokala dator certifikat i rot certifikat arkivet.</span><span class="sxs-lookup"><span data-stu-id="a15f6-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="a15f6-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="a15f6-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="a15f6-124">Anger namnet på den virtuella nätverksgateway som certifikatet har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="a15f6-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="a15f6-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="a15f6-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="a15f6-126">Anger namnet på det VPN-klientcertifikat som tas bort.</span><span class="sxs-lookup"><span data-stu-id="a15f6-126">Specifies the name of the VPN client certificate being removed.</span></span>

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

### <span data-ttu-id="a15f6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a15f6-127">CommonParameters</span></span>
<span data-ttu-id="a15f6-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a15f6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a15f6-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a15f6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a15f6-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a15f6-130">INPUTS</span></span>

## <span data-ttu-id="a15f6-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a15f6-131">OUTPUTS</span></span>

## <span data-ttu-id="a15f6-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a15f6-132">NOTES</span></span>

## <span data-ttu-id="a15f6-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a15f6-133">RELATED LINKS</span></span>

[<span data-ttu-id="a15f6-134">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a15f6-134">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="a15f6-135">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a15f6-135">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="a15f6-136">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a15f6-136">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)


