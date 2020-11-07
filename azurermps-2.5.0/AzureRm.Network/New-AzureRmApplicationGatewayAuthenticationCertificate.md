---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 3847c1026f8cea6f3c33db45215a7a3253e4c680
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929749"
---
# <span data-ttu-id="4ed5a-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4ed5a-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="4ed5a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ed5a-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed5a-103">Skapar ett autentiseringscertifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="4ed5a-103">Creates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ed5a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ed5a-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ed5a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ed5a-105">DESCRIPTION</span></span>
<span data-ttu-id="4ed5a-106">Cmdleten **New-AzureRmApplicationGatewayAuthenticationCertificate** skapar ett autentiseringscertifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4ed5a-106">The **New-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="4ed5a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ed5a-107">EXAMPLES</span></span>

### <span data-ttu-id="4ed5a-108">9.1</span><span class="sxs-lookup"><span data-stu-id="4ed5a-108">1:</span></span>
```

```

## <span data-ttu-id="4ed5a-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ed5a-109">PARAMETERS</span></span>

### <span data-ttu-id="4ed5a-110">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="4ed5a-110">-CertificateFile</span></span>
<span data-ttu-id="4ed5a-111">Anger sökvägen till autentiseringscertifikatet.</span><span class="sxs-lookup"><span data-stu-id="4ed5a-111">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="4ed5a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ed5a-112">-DefaultProfile</span></span>
<span data-ttu-id="4ed5a-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4ed5a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ed5a-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="4ed5a-114">-Name</span></span>
<span data-ttu-id="4ed5a-115">Anger ett namn på autentiseringscertifikatet.</span><span class="sxs-lookup"><span data-stu-id="4ed5a-115">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="4ed5a-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4ed5a-116">-Confirm</span></span>
<span data-ttu-id="4ed5a-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4ed5a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ed5a-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ed5a-118">-WhatIf</span></span>
<span data-ttu-id="4ed5a-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4ed5a-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ed5a-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4ed5a-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ed5a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed5a-121">CommonParameters</span></span>
<span data-ttu-id="4ed5a-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ed5a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed5a-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ed5a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed5a-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ed5a-124">INPUTS</span></span>

### <span data-ttu-id="4ed5a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4ed5a-125">System.String</span></span>

## <span data-ttu-id="4ed5a-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ed5a-126">OUTPUTS</span></span>

### <span data-ttu-id="4ed5a-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4ed5a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="4ed5a-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ed5a-128">NOTES</span></span>
* <span data-ttu-id="4ed5a-129">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="4ed5a-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4ed5a-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ed5a-130">RELATED LINKS</span></span>

[<span data-ttu-id="4ed5a-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4ed5a-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="4ed5a-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4ed5a-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="4ed5a-133">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4ed5a-133">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="4ed5a-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4ed5a-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


