---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 5af778b84981b5b15acaa688bd8ad1702e5ab7e3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390928"
---
# <span data-ttu-id="583b0-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="583b0-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="583b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="583b0-102">SYNOPSIS</span></span>
<span data-ttu-id="583b0-103">Uppdaterar ett autentiseringscertifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="583b0-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="583b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="583b0-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="583b0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="583b0-105">DESCRIPTION</span></span>
<span data-ttu-id="583b0-106">Cmdleten **set-AzApplicationGatewayAuthenticationCertificate** uppdaterar ett autentiseringscertifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="583b0-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="583b0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="583b0-107">EXAMPLES</span></span>

### <span data-ttu-id="583b0-108">Exempel 1: uppdatera ett autentiseringscertifikat</span><span class="sxs-lookup"><span data-stu-id="583b0-108">Example 1: Update an authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert2.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="583b0-109">Med det första kommandot får programgatewayen namnet appGwName och lagras resultatet i $appgw variabel.</span><span class="sxs-lookup"><span data-stu-id="583b0-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="583b0-110">Det andra kommandot uppdaterar autentiseringscertifikatet med namnet cert01 i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="583b0-110">The second command updates the authentication certificate named cert01 in the application gateway.</span></span>
<span data-ttu-id="583b0-111">Det tredje kommandot uppdaterar programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="583b0-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="583b0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="583b0-112">PARAMETERS</span></span>

### <span data-ttu-id="583b0-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="583b0-113">-ApplicationGateway</span></span>
<span data-ttu-id="583b0-114">Anger namnet på den Programgateway för vilken denna cmdlet uppdaterar ett autentiseringscertifikat.</span><span class="sxs-lookup"><span data-stu-id="583b0-114">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="583b0-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="583b0-115">-CertificateFile</span></span>
<span data-ttu-id="583b0-116">Anger sökvägen till den fil för meddelandeautentisering med vilken denna cmdlet uppdaterar certifikatet.</span><span class="sxs-lookup"><span data-stu-id="583b0-116">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="583b0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="583b0-117">-DefaultProfile</span></span>
<span data-ttu-id="583b0-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="583b0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="583b0-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="583b0-119">-Name</span></span>
<span data-ttu-id="583b0-120">Anger namnet på det autentiseringscertifikat som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="583b0-120">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="583b0-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="583b0-121">-Confirm</span></span>
<span data-ttu-id="583b0-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="583b0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="583b0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="583b0-123">-WhatIf</span></span>
<span data-ttu-id="583b0-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="583b0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="583b0-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="583b0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="583b0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="583b0-126">CommonParameters</span></span>
<span data-ttu-id="583b0-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="583b0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="583b0-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="583b0-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="583b0-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="583b0-129">INPUTS</span></span>

### <span data-ttu-id="583b0-130">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="583b0-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="583b0-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="583b0-131">OUTPUTS</span></span>

### <span data-ttu-id="583b0-132">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="583b0-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="583b0-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="583b0-133">NOTES</span></span>
* <span data-ttu-id="583b0-134">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="583b0-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="583b0-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="583b0-135">RELATED LINKS</span></span>

[<span data-ttu-id="583b0-136">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="583b0-136">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="583b0-137">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="583b0-137">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="583b0-138">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="583b0-138">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="583b0-139">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="583b0-139">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)


