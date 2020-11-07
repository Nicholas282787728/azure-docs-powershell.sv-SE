---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 3c70fcd0e04b566ff1cd3297525d3ed2c9ed95ba
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931161"
---
# <span data-ttu-id="a817d-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a817d-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="a817d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a817d-102">SYNOPSIS</span></span>
<span data-ttu-id="a817d-103">Uppdaterar ett autentiseringscertifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="a817d-103">Updates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a817d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a817d-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a817d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a817d-105">DESCRIPTION</span></span>
<span data-ttu-id="a817d-106">Cmdleten **set-AzureRmApplicationGatewayAuthenticationCertificate** uppdaterar ett autentiseringscertifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a817d-106">The **Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="a817d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a817d-107">EXAMPLES</span></span>

### <span data-ttu-id="a817d-108">9.1</span><span class="sxs-lookup"><span data-stu-id="a817d-108">1:</span></span>
```

```

## <span data-ttu-id="a817d-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a817d-109">PARAMETERS</span></span>

### <span data-ttu-id="a817d-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a817d-110">-ApplicationGateway</span></span>
<span data-ttu-id="a817d-111">Anger namnet på den Programgateway för vilken denna cmdlet uppdaterar ett autentiseringscertifikat.</span><span class="sxs-lookup"><span data-stu-id="a817d-111">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a817d-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="a817d-112">-CertificateFile</span></span>
<span data-ttu-id="a817d-113">Anger sökvägen till den fil för meddelandeautentisering med vilken denna cmdlet uppdaterar certifikatet.</span><span class="sxs-lookup"><span data-stu-id="a817d-113">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="a817d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a817d-114">-DefaultProfile</span></span>
<span data-ttu-id="a817d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a817d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a817d-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="a817d-116">-Name</span></span>
<span data-ttu-id="a817d-117">Anger namnet på det autentiseringscertifikat som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="a817d-117">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="a817d-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a817d-118">-Confirm</span></span>
<span data-ttu-id="a817d-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a817d-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a817d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a817d-120">-WhatIf</span></span>
<span data-ttu-id="a817d-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a817d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a817d-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a817d-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a817d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a817d-123">CommonParameters</span></span>
<span data-ttu-id="a817d-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a817d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a817d-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a817d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a817d-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a817d-126">INPUTS</span></span>

### <span data-ttu-id="a817d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a817d-127">System.String</span></span>

## <span data-ttu-id="a817d-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a817d-128">OUTPUTS</span></span>

### <span data-ttu-id="a817d-129">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a817d-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a817d-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a817d-130">NOTES</span></span>
* <span data-ttu-id="a817d-131">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="a817d-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="a817d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a817d-132">RELATED LINKS</span></span>

[<span data-ttu-id="a817d-133">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a817d-133">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="a817d-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a817d-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="a817d-135">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a817d-135">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="a817d-136">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a817d-136">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)


