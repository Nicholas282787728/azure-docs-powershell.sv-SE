---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 9ad926a9dd9a3a13bff1f31cfa1ae7d689cadbb7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753956"
---
# <span data-ttu-id="71268-101">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="71268-101">Add-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="71268-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="71268-102">SYNOPSIS</span></span>
<span data-ttu-id="71268-103">Lägger till ett betrott rot certifikat till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="71268-103">Adds a trusted root certificate to an application gateway.</span></span>

## <span data-ttu-id="71268-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="71268-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71268-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="71268-105">DESCRIPTION</span></span>
<span data-ttu-id="71268-106">Cmdleten **Add-AzApplicationGatewayTrustedRootCertificate** lägger till ett betrott rot certifikat till en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="71268-106">The **Add-AzApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="71268-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="71268-107">EXAMPLES</span></span>

### <span data-ttu-id="71268-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="71268-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName -CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $gw -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="71268-109">Med det första kommandot hämtas programgatewayen och lagras i $gw variabel.</span><span class="sxs-lookup"><span data-stu-id="71268-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="71268-110">Det andra kommandot Addes ett nytt betrott rot certifikat till Application Gateway med sökvägen till rot certifikatet som indata.</span><span class="sxs-lookup"><span data-stu-id="71268-110">The second command addes a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="71268-111">Det tredje kommandot skapar en ny server dels-http-inställning med ett betrott rot certifikat för verifiering av backend server-certifikatet mot.</span><span class="sxs-lookup"><span data-stu-id="71268-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="71268-112">Fouth-kommandot uppdaterar programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="71268-112">The fouth command updates the Application Gateway.</span></span>

## <span data-ttu-id="71268-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="71268-113">PARAMETERS</span></span>

### <span data-ttu-id="71268-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="71268-114">-ApplicationGateway</span></span>
<span data-ttu-id="71268-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="71268-115">The applicationGateway</span></span>

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

### <span data-ttu-id="71268-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="71268-116">-CertificateFile</span></span>
<span data-ttu-id="71268-117">Sökväg till certifikat-CER-fil</span><span class="sxs-lookup"><span data-stu-id="71268-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="71268-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71268-118">-DefaultProfile</span></span>
<span data-ttu-id="71268-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="71268-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71268-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="71268-120">-Name</span></span>
<span data-ttu-id="71268-121">Namnet på TrustedRoot-certifikatet</span><span class="sxs-lookup"><span data-stu-id="71268-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="71268-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="71268-122">-Confirm</span></span>
<span data-ttu-id="71268-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="71268-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71268-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71268-124">-WhatIf</span></span>
<span data-ttu-id="71268-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="71268-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71268-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="71268-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71268-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71268-127">CommonParameters</span></span>
<span data-ttu-id="71268-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71268-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71268-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71268-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71268-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="71268-130">INPUTS</span></span>

### <span data-ttu-id="71268-131">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="71268-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="71268-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="71268-132">OUTPUTS</span></span>

### <span data-ttu-id="71268-133">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="71268-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="71268-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="71268-134">NOTES</span></span>

## <span data-ttu-id="71268-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="71268-135">RELATED LINKS</span></span>

[<span data-ttu-id="71268-136">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="71268-136">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="71268-137">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="71268-137">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="71268-138">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="71268-138">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="71268-139">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="71268-139">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
