---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: c43fe72f8f3669b7e6e123a7f1d606771b161084
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092574"
---
# <span data-ttu-id="eaa81-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="eaa81-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="eaa81-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eaa81-102">SYNOPSIS</span></span>
<span data-ttu-id="eaa81-103">Skapar ett autentiseringscertifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="eaa81-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="eaa81-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eaa81-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaa81-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eaa81-105">DESCRIPTION</span></span>
<span data-ttu-id="eaa81-106">Cmdleten **New-AzApplicationGatewayAuthenticationCertificate** skapar ett autentiseringscertifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="eaa81-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="eaa81-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eaa81-107">EXAMPLES</span></span>

### <span data-ttu-id="eaa81-108">Exempel 1: skapa ett autentiseringscertifikat</span><span class="sxs-lookup"><span data-stu-id="eaa81-108">Example 1: Create an authentication certificate</span></span>
```
PS C:\> $cert = New-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -CertificateFile "C:\cert.cer"
```

<span data-ttu-id="eaa81-109">Det första kommandot skapar autentiseringscertifikatet med namnet cert01.</span><span class="sxs-lookup"><span data-stu-id="eaa81-109">The first command creates authentication certificate named cert01.</span></span>

## <span data-ttu-id="eaa81-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eaa81-110">PARAMETERS</span></span>

### <span data-ttu-id="eaa81-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="eaa81-111">-CertificateFile</span></span>
<span data-ttu-id="eaa81-112">Anger sökvägen till autentiseringscertifikatet.</span><span class="sxs-lookup"><span data-stu-id="eaa81-112">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="eaa81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaa81-113">-DefaultProfile</span></span>
<span data-ttu-id="eaa81-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eaa81-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaa81-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="eaa81-115">-Name</span></span>
<span data-ttu-id="eaa81-116">Anger ett namn på autentiseringscertifikatet.</span><span class="sxs-lookup"><span data-stu-id="eaa81-116">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="eaa81-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eaa81-117">-Confirm</span></span>
<span data-ttu-id="eaa81-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eaa81-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaa81-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaa81-119">-WhatIf</span></span>
<span data-ttu-id="eaa81-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eaa81-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaa81-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eaa81-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaa81-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaa81-122">CommonParameters</span></span>
<span data-ttu-id="eaa81-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaa81-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaa81-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaa81-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaa81-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eaa81-125">INPUTS</span></span>

### <span data-ttu-id="eaa81-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="eaa81-126">None</span></span>

## <span data-ttu-id="eaa81-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eaa81-127">OUTPUTS</span></span>

### <span data-ttu-id="eaa81-128">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="eaa81-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="eaa81-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eaa81-129">NOTES</span></span>
* <span data-ttu-id="eaa81-130">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="eaa81-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="eaa81-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eaa81-131">RELATED LINKS</span></span>

[<span data-ttu-id="eaa81-132">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="eaa81-132">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="eaa81-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="eaa81-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="eaa81-134">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="eaa81-134">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="eaa81-135">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="eaa81-135">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)

