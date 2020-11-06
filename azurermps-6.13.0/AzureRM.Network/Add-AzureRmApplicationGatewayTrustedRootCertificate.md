---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: e44136d5fa9b0a6b0b979005c13faf6041d98f61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582619"
---
# <span data-ttu-id="a014b-101">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a014b-101">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="a014b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a014b-102">SYNOPSIS</span></span>
<span data-ttu-id="a014b-103">Lägger till ett betrott rot certifikat till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="a014b-103">Adds a trusted root certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a014b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a014b-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a014b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a014b-105">DESCRIPTION</span></span>
<span data-ttu-id="a014b-106">Cmdleten **Add-AzureRmApplicationGatewayTrustedRootCertificate** lägger till ett betrott rot certifikat till en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a014b-106">The **Add-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="a014b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a014b-107">EXAMPLES</span></span>

### <span data-ttu-id="a014b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a014b-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzureRmApplicationGatewayBackendHttpSetting -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="a014b-109">Med det första kommandot hämtas programgatewayen och lagras i $gw variabel.</span><span class="sxs-lookup"><span data-stu-id="a014b-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="a014b-110">Det andra kommandot Addes ett nytt betrott rot certifikat till Application Gateway med sökvägen till rot certifikatet som indata.</span><span class="sxs-lookup"><span data-stu-id="a014b-110">The second command addes a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="a014b-111">Det tredje kommandot skapar en ny server dels-http-inställning med ett betrott rot certifikat för verifiering av backend server-certifikatet mot.</span><span class="sxs-lookup"><span data-stu-id="a014b-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="a014b-112">Fouth-kommandot uppdaterar programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="a014b-112">The fouth command updates the Application Gateway.</span></span>

## <span data-ttu-id="a014b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a014b-113">PARAMETERS</span></span>

### <span data-ttu-id="a014b-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a014b-114">-ApplicationGateway</span></span>
<span data-ttu-id="a014b-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a014b-115">The applicationGateway</span></span>

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

### <span data-ttu-id="a014b-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="a014b-116">-CertificateFile</span></span>
<span data-ttu-id="a014b-117">Sökväg till certifikat-CER-fil</span><span class="sxs-lookup"><span data-stu-id="a014b-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="a014b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a014b-118">-DefaultProfile</span></span>
<span data-ttu-id="a014b-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a014b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a014b-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="a014b-120">-Name</span></span>
<span data-ttu-id="a014b-121">Namnet på TrustedRoot-certifikatet</span><span class="sxs-lookup"><span data-stu-id="a014b-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="a014b-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a014b-122">-Confirm</span></span>
<span data-ttu-id="a014b-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a014b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a014b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a014b-124">-WhatIf</span></span>
<span data-ttu-id="a014b-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a014b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a014b-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a014b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a014b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a014b-127">CommonParameters</span></span>
<span data-ttu-id="a014b-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a014b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a014b-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a014b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a014b-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a014b-130">INPUTS</span></span>

### <span data-ttu-id="a014b-131">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a014b-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a014b-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a014b-132">OUTPUTS</span></span>

### <span data-ttu-id="a014b-133">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a014b-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a014b-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a014b-134">NOTES</span></span>

## <span data-ttu-id="a014b-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a014b-135">RELATED LINKS</span></span>
