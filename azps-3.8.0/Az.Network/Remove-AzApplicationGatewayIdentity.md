---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
ms.openlocfilehash: d0056cedad180fda8475abae2106aaba3d2ad239
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088073"
---
# <span data-ttu-id="92cb4-101">Remove-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="92cb4-101">Remove-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="92cb4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92cb4-102">SYNOPSIS</span></span>
<span data-ttu-id="92cb4-103">Tar bort en identitet från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="92cb4-103">Removes a identity from an application gateway.</span></span>

## <span data-ttu-id="92cb4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92cb4-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92cb4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92cb4-105">DESCRIPTION</span></span>
<span data-ttu-id="92cb4-106">**Remove-AzApplicationGatewayIdentity** cmdlet tar bort identitet från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="92cb4-106">**Remove-AzApplicationGatewayIdentity** cmdlet removes identity from an application gateway.</span></span>

## <span data-ttu-id="92cb4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92cb4-107">EXAMPLES</span></span>

### <span data-ttu-id="92cb4-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="92cb4-108">Example 1</span></span>
```powershell
PS C:\> $appgw = Remove-AzApplicationGatewayIdentity -ApplicationGateway $appgw
PS C:\> $updatedgateway = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="92cb4-109">I det här exemplet tar vi bort identitet från en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="92cb4-109">In this example, we remove identity from an existing application gateway.</span></span>
<span data-ttu-id="92cb4-110">OBS! om gatewayen refererar till en nyckel valv hemlighet är det också viktigt att ta bort dessa SSL-certifikat.</span><span class="sxs-lookup"><span data-stu-id="92cb4-110">Note: If the gateway is referencing a keyvault secret, then it is also important to remove those ssl certificate references along this operation.</span></span>

## <span data-ttu-id="92cb4-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92cb4-111">PARAMETERS</span></span>

### <span data-ttu-id="92cb4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92cb4-112">-ApplicationGateway</span></span>
<span data-ttu-id="92cb4-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92cb4-113">The applicationGateway</span></span>

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

### <span data-ttu-id="92cb4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92cb4-114">-DefaultProfile</span></span>
<span data-ttu-id="92cb4-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="92cb4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92cb4-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="92cb4-116">-Confirm</span></span>
<span data-ttu-id="92cb4-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="92cb4-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92cb4-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92cb4-118">-WhatIf</span></span>
<span data-ttu-id="92cb4-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="92cb4-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92cb4-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="92cb4-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92cb4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92cb4-121">CommonParameters</span></span>
<span data-ttu-id="92cb4-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92cb4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92cb4-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92cb4-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92cb4-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92cb4-124">INPUTS</span></span>

### <span data-ttu-id="92cb4-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92cb4-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="92cb4-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92cb4-126">OUTPUTS</span></span>

### <span data-ttu-id="92cb4-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92cb4-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="92cb4-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92cb4-128">NOTES</span></span>

## <span data-ttu-id="92cb4-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92cb4-129">RELATED LINKS</span></span>