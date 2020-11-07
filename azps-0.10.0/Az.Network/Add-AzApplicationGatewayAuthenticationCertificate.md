---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 6652da4491bc503ecc2d0c8ee016416cefbff172
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922470"
---
# <span data-ttu-id="47ac9-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="47ac9-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="47ac9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="47ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="47ac9-103">Lägger till ett autentiseringscertifikat i en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="47ac9-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="47ac9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="47ac9-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47ac9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="47ac9-105">DESCRIPTION</span></span>
<span data-ttu-id="47ac9-106">Cmdleten **Add-AzApplicationGatewayAuthenticationCertificate** lägger till ett autentiseringscertifikat i en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="47ac9-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="47ac9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="47ac9-107">EXAMPLES</span></span>

### <span data-ttu-id="47ac9-108">9.1</span><span class="sxs-lookup"><span data-stu-id="47ac9-108">1:</span></span>
```

```

## <span data-ttu-id="47ac9-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="47ac9-109">PARAMETERS</span></span>

### <span data-ttu-id="47ac9-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47ac9-110">-ApplicationGateway</span></span>
<span data-ttu-id="47ac9-111">Anger namnet på den Programgateway som denna cmdlet lägger till ett autentiseringscertifikat för.</span><span class="sxs-lookup"><span data-stu-id="47ac9-111">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="47ac9-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="47ac9-112">-CertificateFile</span></span>
<span data-ttu-id="47ac9-113">Anger sökvägen för det autentiseringscertifikat som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="47ac9-113">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="47ac9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47ac9-114">-DefaultProfile</span></span>
<span data-ttu-id="47ac9-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="47ac9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47ac9-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="47ac9-116">-Name</span></span>
<span data-ttu-id="47ac9-117">Anger namnet på ett certifikat som denna cmdlet lägger till i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="47ac9-117">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="47ac9-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="47ac9-118">-Confirm</span></span>
<span data-ttu-id="47ac9-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="47ac9-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47ac9-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47ac9-120">-WhatIf</span></span>
<span data-ttu-id="47ac9-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="47ac9-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47ac9-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="47ac9-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47ac9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47ac9-123">CommonParameters</span></span>
<span data-ttu-id="47ac9-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47ac9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47ac9-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47ac9-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47ac9-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="47ac9-126">INPUTS</span></span>

### <span data-ttu-id="47ac9-127">System. String</span><span class="sxs-lookup"><span data-stu-id="47ac9-127">System.String</span></span>

## <span data-ttu-id="47ac9-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="47ac9-128">OUTPUTS</span></span>

### <span data-ttu-id="47ac9-129">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47ac9-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="47ac9-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="47ac9-130">NOTES</span></span>
* <span data-ttu-id="47ac9-131">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="47ac9-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="47ac9-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="47ac9-132">RELATED LINKS</span></span>

[<span data-ttu-id="47ac9-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="47ac9-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="47ac9-134">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="47ac9-134">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="47ac9-135">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="47ac9-135">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="47ac9-136">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="47ac9-136">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


