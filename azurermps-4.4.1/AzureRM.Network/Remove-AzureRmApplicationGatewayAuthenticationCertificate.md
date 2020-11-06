---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 3facee36f6862c02975566dee20d9e7fb8c8824f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574579"
---
# <span data-ttu-id="3f59c-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="3f59c-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="3f59c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f59c-102">SYNOPSIS</span></span>
<span data-ttu-id="3f59c-103">Tar bort ett autentiseringscertifikat från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="3f59c-103">Removes an authentication certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f59c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f59c-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f59c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f59c-105">DESCRIPTION</span></span>
<span data-ttu-id="3f59c-106">Cmdleten **Remove-AzureRmApplicationGatewayAuthenticationCertificate** tar bort ett autentiseringscertifikat från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="3f59c-106">The **Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="3f59c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f59c-107">EXAMPLES</span></span>

## <span data-ttu-id="3f59c-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f59c-108">PARAMETERS</span></span>

### <span data-ttu-id="3f59c-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3f59c-109">-ApplicationGateway</span></span>
<span data-ttu-id="3f59c-110">Anger namnet på den Programgateway som den här cmdleten tar bort ett autentiseringscertifikat från.</span><span class="sxs-lookup"><span data-stu-id="3f59c-110">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="3f59c-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="3f59c-111">-Name</span></span>
<span data-ttu-id="3f59c-112">Anger namnet på det autentiseringscertifikat som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="3f59c-112">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3f59c-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3f59c-113">-Confirm</span></span>
<span data-ttu-id="3f59c-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3f59c-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f59c-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f59c-115">-WhatIf</span></span>
<span data-ttu-id="3f59c-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3f59c-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f59c-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3f59c-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f59c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f59c-118">-DefaultProfile</span></span>
<span data-ttu-id="3f59c-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3f59c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f59c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f59c-120">CommonParameters</span></span>
<span data-ttu-id="3f59c-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f59c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f59c-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f59c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f59c-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f59c-123">INPUTS</span></span>

### <span data-ttu-id="3f59c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="3f59c-124">System.String</span></span>

## <span data-ttu-id="3f59c-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f59c-125">OUTPUTS</span></span>

### <span data-ttu-id="3f59c-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3f59c-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3f59c-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f59c-127">NOTES</span></span>
* <span data-ttu-id="3f59c-128">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="3f59c-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="3f59c-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f59c-129">RELATED LINKS</span></span>

[<span data-ttu-id="3f59c-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="3f59c-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="3f59c-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="3f59c-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="3f59c-132">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="3f59c-132">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="3f59c-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="3f59c-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


