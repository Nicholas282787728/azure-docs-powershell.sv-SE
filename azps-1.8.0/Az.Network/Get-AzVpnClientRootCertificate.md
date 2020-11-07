---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
ms.openlocfilehash: 847f1c06975e9bef570c5ab3fdaf5f6f3e4a99d6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748173"
---
# <span data-ttu-id="7b762-101">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7b762-101">Get-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="7b762-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7b762-102">SYNOPSIS</span></span>
<span data-ttu-id="7b762-103">Hämtar information om VPN-rotcertifikat.</span><span class="sxs-lookup"><span data-stu-id="7b762-103">Gets information about VPN root certificates.</span></span>

## <span data-ttu-id="7b762-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7b762-104">SYNTAX</span></span>

```
Get-AzVpnClientRootCertificate [-VpnClientRootCertificateName <String>] -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b762-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7b762-105">DESCRIPTION</span></span>
<span data-ttu-id="7b762-106">Cmdleten **Get-AzVpnClientRootCertificate** returnerar information om rot certifikaten som har kopplats till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="7b762-106">The **Get-AzVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="7b762-107">Rot certifikat är 509 certifikat som identifierar rot certifikat utfärdaren: alla andra certifikat som används på gatewayen har rot certifikatet.</span><span class="sxs-lookup"><span data-stu-id="7b762-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="7b762-108">Som standard returnerar **Get-AzVpnClientRootCertificate** information om alla rot certifikat som har kopplats till en gateway.</span><span class="sxs-lookup"><span data-stu-id="7b762-108">By default, **Get-AzVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="7b762-109">(Gateways kan ha mer än ett rot certifikat.) Genom att inkludera **VpnClientRootCertificateName** -parametern kan du emellertid begränsa den returnerade informationen till ett visst certifikat.</span><span class="sxs-lookup"><span data-stu-id="7b762-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="7b762-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7b762-110">EXAMPLES</span></span>

### <span data-ttu-id="7b762-111">Exempel 1: få information om alla rot certifikat</span><span class="sxs-lookup"><span data-stu-id="7b762-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="7b762-112">Det här kommandot får information om alla rot certifikat som tilldelats en virtuell nätverksgateway som heter ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="7b762-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="7b762-113">Exempel 2: få information om specifika rot certifikat</span><span class="sxs-lookup"><span data-stu-id="7b762-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="7b762-114">Det här kommandot är en variant av kommandot som visas i exempel 1.</span><span class="sxs-lookup"><span data-stu-id="7b762-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="7b762-115">I det här fallet är parametern *VpnClientRootCertificateName* inkluderad för att begränsa vilka data som returneras till ett visst rot certifikat: ContosoRootClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="7b762-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="7b762-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7b762-116">PARAMETERS</span></span>

### <span data-ttu-id="7b762-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b762-117">-DefaultProfile</span></span>
<span data-ttu-id="7b762-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7b762-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b762-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b762-119">-ResourceGroupName</span></span>
<span data-ttu-id="7b762-120">Anger namnet på den resurs grupp som den virtuella Nätverksgatewayen är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="7b762-120">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="7b762-121">Resurs grupper kategoriserar artiklar för att förenkla lager hantering och allmän Azure-administration.</span><span class="sxs-lookup"><span data-stu-id="7b762-121">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="7b762-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="7b762-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="7b762-123">Anger namnet på den virtuella nätverksgateway där rot certifikatet har tilldelats.</span><span class="sxs-lookup"><span data-stu-id="7b762-123">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

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

### <span data-ttu-id="7b762-124">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="7b762-124">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="7b762-125">Anger namnet på klient rot certifikatet som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="7b762-125">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7b762-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b762-126">CommonParameters</span></span>
<span data-ttu-id="7b762-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b762-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b762-128">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b762-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b762-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7b762-129">INPUTS</span></span>

### <span data-ttu-id="7b762-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7b762-130">System.String</span></span>

## <span data-ttu-id="7b762-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7b762-131">OUTPUTS</span></span>

### <span data-ttu-id="7b762-132">Microsoft. Azure. commands. Networks. Models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7b762-132">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="7b762-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7b762-133">NOTES</span></span>

## <span data-ttu-id="7b762-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7b762-134">RELATED LINKS</span></span>

[<span data-ttu-id="7b762-135">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7b762-135">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="7b762-136">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7b762-136">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="7b762-137">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7b762-137">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)

