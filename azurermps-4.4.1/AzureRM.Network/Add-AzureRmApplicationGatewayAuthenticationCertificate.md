---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 271eaf702165c3c1e80243efa080b3e4d981390d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580571"
---
# <span data-ttu-id="4c9bc-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4c9bc-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="4c9bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4c9bc-102">SYNOPSIS</span></span>
<span data-ttu-id="4c9bc-103">Lägger till ett autentiseringscertifikat i en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="4c9bc-103">Adds an authentication certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c9bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4c9bc-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c9bc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4c9bc-105">DESCRIPTION</span></span>
<span data-ttu-id="4c9bc-106">Cmdleten **Add-AzureRmApplicationGatewayAuthenticationCertificate** lägger till ett autentiseringscertifikat i en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4c9bc-106">The **Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="4c9bc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4c9bc-107">EXAMPLES</span></span>

## <span data-ttu-id="4c9bc-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4c9bc-108">PARAMETERS</span></span>

### <span data-ttu-id="4c9bc-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c9bc-109">-ApplicationGateway</span></span>
<span data-ttu-id="4c9bc-110">Anger namnet på den Programgateway som denna cmdlet lägger till ett autentiseringscertifikat för.</span><span class="sxs-lookup"><span data-stu-id="4c9bc-110">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c9bc-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="4c9bc-111">-CertificateFile</span></span>
<span data-ttu-id="4c9bc-112">Anger sökvägen för det autentiseringscertifikat som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="4c9bc-112">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="4c9bc-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="4c9bc-113">-Name</span></span>
<span data-ttu-id="4c9bc-114">Anger namnet på ett certifikat som denna cmdlet lägger till i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="4c9bc-114">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="4c9bc-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4c9bc-115">-Confirm</span></span>
<span data-ttu-id="4c9bc-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4c9bc-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c9bc-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c9bc-117">-WhatIf</span></span>
<span data-ttu-id="4c9bc-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4c9bc-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c9bc-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4c9bc-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c9bc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c9bc-120">-DefaultProfile</span></span>
<span data-ttu-id="4c9bc-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4c9bc-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c9bc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c9bc-122">CommonParameters</span></span>
<span data-ttu-id="4c9bc-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c9bc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c9bc-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c9bc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c9bc-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4c9bc-125">INPUTS</span></span>

### <span data-ttu-id="4c9bc-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4c9bc-126">System.String</span></span>

## <span data-ttu-id="4c9bc-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4c9bc-127">OUTPUTS</span></span>

### <span data-ttu-id="4c9bc-128">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c9bc-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4c9bc-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4c9bc-129">NOTES</span></span>
* <span data-ttu-id="4c9bc-130">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="4c9bc-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4c9bc-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4c9bc-131">RELATED LINKS</span></span>

[<span data-ttu-id="4c9bc-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4c9bc-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="4c9bc-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4c9bc-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="4c9bc-134">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4c9bc-134">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="4c9bc-135">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4c9bc-135">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


