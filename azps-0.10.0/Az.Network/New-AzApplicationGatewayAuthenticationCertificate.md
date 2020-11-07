---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 8f3685fddf4796cd0ad500c261f157e8ac5b95f5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922182"
---
# <span data-ttu-id="74221-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="74221-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="74221-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="74221-102">SYNOPSIS</span></span>
<span data-ttu-id="74221-103">Skapar ett autentiseringscertifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="74221-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="74221-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="74221-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74221-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="74221-105">DESCRIPTION</span></span>
<span data-ttu-id="74221-106">Cmdleten **New-AzApplicationGatewayAuthenticationCertificate** skapar ett autentiseringscertifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="74221-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="74221-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="74221-107">EXAMPLES</span></span>

### <span data-ttu-id="74221-108">9.1</span><span class="sxs-lookup"><span data-stu-id="74221-108">1:</span></span>
```

```

## <span data-ttu-id="74221-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="74221-109">PARAMETERS</span></span>

### <span data-ttu-id="74221-110">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="74221-110">-CertificateFile</span></span>
<span data-ttu-id="74221-111">Anger sökvägen till autentiseringscertifikatet.</span><span class="sxs-lookup"><span data-stu-id="74221-111">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="74221-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74221-112">-DefaultProfile</span></span>
<span data-ttu-id="74221-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="74221-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74221-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="74221-114">-Name</span></span>
<span data-ttu-id="74221-115">Anger ett namn på autentiseringscertifikatet.</span><span class="sxs-lookup"><span data-stu-id="74221-115">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="74221-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="74221-116">-Confirm</span></span>
<span data-ttu-id="74221-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="74221-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74221-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74221-118">-WhatIf</span></span>
<span data-ttu-id="74221-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="74221-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74221-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="74221-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74221-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74221-121">CommonParameters</span></span>
<span data-ttu-id="74221-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74221-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74221-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74221-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74221-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="74221-124">INPUTS</span></span>

### <span data-ttu-id="74221-125">System. String</span><span class="sxs-lookup"><span data-stu-id="74221-125">System.String</span></span>

## <span data-ttu-id="74221-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="74221-126">OUTPUTS</span></span>

### <span data-ttu-id="74221-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="74221-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="74221-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="74221-128">NOTES</span></span>
* <span data-ttu-id="74221-129">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="74221-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="74221-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="74221-130">RELATED LINKS</span></span>

[<span data-ttu-id="74221-131">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="74221-131">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="74221-132">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="74221-132">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="74221-133">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="74221-133">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="74221-134">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="74221-134">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


