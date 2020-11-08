---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 02416fdb18f01c9a2af6c091b0be109b479ce45d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089782"
---
# <span data-ttu-id="abee1-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="abee1-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="abee1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="abee1-102">SYNOPSIS</span></span>
<span data-ttu-id="abee1-103">Tar bort ett autentiseringscertifikat från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="abee1-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="abee1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="abee1-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abee1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="abee1-105">DESCRIPTION</span></span>
<span data-ttu-id="abee1-106">Cmdleten **Remove-AzApplicationGatewayAuthenticationCertificate** tar bort ett autentiseringscertifikat från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="abee1-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="abee1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="abee1-107">EXAMPLES</span></span>

### <span data-ttu-id="abee1-108">Exempel 1: ta bort ett autentiseringscertifikat från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="abee1-108">Example 1: Remove an authentication certificate from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="abee1-109">Med det första kommandot får programgatewayen namnet appGwName och lagras resultatet i $appgw variabel.</span><span class="sxs-lookup"><span data-stu-id="abee1-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="abee1-110">Det andra kommandot tar bort autentiseringscertifikatet som heter cert01 från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="abee1-110">The second command removes the authentication certificate named cert01 from the application gateway.</span></span>
<span data-ttu-id="abee1-111">Det tredje kommandot uppdaterar programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="abee1-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="abee1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="abee1-112">PARAMETERS</span></span>

### <span data-ttu-id="abee1-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="abee1-113">-ApplicationGateway</span></span>
<span data-ttu-id="abee1-114">Anger namnet på den Programgateway som den här cmdleten tar bort ett autentiseringscertifikat från.</span><span class="sxs-lookup"><span data-stu-id="abee1-114">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="abee1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abee1-115">-DefaultProfile</span></span>
<span data-ttu-id="abee1-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="abee1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abee1-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="abee1-117">-Name</span></span>
<span data-ttu-id="abee1-118">Anger namnet på det autentiseringscertifikat som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="abee1-118">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="abee1-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="abee1-119">-Confirm</span></span>
<span data-ttu-id="abee1-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="abee1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abee1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abee1-121">-WhatIf</span></span>
<span data-ttu-id="abee1-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="abee1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abee1-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="abee1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abee1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abee1-124">CommonParameters</span></span>
<span data-ttu-id="abee1-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abee1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abee1-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abee1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abee1-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="abee1-127">INPUTS</span></span>

### <span data-ttu-id="abee1-128">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="abee1-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="abee1-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="abee1-129">OUTPUTS</span></span>

### <span data-ttu-id="abee1-130">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="abee1-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="abee1-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="abee1-131">NOTES</span></span>
* <span data-ttu-id="abee1-132">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="abee1-132">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="abee1-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="abee1-133">RELATED LINKS</span></span>

[<span data-ttu-id="abee1-134">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="abee1-134">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="abee1-135">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="abee1-135">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="abee1-136">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="abee1-136">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="abee1-137">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="abee1-137">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


