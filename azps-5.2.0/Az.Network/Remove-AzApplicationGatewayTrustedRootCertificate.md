---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 3e8c4f6bc25ea5ff9b8efcee989937fb688fea57
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389964"
---
# <span data-ttu-id="6808e-101">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6808e-101">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="6808e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6808e-102">SYNOPSIS</span></span>
<span data-ttu-id="6808e-103">Tar bort ett betrott rot certifikat från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="6808e-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

## <span data-ttu-id="6808e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6808e-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedRootCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6808e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6808e-105">DESCRIPTION</span></span>
<span data-ttu-id="6808e-106">Cmdleten **Remove-AzApplicationGatewayTrustedRootCertificate** tar bort ett betrott rot certifikat från en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="6808e-106">The **Remove-AzApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="6808e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6808e-107">EXAMPLES</span></span>

### <span data-ttu-id="6808e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6808e-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="6808e-109">Det första kommandot får en Programgateway och lagrar den i $gw variabeln.</span><span class="sxs-lookup"><span data-stu-id="6808e-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="6808e-110">Det andra kommandot tar bort det betrodda rot certifikatet med namnet myRootCA från Application Gateway som lagras i $gw.</span><span class="sxs-lookup"><span data-stu-id="6808e-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="6808e-111">Det tredje kommandot uppdaterar programgatewayen på Azure.</span><span class="sxs-lookup"><span data-stu-id="6808e-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="6808e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6808e-112">PARAMETERS</span></span>

### <span data-ttu-id="6808e-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6808e-113">-ApplicationGateway</span></span>
<span data-ttu-id="6808e-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6808e-114">The applicationGateway</span></span>

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

### <span data-ttu-id="6808e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6808e-115">-DefaultProfile</span></span>
<span data-ttu-id="6808e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6808e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6808e-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="6808e-117">-Name</span></span>
<span data-ttu-id="6808e-118">Namnet på TrustedRoot-certifikatet</span><span class="sxs-lookup"><span data-stu-id="6808e-118">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="6808e-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6808e-119">-Confirm</span></span>
<span data-ttu-id="6808e-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6808e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6808e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6808e-121">-WhatIf</span></span>
<span data-ttu-id="6808e-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6808e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6808e-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6808e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6808e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6808e-124">CommonParameters</span></span>
<span data-ttu-id="6808e-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6808e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6808e-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6808e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6808e-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6808e-127">INPUTS</span></span>

### <span data-ttu-id="6808e-128">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6808e-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6808e-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6808e-129">OUTPUTS</span></span>

### <span data-ttu-id="6808e-130">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6808e-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6808e-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6808e-131">NOTES</span></span>

## <span data-ttu-id="6808e-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6808e-132">RELATED LINKS</span></span>

[<span data-ttu-id="6808e-133">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6808e-133">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="6808e-134">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6808e-134">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="6808e-135">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6808e-135">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="6808e-136">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6808e-136">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
