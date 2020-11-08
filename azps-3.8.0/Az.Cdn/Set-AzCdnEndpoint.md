---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: 7222b33470dc1fff22039c5e88bf3c6560b80c31
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090557"
---
# <span data-ttu-id="38de9-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="38de9-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="38de9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="38de9-102">SYNOPSIS</span></span>
<span data-ttu-id="38de9-103">Uppdaterar en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="38de9-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="38de9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="38de9-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38de9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="38de9-105">DESCRIPTION</span></span>
<span data-ttu-id="38de9-106">Cmdleten **set-AzCdnEndpoint** uppdaterar en CDN-slutpunkt (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="38de9-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="38de9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="38de9-107">EXAMPLES</span></span>

## <span data-ttu-id="38de9-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="38de9-108">PARAMETERS</span></span>

### <span data-ttu-id="38de9-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="38de9-109">-CdnEndpoint</span></span>
<span data-ttu-id="38de9-110">Anger slut punkten som den här cmdleten uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="38de9-110">Specifies the endpoint that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38de9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38de9-111">-DefaultProfile</span></span>
<span data-ttu-id="38de9-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="38de9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38de9-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="38de9-113">-Confirm</span></span>
<span data-ttu-id="38de9-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="38de9-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38de9-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38de9-115">-WhatIf</span></span>
<span data-ttu-id="38de9-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="38de9-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38de9-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="38de9-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38de9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38de9-118">CommonParameters</span></span>
<span data-ttu-id="38de9-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38de9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38de9-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38de9-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38de9-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="38de9-121">INPUTS</span></span>

### <span data-ttu-id="38de9-122">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="38de9-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="38de9-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="38de9-123">OUTPUTS</span></span>

### <span data-ttu-id="38de9-124">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="38de9-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="38de9-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="38de9-125">NOTES</span></span>

## <span data-ttu-id="38de9-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="38de9-126">RELATED LINKS</span></span>

[<span data-ttu-id="38de9-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="38de9-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="38de9-128">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="38de9-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="38de9-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="38de9-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="38de9-130">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="38de9-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="38de9-131">Stopp-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="38de9-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


