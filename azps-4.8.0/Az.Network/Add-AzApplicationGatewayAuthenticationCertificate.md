---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 687752d74e13030cd954736132dba845c2c55127
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102763"
---
# <span data-ttu-id="5f402-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5f402-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="5f402-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f402-102">SYNOPSIS</span></span>
<span data-ttu-id="5f402-103">Lägger till ett autentiseringscertifikat i en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="5f402-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="5f402-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f402-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f402-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f402-105">DESCRIPTION</span></span>
<span data-ttu-id="5f402-106">Cmdleten **Add-AzApplicationGatewayAuthenticationCertificate** lägger till ett autentiseringscertifikat i en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="5f402-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="5f402-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f402-107">EXAMPLES</span></span>

### <span data-ttu-id="5f402-108">Exempel 1: lägga till autentiseringscertifikat i en Programgateway</span><span class="sxs-lookup"><span data-stu-id="5f402-108">Example 1: Add authentication certificate to an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="5f402-109">Det första kommandot får en Programgateway som heter appGwName och lagrar den i $appgw variabel.</span><span class="sxs-lookup"><span data-stu-id="5f402-109">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="5f402-110">Det andra kommandot lägger till autentiseringscertifikatet med namnet cert01 i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="5f402-110">The second command adds authentication certificate named cert01 to the application gateway.</span></span>
<span data-ttu-id="5f402-111">Det tredje kommandot uppdaterar programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="5f402-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="5f402-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f402-112">PARAMETERS</span></span>

### <span data-ttu-id="5f402-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5f402-113">-ApplicationGateway</span></span>
<span data-ttu-id="5f402-114">Anger namnet på den Programgateway som denna cmdlet lägger till ett autentiseringscertifikat för.</span><span class="sxs-lookup"><span data-stu-id="5f402-114">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="5f402-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="5f402-115">-CertificateFile</span></span>
<span data-ttu-id="5f402-116">Anger sökvägen för det autentiseringscertifikat som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="5f402-116">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="5f402-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f402-117">-DefaultProfile</span></span>
<span data-ttu-id="5f402-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5f402-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f402-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="5f402-119">-Name</span></span>
<span data-ttu-id="5f402-120">Anger namnet på ett certifikat som denna cmdlet lägger till i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="5f402-120">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="5f402-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5f402-121">-Confirm</span></span>
<span data-ttu-id="5f402-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5f402-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f402-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f402-123">-WhatIf</span></span>
<span data-ttu-id="5f402-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5f402-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f402-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5f402-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f402-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f402-126">CommonParameters</span></span>
<span data-ttu-id="5f402-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f402-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f402-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f402-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f402-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f402-129">INPUTS</span></span>

### <span data-ttu-id="5f402-130">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5f402-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5f402-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f402-131">OUTPUTS</span></span>

### <span data-ttu-id="5f402-132">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5f402-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5f402-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f402-133">NOTES</span></span>
* <span data-ttu-id="5f402-134">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="5f402-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="5f402-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f402-135">RELATED LINKS</span></span>

[<span data-ttu-id="5f402-136">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5f402-136">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5f402-137">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5f402-137">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5f402-138">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5f402-138">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5f402-139">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5f402-139">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


