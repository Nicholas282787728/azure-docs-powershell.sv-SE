---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 00ad021e86617d08f0ca30f660cac28110348885
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929346"
---
# <span data-ttu-id="2f1cb-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2f1cb-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="2f1cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f1cb-102">SYNOPSIS</span></span>
<span data-ttu-id="2f1cb-103">Tar bort ett autentiseringscertifikat från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="2f1cb-103">Removes an authentication certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f1cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2f1cb-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f1cb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2f1cb-105">DESCRIPTION</span></span>
<span data-ttu-id="2f1cb-106">Cmdleten **Remove-AzureRmApplicationGatewayAuthenticationCertificate** tar bort ett autentiseringscertifikat från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="2f1cb-106">The **Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="2f1cb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2f1cb-107">EXAMPLES</span></span>

### <span data-ttu-id="2f1cb-108">9.1</span><span class="sxs-lookup"><span data-stu-id="2f1cb-108">1:</span></span>
```

```

## <span data-ttu-id="2f1cb-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2f1cb-109">PARAMETERS</span></span>

### <span data-ttu-id="2f1cb-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2f1cb-110">-ApplicationGateway</span></span>
<span data-ttu-id="2f1cb-111">Anger namnet på den Programgateway som den här cmdleten tar bort ett autentiseringscertifikat från.</span><span class="sxs-lookup"><span data-stu-id="2f1cb-111">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="2f1cb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f1cb-112">-DefaultProfile</span></span>
<span data-ttu-id="2f1cb-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2f1cb-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f1cb-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="2f1cb-114">-Name</span></span>
<span data-ttu-id="2f1cb-115">Anger namnet på det autentiseringscertifikat som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="2f1cb-115">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2f1cb-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2f1cb-116">-Confirm</span></span>
<span data-ttu-id="2f1cb-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2f1cb-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f1cb-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f1cb-118">-WhatIf</span></span>
<span data-ttu-id="2f1cb-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2f1cb-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f1cb-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2f1cb-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f1cb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f1cb-121">CommonParameters</span></span>
<span data-ttu-id="2f1cb-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f1cb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f1cb-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f1cb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f1cb-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2f1cb-124">INPUTS</span></span>

### <span data-ttu-id="2f1cb-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2f1cb-125">System.String</span></span>

## <span data-ttu-id="2f1cb-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2f1cb-126">OUTPUTS</span></span>

### <span data-ttu-id="2f1cb-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2f1cb-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2f1cb-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2f1cb-128">NOTES</span></span>
* <span data-ttu-id="2f1cb-129">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="2f1cb-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="2f1cb-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2f1cb-130">RELATED LINKS</span></span>

[<span data-ttu-id="2f1cb-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2f1cb-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="2f1cb-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2f1cb-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="2f1cb-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2f1cb-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="2f1cb-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2f1cb-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


