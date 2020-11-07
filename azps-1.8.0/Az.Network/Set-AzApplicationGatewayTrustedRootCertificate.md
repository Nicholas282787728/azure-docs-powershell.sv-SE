---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: e94ca1bbed8e37643b301e5a5cb2ca3acc78d264
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747758"
---
# <span data-ttu-id="73266-101">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="73266-101">Set-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="73266-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73266-102">SYNOPSIS</span></span>
<span data-ttu-id="73266-103">Uppdaterar ett betrott rot certifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="73266-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

## <span data-ttu-id="73266-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73266-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73266-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73266-105">DESCRIPTION</span></span>
<span data-ttu-id="73266-106">Cmdleten **set-AzApplicationGatewayTrustedRootCertificate** ändrar det befintliga betrodda rot certifikatet för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="73266-106">The **Set-AzApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="73266-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73266-107">EXAMPLES</span></span>

### <span data-ttu-id="73266-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="73266-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="73266-109">Ovan visas exempel på hur du uppdaterar ett befintligt betrott rot certifikat när ett rot certifikat är uppkopplat.</span><span class="sxs-lookup"><span data-stu-id="73266-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="73266-110">Det första kommandot får en Programgateway och lagrar den i $gw variabeln.</span><span class="sxs-lookup"><span data-stu-id="73266-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="73266-111">Det andra kommandot ändrar det befintliga betrodda rot certifikatet med ett nytt rot certifikat.</span><span class="sxs-lookup"><span data-stu-id="73266-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="73266-112">Det tredje kommandot uppdaterar programgatewayen på Azure.</span><span class="sxs-lookup"><span data-stu-id="73266-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="73266-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73266-113">PARAMETERS</span></span>

### <span data-ttu-id="73266-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73266-114">-ApplicationGateway</span></span>
<span data-ttu-id="73266-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73266-115">The applicationGateway</span></span>

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

### <span data-ttu-id="73266-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="73266-116">-CertificateFile</span></span>
<span data-ttu-id="73266-117">Sökväg till certifikat-CER-fil</span><span class="sxs-lookup"><span data-stu-id="73266-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="73266-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73266-118">-DefaultProfile</span></span>
<span data-ttu-id="73266-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="73266-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73266-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="73266-120">-Name</span></span>
<span data-ttu-id="73266-121">Namnet på TrustedRoot-certifikatet</span><span class="sxs-lookup"><span data-stu-id="73266-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="73266-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="73266-122">-Confirm</span></span>
<span data-ttu-id="73266-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="73266-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73266-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73266-124">-WhatIf</span></span>
<span data-ttu-id="73266-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="73266-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73266-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="73266-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73266-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73266-127">CommonParameters</span></span>
<span data-ttu-id="73266-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73266-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73266-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73266-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73266-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73266-130">INPUTS</span></span>

### <span data-ttu-id="73266-131">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73266-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="73266-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73266-132">OUTPUTS</span></span>

### <span data-ttu-id="73266-133">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73266-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="73266-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73266-134">NOTES</span></span>

## <span data-ttu-id="73266-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73266-135">RELATED LINKS</span></span>

[<span data-ttu-id="73266-136">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="73266-136">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="73266-137">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="73266-137">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="73266-138">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="73266-138">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="73266-139">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="73266-139">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)