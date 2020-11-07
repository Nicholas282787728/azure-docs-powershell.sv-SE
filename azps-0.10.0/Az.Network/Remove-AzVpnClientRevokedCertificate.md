---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 3ea5a6ba20b02fd7289e597683d97c1513aa9873
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924310"
---
# <span data-ttu-id="898f9-101">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="898f9-101">Remove-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="898f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="898f9-102">SYNOPSIS</span></span>
<span data-ttu-id="898f9-103">Tar bort en VPN-klient-åter kallelse intyg.</span><span class="sxs-lookup"><span data-stu-id="898f9-103">Removes a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="898f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="898f9-104">SYNTAX</span></span>

```
Remove-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="898f9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="898f9-105">DESCRIPTION</span></span>
<span data-ttu-id="898f9-106">Cmdleten **Remove-AzVpnClientRevokedCertificate** tar bort ett certifikat för klient åter kallelse från en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="898f9-106">The **Remove-AzVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="898f9-107">Certifikat för klient åter kallelse gör att klient datorer inte använder det angivna certifikatet för att verifiera.</span><span class="sxs-lookup"><span data-stu-id="898f9-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="898f9-108">Om du tar bort klient datorer för klient åter kallelse kan du använda det tidigare blockerade certifikatet för att skapa en anslutning till ett virtuellt privat nätverk (VPN).</span><span class="sxs-lookup"><span data-stu-id="898f9-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="898f9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="898f9-109">EXAMPLES</span></span>

### <span data-ttu-id="898f9-110">Exempel 1: ta bort ett certifikat för klient åter kallelse från en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="898f9-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```
PS C:\>Remove-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="898f9-111">Det här kommandot tar bort ett certifikat för klient åter kallelse från en virtuell nätverksgateway som heter ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="898f9-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="898f9-112">Om du vill ta bort ett certifikat för klient åter kallelse måste du ange både certifikatets namn och tumavtryck för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="898f9-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="898f9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="898f9-113">PARAMETERS</span></span>

### <span data-ttu-id="898f9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="898f9-114">-DefaultProfile</span></span>
<span data-ttu-id="898f9-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="898f9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="898f9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="898f9-116">-ResourceGroupName</span></span>
<span data-ttu-id="898f9-117">Anger namnet på den resurs grupp som den virtuella Nätverksgatewayen är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="898f9-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="898f9-118">Resurs grupper kategoriserar artiklar för att förenkla lager hantering och allmän Azure-administration.</span><span class="sxs-lookup"><span data-stu-id="898f9-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="898f9-119">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="898f9-119">-Thumbprint</span></span>
<span data-ttu-id="898f9-120">Anger unik identifierare för det certifikat som tas bort.</span><span class="sxs-lookup"><span data-stu-id="898f9-120">Specifies the unique identifier of the certificate being removed.</span></span>

<span data-ttu-id="898f9-121">Du kan returnera tumavtryck för dina certifikat genom att använda ett Windows PowerShell-kommando som liknar det här:</span><span class="sxs-lookup"><span data-stu-id="898f9-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this:</span></span>

`Get-ChildItem -Path "Cert:\LocalMachine\Root"`

<span data-ttu-id="898f9-122">Föregående kommando returnerar information för alla lokala dator certifikat i rot certifikat arkivet.</span><span class="sxs-lookup"><span data-stu-id="898f9-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="898f9-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="898f9-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="898f9-124">Anger namnet på den virtuella nätverksgateway som certifikatet har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="898f9-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="898f9-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="898f9-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="898f9-126">Anger namnet på det VPN-klientcertifikat som tas bort.</span><span class="sxs-lookup"><span data-stu-id="898f9-126">Specifies the name of the VPN client certificate being removed.</span></span>

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

### <span data-ttu-id="898f9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="898f9-127">CommonParameters</span></span>
<span data-ttu-id="898f9-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="898f9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="898f9-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="898f9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="898f9-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="898f9-130">INPUTS</span></span>

## <span data-ttu-id="898f9-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="898f9-131">OUTPUTS</span></span>

## <span data-ttu-id="898f9-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="898f9-132">NOTES</span></span>

## <span data-ttu-id="898f9-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="898f9-133">RELATED LINKS</span></span>

[<span data-ttu-id="898f9-134">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="898f9-134">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="898f9-135">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="898f9-135">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="898f9-136">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="898f9-136">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)


