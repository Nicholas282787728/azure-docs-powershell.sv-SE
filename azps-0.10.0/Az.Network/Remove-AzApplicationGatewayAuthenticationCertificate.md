---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: bf11b2b3010a7f7683d670c3c5e95d4248b83cd6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922075"
---
# <span data-ttu-id="1c5e8-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1c5e8-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="1c5e8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c5e8-102">SYNOPSIS</span></span>
<span data-ttu-id="1c5e8-103">Tar bort ett autentiseringscertifikat från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="1c5e8-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="1c5e8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c5e8-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1c5e8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c5e8-105">DESCRIPTION</span></span>
<span data-ttu-id="1c5e8-106">Cmdleten **Remove-AzApplicationGatewayAuthenticationCertificate** tar bort ett autentiseringscertifikat från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="1c5e8-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="1c5e8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c5e8-107">EXAMPLES</span></span>

### <span data-ttu-id="1c5e8-108">9.1</span><span class="sxs-lookup"><span data-stu-id="1c5e8-108">1:</span></span>
```

```

## <span data-ttu-id="1c5e8-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c5e8-109">PARAMETERS</span></span>

### <span data-ttu-id="1c5e8-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1c5e8-110">-ApplicationGateway</span></span>
<span data-ttu-id="1c5e8-111">Anger namnet på den Programgateway som den här cmdleten tar bort ett autentiseringscertifikat från.</span><span class="sxs-lookup"><span data-stu-id="1c5e8-111">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="1c5e8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c5e8-112">-DefaultProfile</span></span>
<span data-ttu-id="1c5e8-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1c5e8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c5e8-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="1c5e8-114">-Name</span></span>
<span data-ttu-id="1c5e8-115">Anger namnet på det autentiseringscertifikat som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="1c5e8-115">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1c5e8-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1c5e8-116">-Confirm</span></span>
<span data-ttu-id="1c5e8-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1c5e8-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c5e8-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c5e8-118">-WhatIf</span></span>
<span data-ttu-id="1c5e8-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1c5e8-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c5e8-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1c5e8-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c5e8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c5e8-121">CommonParameters</span></span>
<span data-ttu-id="1c5e8-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c5e8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c5e8-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c5e8-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c5e8-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c5e8-124">INPUTS</span></span>

### <span data-ttu-id="1c5e8-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1c5e8-125">System.String</span></span>

## <span data-ttu-id="1c5e8-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c5e8-126">OUTPUTS</span></span>

### <span data-ttu-id="1c5e8-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1c5e8-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1c5e8-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c5e8-128">NOTES</span></span>
* <span data-ttu-id="1c5e8-129">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="1c5e8-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="1c5e8-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c5e8-130">RELATED LINKS</span></span>

[<span data-ttu-id="1c5e8-131">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1c5e8-131">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="1c5e8-132">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1c5e8-132">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="1c5e8-133">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1c5e8-133">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="1c5e8-134">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1c5e8-134">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


