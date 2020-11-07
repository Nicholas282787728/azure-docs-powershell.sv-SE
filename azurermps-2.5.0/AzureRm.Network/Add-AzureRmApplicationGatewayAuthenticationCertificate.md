---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 4d664018592f05203c684a896f0a0701940301a6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930221"
---
# <span data-ttu-id="fc1ec-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fc1ec-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="fc1ec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc1ec-102">SYNOPSIS</span></span>
<span data-ttu-id="fc1ec-103">Lägger till ett autentiseringscertifikat i en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="fc1ec-103">Adds an authentication certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc1ec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc1ec-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc1ec-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc1ec-105">DESCRIPTION</span></span>
<span data-ttu-id="fc1ec-106">Cmdleten **Add-AzureRmApplicationGatewayAuthenticationCertificate** lägger till ett autentiseringscertifikat i en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="fc1ec-106">The **Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="fc1ec-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc1ec-107">EXAMPLES</span></span>

### <span data-ttu-id="fc1ec-108">9.1</span><span class="sxs-lookup"><span data-stu-id="fc1ec-108">1:</span></span>
```

```

## <span data-ttu-id="fc1ec-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc1ec-109">PARAMETERS</span></span>

### <span data-ttu-id="fc1ec-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc1ec-110">-ApplicationGateway</span></span>
<span data-ttu-id="fc1ec-111">Anger namnet på den Programgateway som denna cmdlet lägger till ett autentiseringscertifikat för.</span><span class="sxs-lookup"><span data-stu-id="fc1ec-111">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="fc1ec-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="fc1ec-112">-CertificateFile</span></span>
<span data-ttu-id="fc1ec-113">Anger sökvägen för det autentiseringscertifikat som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="fc1ec-113">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="fc1ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc1ec-114">-DefaultProfile</span></span>
<span data-ttu-id="fc1ec-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fc1ec-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc1ec-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="fc1ec-116">-Name</span></span>
<span data-ttu-id="fc1ec-117">Anger namnet på ett certifikat som denna cmdlet lägger till i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="fc1ec-117">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="fc1ec-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fc1ec-118">-Confirm</span></span>
<span data-ttu-id="fc1ec-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fc1ec-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc1ec-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc1ec-120">-WhatIf</span></span>
<span data-ttu-id="fc1ec-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fc1ec-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc1ec-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fc1ec-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc1ec-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc1ec-123">CommonParameters</span></span>
<span data-ttu-id="fc1ec-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc1ec-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc1ec-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc1ec-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc1ec-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc1ec-126">INPUTS</span></span>

### <span data-ttu-id="fc1ec-127">System. String</span><span class="sxs-lookup"><span data-stu-id="fc1ec-127">System.String</span></span>

## <span data-ttu-id="fc1ec-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc1ec-128">OUTPUTS</span></span>

### <span data-ttu-id="fc1ec-129">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc1ec-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fc1ec-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc1ec-130">NOTES</span></span>
* <span data-ttu-id="fc1ec-131">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="fc1ec-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="fc1ec-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc1ec-132">RELATED LINKS</span></span>

[<span data-ttu-id="fc1ec-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fc1ec-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="fc1ec-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fc1ec-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="fc1ec-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fc1ec-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="fc1ec-136">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fc1ec-136">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


