---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: a71ba6f6d9b45e0016589d5629f029998f33963f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758376"
---
# <span data-ttu-id="e3f0a-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e3f0a-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="e3f0a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="e3f0a-103">Uppdaterar ett autentiseringscertifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="e3f0a-103">Updates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3f0a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3f0a-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3f0a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3f0a-105">DESCRIPTION</span></span>
<span data-ttu-id="e3f0a-106">Cmdleten **set-AzureRmApplicationGatewayAuthenticationCertificate** uppdaterar ett autentiseringscertifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e3f0a-106">The **Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="e3f0a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3f0a-107">EXAMPLES</span></span>

## <span data-ttu-id="e3f0a-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3f0a-108">PARAMETERS</span></span>

### <span data-ttu-id="e3f0a-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3f0a-109">-ApplicationGateway</span></span>
<span data-ttu-id="e3f0a-110">Anger namnet på den Programgateway för vilken denna cmdlet uppdaterar ett autentiseringscertifikat.</span><span class="sxs-lookup"><span data-stu-id="e3f0a-110">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="e3f0a-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="e3f0a-111">-CertificateFile</span></span>
<span data-ttu-id="e3f0a-112">Anger sökvägen till den fil för meddelandeautentisering med vilken denna cmdlet uppdaterar certifikatet.</span><span class="sxs-lookup"><span data-stu-id="e3f0a-112">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="e3f0a-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="e3f0a-113">-Name</span></span>
<span data-ttu-id="e3f0a-114">Anger namnet på det autentiseringscertifikat som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="e3f0a-114">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="e3f0a-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e3f0a-115">-Confirm</span></span>
<span data-ttu-id="e3f0a-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e3f0a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3f0a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3f0a-117">-WhatIf</span></span>
<span data-ttu-id="e3f0a-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e3f0a-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3f0a-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e3f0a-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3f0a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3f0a-120">-DefaultProfile</span></span>
<span data-ttu-id="e3f0a-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e3f0a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3f0a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f0a-122">CommonParameters</span></span>
<span data-ttu-id="e3f0a-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3f0a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f0a-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3f0a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f0a-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3f0a-125">INPUTS</span></span>

### <span data-ttu-id="e3f0a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e3f0a-126">System.String</span></span>

## <span data-ttu-id="e3f0a-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3f0a-127">OUTPUTS</span></span>

### <span data-ttu-id="e3f0a-128">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3f0a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e3f0a-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3f0a-129">NOTES</span></span>
* <span data-ttu-id="e3f0a-130">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="e3f0a-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e3f0a-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3f0a-131">RELATED LINKS</span></span>

[<span data-ttu-id="e3f0a-132">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e3f0a-132">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="e3f0a-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e3f0a-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="e3f0a-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e3f0a-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="e3f0a-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e3f0a-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)


