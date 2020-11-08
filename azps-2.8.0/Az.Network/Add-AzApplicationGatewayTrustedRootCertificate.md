---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: c8db96e9758e04a96f3f7b28c9fda9d8ac73a47e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918846"
---
# <span data-ttu-id="f6385-101">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f6385-101">Add-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="f6385-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6385-102">SYNOPSIS</span></span>
<span data-ttu-id="f6385-103">Lägger till ett betrott rot certifikat till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="f6385-103">Adds a trusted root certificate to an application gateway.</span></span>

## <span data-ttu-id="f6385-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6385-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6385-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6385-105">DESCRIPTION</span></span>
<span data-ttu-id="f6385-106">Cmdleten **Add-AzApplicationGatewayTrustedRootCertificate** lägger till ett betrott rot certifikat till en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f6385-106">The **Add-AzApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="f6385-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6385-107">EXAMPLES</span></span>

### <span data-ttu-id="f6385-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f6385-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName -CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $gw -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="f6385-109">Med det första kommandot hämtas programgatewayen och lagras i $gw variabel.</span><span class="sxs-lookup"><span data-stu-id="f6385-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="f6385-110">Det andra kommandot lägger till ett nytt betrott rot certifikat till Application Gateway och kopplar sökvägen till rot certifikatet som indata.</span><span class="sxs-lookup"><span data-stu-id="f6385-110">The second command adds a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="f6385-111">Det tredje kommandot skapar en ny server dels-http-inställning med ett betrott rot certifikat för verifiering av backend server-certifikatet mot.</span><span class="sxs-lookup"><span data-stu-id="f6385-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="f6385-112">Det fjärde kommandot uppdaterar programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="f6385-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="f6385-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6385-113">PARAMETERS</span></span>

### <span data-ttu-id="f6385-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6385-114">-ApplicationGateway</span></span>
<span data-ttu-id="f6385-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6385-115">The applicationGateway</span></span>

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

### <span data-ttu-id="f6385-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f6385-116">-CertificateFile</span></span>
<span data-ttu-id="f6385-117">Sökväg till certifikat-CER-fil</span><span class="sxs-lookup"><span data-stu-id="f6385-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="f6385-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6385-118">-DefaultProfile</span></span>
<span data-ttu-id="f6385-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f6385-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6385-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="f6385-120">-Name</span></span>
<span data-ttu-id="f6385-121">Namnet på TrustedRoot-certifikatet</span><span class="sxs-lookup"><span data-stu-id="f6385-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="f6385-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f6385-122">-Confirm</span></span>
<span data-ttu-id="f6385-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f6385-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6385-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6385-124">-WhatIf</span></span>
<span data-ttu-id="f6385-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f6385-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6385-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f6385-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6385-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6385-127">CommonParameters</span></span>
<span data-ttu-id="f6385-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6385-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6385-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6385-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6385-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6385-130">INPUTS</span></span>

### <span data-ttu-id="f6385-131">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6385-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f6385-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6385-132">OUTPUTS</span></span>

### <span data-ttu-id="f6385-133">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6385-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f6385-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6385-134">NOTES</span></span>

## <span data-ttu-id="f6385-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6385-135">RELATED LINKS</span></span>

[<span data-ttu-id="f6385-136">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f6385-136">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f6385-137">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f6385-137">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f6385-138">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f6385-138">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f6385-139">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f6385-139">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)