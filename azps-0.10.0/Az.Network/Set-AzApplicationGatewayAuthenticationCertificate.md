---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 23b337779da46169be29e3dd6fef55fc70f4f035
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924301"
---
# <span data-ttu-id="126cc-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="126cc-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="126cc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="126cc-102">SYNOPSIS</span></span>
<span data-ttu-id="126cc-103">Uppdaterar ett autentiseringscertifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="126cc-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="126cc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="126cc-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="126cc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="126cc-105">DESCRIPTION</span></span>
<span data-ttu-id="126cc-106">Cmdleten **set-AzApplicationGatewayAuthenticationCertificate** uppdaterar ett autentiseringscertifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="126cc-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="126cc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="126cc-107">EXAMPLES</span></span>

### <span data-ttu-id="126cc-108">9.1</span><span class="sxs-lookup"><span data-stu-id="126cc-108">1:</span></span>
```

```

## <span data-ttu-id="126cc-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="126cc-109">PARAMETERS</span></span>

### <span data-ttu-id="126cc-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="126cc-110">-ApplicationGateway</span></span>
<span data-ttu-id="126cc-111">Anger namnet på den Programgateway för vilken denna cmdlet uppdaterar ett autentiseringscertifikat.</span><span class="sxs-lookup"><span data-stu-id="126cc-111">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="126cc-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="126cc-112">-CertificateFile</span></span>
<span data-ttu-id="126cc-113">Anger sökvägen till den fil för meddelandeautentisering med vilken denna cmdlet uppdaterar certifikatet.</span><span class="sxs-lookup"><span data-stu-id="126cc-113">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="126cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="126cc-114">-DefaultProfile</span></span>
<span data-ttu-id="126cc-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="126cc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="126cc-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="126cc-116">-Name</span></span>
<span data-ttu-id="126cc-117">Anger namnet på det autentiseringscertifikat som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="126cc-117">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="126cc-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="126cc-118">-Confirm</span></span>
<span data-ttu-id="126cc-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="126cc-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="126cc-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="126cc-120">-WhatIf</span></span>
<span data-ttu-id="126cc-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="126cc-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="126cc-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="126cc-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="126cc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="126cc-123">CommonParameters</span></span>
<span data-ttu-id="126cc-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="126cc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="126cc-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="126cc-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="126cc-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="126cc-126">INPUTS</span></span>

### <span data-ttu-id="126cc-127">System. String</span><span class="sxs-lookup"><span data-stu-id="126cc-127">System.String</span></span>

## <span data-ttu-id="126cc-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="126cc-128">OUTPUTS</span></span>

### <span data-ttu-id="126cc-129">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="126cc-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="126cc-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="126cc-130">NOTES</span></span>
* <span data-ttu-id="126cc-131">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="126cc-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="126cc-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="126cc-132">RELATED LINKS</span></span>

[<span data-ttu-id="126cc-133">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="126cc-133">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="126cc-134">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="126cc-134">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="126cc-135">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="126cc-135">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="126cc-136">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="126cc-136">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)


