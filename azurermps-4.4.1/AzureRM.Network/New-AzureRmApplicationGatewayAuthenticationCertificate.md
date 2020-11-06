---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 51bb8ff46613080d3fa62a2b4953419348cb99bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580539"
---
# <span data-ttu-id="82f34-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="82f34-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="82f34-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82f34-102">SYNOPSIS</span></span>
<span data-ttu-id="82f34-103">Skapar ett autentiseringscertifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="82f34-103">Creates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82f34-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82f34-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82f34-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82f34-105">DESCRIPTION</span></span>
<span data-ttu-id="82f34-106">Cmdleten **New-AzureRmApplicationGatewayAuthenticationCertificate** skapar ett autentiseringscertifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="82f34-106">The **New-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="82f34-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82f34-107">EXAMPLES</span></span>

## <span data-ttu-id="82f34-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82f34-108">PARAMETERS</span></span>

### <span data-ttu-id="82f34-109">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="82f34-109">-CertificateFile</span></span>
<span data-ttu-id="82f34-110">Anger sökvägen till autentiseringscertifikatet.</span><span class="sxs-lookup"><span data-stu-id="82f34-110">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="82f34-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="82f34-111">-Name</span></span>
<span data-ttu-id="82f34-112">Anger ett namn på autentiseringscertifikatet.</span><span class="sxs-lookup"><span data-stu-id="82f34-112">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="82f34-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="82f34-113">-Confirm</span></span>
<span data-ttu-id="82f34-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="82f34-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82f34-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82f34-115">-WhatIf</span></span>
<span data-ttu-id="82f34-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="82f34-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82f34-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="82f34-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82f34-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82f34-118">-DefaultProfile</span></span>
<span data-ttu-id="82f34-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="82f34-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82f34-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82f34-120">CommonParameters</span></span>
<span data-ttu-id="82f34-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82f34-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82f34-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82f34-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82f34-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82f34-123">INPUTS</span></span>

### <span data-ttu-id="82f34-124">System. String</span><span class="sxs-lookup"><span data-stu-id="82f34-124">System.String</span></span>

## <span data-ttu-id="82f34-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82f34-125">OUTPUTS</span></span>

### <span data-ttu-id="82f34-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="82f34-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="82f34-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82f34-127">NOTES</span></span>
* <span data-ttu-id="82f34-128">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="82f34-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="82f34-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82f34-129">RELATED LINKS</span></span>

[<span data-ttu-id="82f34-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="82f34-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="82f34-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="82f34-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="82f34-132">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="82f34-132">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="82f34-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="82f34-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


