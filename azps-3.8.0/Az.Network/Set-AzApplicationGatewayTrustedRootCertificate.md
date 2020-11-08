---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 746bbc2ec606bff74a49130e356bd531a3f63f8c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088628"
---
# <span data-ttu-id="cb864-101">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cb864-101">Set-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="cb864-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb864-102">SYNOPSIS</span></span>
<span data-ttu-id="cb864-103">Uppdaterar ett betrott rot certifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="cb864-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

## <span data-ttu-id="cb864-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb864-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb864-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb864-105">DESCRIPTION</span></span>
<span data-ttu-id="cb864-106">Cmdleten **set-AzApplicationGatewayTrustedRootCertificate** ändrar det befintliga betrodda rot certifikatet för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="cb864-106">The **Set-AzApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="cb864-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb864-107">EXAMPLES</span></span>

### <span data-ttu-id="cb864-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cb864-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="cb864-109">Ovan visas exempel på hur du uppdaterar ett befintligt betrott rot certifikat när ett rot certifikat är uppkopplat.</span><span class="sxs-lookup"><span data-stu-id="cb864-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="cb864-110">Det första kommandot får en Programgateway och lagrar den i $gw variabeln.</span><span class="sxs-lookup"><span data-stu-id="cb864-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="cb864-111">Det andra kommandot ändrar det befintliga betrodda rot certifikatet med ett nytt rot certifikat.</span><span class="sxs-lookup"><span data-stu-id="cb864-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="cb864-112">Det tredje kommandot uppdaterar programgatewayen på Azure.</span><span class="sxs-lookup"><span data-stu-id="cb864-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="cb864-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb864-113">PARAMETERS</span></span>

### <span data-ttu-id="cb864-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb864-114">-ApplicationGateway</span></span>
<span data-ttu-id="cb864-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb864-115">The applicationGateway</span></span>

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

### <span data-ttu-id="cb864-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="cb864-116">-CertificateFile</span></span>
<span data-ttu-id="cb864-117">Sökväg till certifikat-CER-fil</span><span class="sxs-lookup"><span data-stu-id="cb864-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="cb864-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb864-118">-DefaultProfile</span></span>
<span data-ttu-id="cb864-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cb864-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb864-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="cb864-120">-Name</span></span>
<span data-ttu-id="cb864-121">Namnet på TrustedRoot-certifikatet</span><span class="sxs-lookup"><span data-stu-id="cb864-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="cb864-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cb864-122">-Confirm</span></span>
<span data-ttu-id="cb864-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cb864-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb864-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb864-124">-WhatIf</span></span>
<span data-ttu-id="cb864-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cb864-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb864-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cb864-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb864-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb864-127">CommonParameters</span></span>
<span data-ttu-id="cb864-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb864-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb864-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb864-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb864-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb864-130">INPUTS</span></span>

### <span data-ttu-id="cb864-131">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb864-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cb864-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb864-132">OUTPUTS</span></span>

### <span data-ttu-id="cb864-133">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb864-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cb864-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb864-134">NOTES</span></span>

## <span data-ttu-id="cb864-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb864-135">RELATED LINKS</span></span>

[<span data-ttu-id="cb864-136">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cb864-136">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="cb864-137">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cb864-137">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="cb864-138">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cb864-138">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="cb864-139">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cb864-139">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)
