---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: e3a92085c15116527e1b6c14d5403f68748f4f90
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422328"
---
# <span data-ttu-id="b9ca6-101">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b9ca6-101">Add-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="b9ca6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b9ca6-102">SYNOPSIS</span></span>
<span data-ttu-id="b9ca6-103">Lägger till en kedja med betrodda klient certifikat utfärdare till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="b9ca6-103">Adds a trusted client CA certificate chain to an application gateway.</span></span>

## <span data-ttu-id="b9ca6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b9ca6-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9ca6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b9ca6-105">DESCRIPTION</span></span>
<span data-ttu-id="b9ca6-106">Cmdleten **Add-AzApplicationGatewayTrustedClientCertificate** lägger till en betrodd klient certifikat utfärdares certifikat kedja till en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="b9ca6-106">The **Add-AzApplicationGatewayTrustedClientCertificate** cmdlet adds a trusted client CA certificate chain to an Azure application gateway.</span></span>

## <span data-ttu-id="b9ca6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b9ca6-107">EXAMPLES</span></span>

### <span data-ttu-id="b9ca6-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b9ca6-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfileName -ApplicationGateway $gw -TrustedClientCertificates $trustedClient
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="b9ca6-109">Med det första kommandot hämtas programgatewayen och lagras i $gw variabel.</span><span class="sxs-lookup"><span data-stu-id="b9ca6-109">The first command gets the application gateway and stores it in $gw variable.</span></span> <span data-ttu-id="b9ca6-110">Det andra kommandot skapar en ny kedja av certifikat certifikat utfärdare som tar vägen till klient certifikat utfärdarens certifikat som indata.</span><span class="sxs-lookup"><span data-stu-id="b9ca6-110">The second command creates a new trusted client CA certificate chain taking path of the client CA certificate as input.</span></span> <span data-ttu-id="b9ca6-111">Det tredje kommandot skapar en SSL-profil med certifikat för betrodda klienter.</span><span class="sxs-lookup"><span data-stu-id="b9ca6-111">The third command creates a SSL profile using trusted client certificate.</span></span> <span data-ttu-id="b9ca6-112">Det fjärde kommandot uppdaterar programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="b9ca6-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="b9ca6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b9ca6-113">PARAMETERS</span></span>

### <span data-ttu-id="b9ca6-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9ca6-114">-ApplicationGateway</span></span>
<span data-ttu-id="b9ca6-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9ca6-115">The applicationGateway</span></span>

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

### <span data-ttu-id="b9ca6-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b9ca6-116">-CertificateFile</span></span>
<span data-ttu-id="b9ca6-117">Sökväg till den betrodda klient certifikat utfärdarens certifikats kedja</span><span class="sxs-lookup"><span data-stu-id="b9ca6-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="b9ca6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9ca6-118">-DefaultProfile</span></span>
<span data-ttu-id="b9ca6-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ca6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ca6-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="b9ca6-120">-Name</span></span>
<span data-ttu-id="b9ca6-121">Namnet på den betrodda klient certifikat utfärdarens certifikat kedja</span><span class="sxs-lookup"><span data-stu-id="b9ca6-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="b9ca6-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b9ca6-122">-Confirm</span></span>
<span data-ttu-id="b9ca6-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b9ca6-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ca6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9ca6-124">-WhatIf</span></span>
<span data-ttu-id="b9ca6-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b9ca6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9ca6-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b9ca6-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ca6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9ca6-127">CommonParameters</span></span>
<span data-ttu-id="b9ca6-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9ca6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9ca6-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9ca6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9ca6-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b9ca6-130">INPUTS</span></span>

### <span data-ttu-id="b9ca6-131">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9ca6-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9ca6-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b9ca6-132">OUTPUTS</span></span>

### <span data-ttu-id="b9ca6-133">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9ca6-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9ca6-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b9ca6-134">NOTES</span></span>

## <span data-ttu-id="b9ca6-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b9ca6-135">RELATED LINKS</span></span>

[<span data-ttu-id="b9ca6-136">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b9ca6-136">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="b9ca6-137">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b9ca6-137">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="b9ca6-138">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b9ca6-138">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="b9ca6-139">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b9ca6-139">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)