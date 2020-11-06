---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 8edf8d3cee1936af263d759e512a6683af1ccde8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581095"
---
# <span data-ttu-id="5ee1b-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5ee1b-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="5ee1b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ee1b-102">SYNOPSIS</span></span>
<span data-ttu-id="5ee1b-103">Skapar ett autentiseringscertifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="5ee1b-103">Creates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ee1b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ee1b-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ee1b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ee1b-105">DESCRIPTION</span></span>
<span data-ttu-id="5ee1b-106">Cmdleten **New-AzureRmApplicationGatewayAuthenticationCertificate** skapar ett autentiseringscertifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="5ee1b-106">The **New-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="5ee1b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ee1b-107">EXAMPLES</span></span>

## <span data-ttu-id="5ee1b-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ee1b-108">PARAMETERS</span></span>

### <span data-ttu-id="5ee1b-109">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="5ee1b-109">-CertificateFile</span></span>
<span data-ttu-id="5ee1b-110">Anger sökvägen till autentiseringscertifikatet.</span><span class="sxs-lookup"><span data-stu-id="5ee1b-110">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="5ee1b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ee1b-111">-DefaultProfile</span></span>
<span data-ttu-id="5ee1b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ee1b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ee1b-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="5ee1b-113">-Name</span></span>
<span data-ttu-id="5ee1b-114">Anger ett namn på autentiseringscertifikatet.</span><span class="sxs-lookup"><span data-stu-id="5ee1b-114">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="5ee1b-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5ee1b-115">-Confirm</span></span>
<span data-ttu-id="5ee1b-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5ee1b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ee1b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ee1b-117">-WhatIf</span></span>
<span data-ttu-id="5ee1b-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5ee1b-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ee1b-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5ee1b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ee1b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ee1b-120">CommonParameters</span></span>
<span data-ttu-id="5ee1b-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ee1b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ee1b-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ee1b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ee1b-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ee1b-123">INPUTS</span></span>

### <span data-ttu-id="5ee1b-124">System. String</span><span class="sxs-lookup"><span data-stu-id="5ee1b-124">System.String</span></span>

## <span data-ttu-id="5ee1b-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ee1b-125">OUTPUTS</span></span>

### <span data-ttu-id="5ee1b-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5ee1b-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="5ee1b-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ee1b-127">NOTES</span></span>
* <span data-ttu-id="5ee1b-128">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="5ee1b-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="5ee1b-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ee1b-129">RELATED LINKS</span></span>

[<span data-ttu-id="5ee1b-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5ee1b-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5ee1b-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5ee1b-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5ee1b-132">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5ee1b-132">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5ee1b-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5ee1b-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


