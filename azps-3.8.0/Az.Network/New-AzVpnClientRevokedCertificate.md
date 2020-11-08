---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: ba9715b6f29cd45ba25f8b2d2ab85ba0d7ef7979
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090940"
---
# <span data-ttu-id="31546-101">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="31546-101">New-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="31546-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="31546-102">SYNOPSIS</span></span>
<span data-ttu-id="31546-103">Skapar en ny VPN-klient-åter kallelse intyg.</span><span class="sxs-lookup"><span data-stu-id="31546-103">Creates a new VPN client-revocation certificate.</span></span>

## <span data-ttu-id="31546-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="31546-104">SYNTAX</span></span>

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31546-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="31546-105">DESCRIPTION</span></span>
<span data-ttu-id="31546-106">Cmdleten **New-AzVpnClientRevokedCertificate** skapar ett nytt virtuellt privat nätverk (VPN)-certifikat för åter kallelse för användning på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="31546-106">The **New-AzVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="31546-107">Certifikat för klient åter kallelse gör att klient datorer inte använder det angivna certifikatet för att verifiera.</span><span class="sxs-lookup"><span data-stu-id="31546-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="31546-108">Denna cmdlet skapar ett fristående certifikat som inte är kopplat till en virtuell gateway.</span><span class="sxs-lookup"><span data-stu-id="31546-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="31546-109">I stället används certifikatet som skapas av **New-AzVpnClientRevokedCertificate** tillsammans med New-AzVirtualNetworkGateway cmdlet när en ny Gateway skapas.</span><span class="sxs-lookup"><span data-stu-id="31546-109">Instead, the certificate created by **New-AzVpnClientRevokedCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="31546-110">Antag till exempel att du skapar ett nytt certifikat och lagrar det i en variabel som heter $Certificate.</span><span class="sxs-lookup"><span data-stu-id="31546-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="31546-111">Du kan sedan använda detta certifikat objekt när du skapar en ny virtuell gateway.</span><span class="sxs-lookup"><span data-stu-id="31546-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="31546-112">Till exempel: `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="31546-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span></span>
<span data-ttu-id="31546-113">Mer information finns i dokumentationen för New-AzVirtualNetworkGateway-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="31546-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="31546-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="31546-114">EXAMPLES</span></span>

### <span data-ttu-id="31546-115">Exempel 1: skapa ett nytt klient-återkallat certifikat</span><span class="sxs-lookup"><span data-stu-id="31546-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="31546-116">Det här kommandot skapar ett nytt klient-återkallat certifikat och lagrar certifikat-objektet i en variabel som heter $Certificate.</span><span class="sxs-lookup"><span data-stu-id="31546-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="31546-117">Denna variabel kan sedan användas av **New-AzVirtualNetworkGateway-** cmdleten för att lägga till certifikatet till en ny virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="31546-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="31546-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="31546-118">PARAMETERS</span></span>

### <span data-ttu-id="31546-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31546-119">-DefaultProfile</span></span>
<span data-ttu-id="31546-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="31546-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31546-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="31546-121">-Name</span></span>
<span data-ttu-id="31546-122">Anger ett unikt namn för det nya klient certifikat för åter kallelse.</span><span class="sxs-lookup"><span data-stu-id="31546-122">Specifies a unique name for the new client-revocation certificate.</span></span>

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

### <span data-ttu-id="31546-123">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="31546-123">-Thumbprint</span></span>
<span data-ttu-id="31546-124">Anger unikt ID för det certifikat som läggs till.</span><span class="sxs-lookup"><span data-stu-id="31546-124">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="31546-125">Du kan returnera tumavtryck för dina certifikat genom att använda ett Windows PowerShell-kommando som liknar det här: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span><span class="sxs-lookup"><span data-stu-id="31546-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span></span>
<span data-ttu-id="31546-126">Föregående kommando returnerar information för alla lokala dator certifikat i rot certifikat arkivet.</span><span class="sxs-lookup"><span data-stu-id="31546-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="31546-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31546-127">CommonParameters</span></span>
<span data-ttu-id="31546-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31546-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31546-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31546-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31546-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="31546-130">INPUTS</span></span>

### <span data-ttu-id="31546-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="31546-131">None</span></span>

## <span data-ttu-id="31546-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="31546-132">OUTPUTS</span></span>

### <span data-ttu-id="31546-133">Microsoft. Azure. commands. Networks. Models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="31546-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="31546-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="31546-134">NOTES</span></span>

## <span data-ttu-id="31546-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="31546-135">RELATED LINKS</span></span>

[<span data-ttu-id="31546-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="31546-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="31546-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="31546-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="31546-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="31546-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


