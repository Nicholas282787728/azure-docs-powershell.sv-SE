---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 9ec4522da3c5a75a1c9e5bad977f294e0987f4fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575199"
---
# <span data-ttu-id="fb281-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fb281-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="fb281-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb281-102">SYNOPSIS</span></span>
<span data-ttu-id="fb281-103">Tar bort ett autentiseringscertifikat från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="fb281-103">Removes an authentication certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb281-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb281-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb281-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb281-105">DESCRIPTION</span></span>
<span data-ttu-id="fb281-106">Cmdleten **Remove-AzureRmApplicationGatewayAuthenticationCertificate** tar bort ett autentiseringscertifikat från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="fb281-106">The **Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="fb281-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb281-107">EXAMPLES</span></span>

## <span data-ttu-id="fb281-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb281-108">PARAMETERS</span></span>

### <span data-ttu-id="fb281-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb281-109">-ApplicationGateway</span></span>
<span data-ttu-id="fb281-110">Anger namnet på den Programgateway som den här cmdleten tar bort ett autentiseringscertifikat från.</span><span class="sxs-lookup"><span data-stu-id="fb281-110">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="fb281-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb281-111">-DefaultProfile</span></span>
<span data-ttu-id="fb281-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fb281-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb281-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="fb281-113">-Name</span></span>
<span data-ttu-id="fb281-114">Anger namnet på det autentiseringscertifikat som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="fb281-114">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fb281-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fb281-115">-Confirm</span></span>
<span data-ttu-id="fb281-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fb281-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb281-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb281-117">-WhatIf</span></span>
<span data-ttu-id="fb281-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fb281-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb281-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fb281-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb281-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb281-120">CommonParameters</span></span>
<span data-ttu-id="fb281-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb281-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb281-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb281-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb281-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb281-123">INPUTS</span></span>

### <span data-ttu-id="fb281-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb281-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="fb281-125">Parametrar: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fb281-125">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="fb281-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb281-126">OUTPUTS</span></span>

### <span data-ttu-id="fb281-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb281-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fb281-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb281-128">NOTES</span></span>
* <span data-ttu-id="fb281-129">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="fb281-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="fb281-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb281-130">RELATED LINKS</span></span>

[<span data-ttu-id="fb281-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fb281-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="fb281-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fb281-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="fb281-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fb281-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="fb281-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fb281-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


