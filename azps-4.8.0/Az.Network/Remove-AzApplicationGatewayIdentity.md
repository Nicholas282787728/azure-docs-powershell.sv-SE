---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
ms.openlocfilehash: d0056cedad180fda8475abae2106aaba3d2ad239
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261834"
---
# <span data-ttu-id="7bfa9-101">Remove-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="7bfa9-101">Remove-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="7bfa9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7bfa9-102">SYNOPSIS</span></span>
<span data-ttu-id="7bfa9-103">Tar bort en identitet från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-103">Removes a identity from an application gateway.</span></span>

## <span data-ttu-id="7bfa9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7bfa9-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bfa9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7bfa9-105">DESCRIPTION</span></span>
<span data-ttu-id="7bfa9-106">**Remove-AzApplicationGatewayIdentity** cmdlet tar bort identitet från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-106">**Remove-AzApplicationGatewayIdentity** cmdlet removes identity from an application gateway.</span></span>

## <span data-ttu-id="7bfa9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7bfa9-107">EXAMPLES</span></span>

### <span data-ttu-id="7bfa9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7bfa9-108">Example 1</span></span>
```powershell
PS C:\> $appgw = Remove-AzApplicationGatewayIdentity -ApplicationGateway $appgw
PS C:\> $updatedgateway = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="7bfa9-109">I det här exemplet tar vi bort identitet från en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-109">In this example, we remove identity from an existing application gateway.</span></span>
<span data-ttu-id="7bfa9-110">OBS! om gatewayen refererar till en nyckel valv hemlighet är det också viktigt att ta bort dessa SSL-certifikat.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-110">Note: If the gateway is referencing a keyvault secret, then it is also important to remove those ssl certificate references along this operation.</span></span>

## <span data-ttu-id="7bfa9-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7bfa9-111">PARAMETERS</span></span>

### <span data-ttu-id="7bfa9-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7bfa9-112">-ApplicationGateway</span></span>
<span data-ttu-id="7bfa9-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7bfa9-113">The applicationGateway</span></span>

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

### <span data-ttu-id="7bfa9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bfa9-114">-DefaultProfile</span></span>
<span data-ttu-id="7bfa9-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bfa9-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7bfa9-116">-Confirm</span></span>
<span data-ttu-id="7bfa9-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bfa9-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bfa9-118">-WhatIf</span></span>
<span data-ttu-id="7bfa9-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bfa9-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bfa9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bfa9-121">CommonParameters</span></span>
<span data-ttu-id="7bfa9-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bfa9-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bfa9-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bfa9-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7bfa9-124">INPUTS</span></span>

### <span data-ttu-id="7bfa9-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7bfa9-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7bfa9-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7bfa9-126">OUTPUTS</span></span>

### <span data-ttu-id="7bfa9-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7bfa9-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7bfa9-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7bfa9-128">NOTES</span></span>

## <span data-ttu-id="7bfa9-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7bfa9-129">RELATED LINKS</span></span>