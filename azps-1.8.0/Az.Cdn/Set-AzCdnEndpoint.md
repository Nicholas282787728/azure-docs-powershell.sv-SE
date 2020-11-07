---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: cce3e2f9deb1f5df5c85d4f0b289b97e9cd36820
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754629"
---
# <span data-ttu-id="6887d-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6887d-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="6887d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6887d-102">SYNOPSIS</span></span>
<span data-ttu-id="6887d-103">Uppdaterar en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="6887d-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="6887d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6887d-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6887d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6887d-105">DESCRIPTION</span></span>
<span data-ttu-id="6887d-106">Cmdleten **set-AzCdnEndpoint** uppdaterar en CDN-slutpunkt (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="6887d-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="6887d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6887d-107">EXAMPLES</span></span>

## <span data-ttu-id="6887d-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6887d-108">PARAMETERS</span></span>

### <span data-ttu-id="6887d-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6887d-109">-CdnEndpoint</span></span>
<span data-ttu-id="6887d-110">Anger slut punkten som den här cmdleten uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="6887d-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="6887d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6887d-111">-DefaultProfile</span></span>
<span data-ttu-id="6887d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6887d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6887d-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6887d-113">-Confirm</span></span>
<span data-ttu-id="6887d-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6887d-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6887d-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6887d-115">-WhatIf</span></span>
<span data-ttu-id="6887d-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6887d-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6887d-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6887d-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6887d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6887d-118">CommonParameters</span></span>
<span data-ttu-id="6887d-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6887d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6887d-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6887d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6887d-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6887d-121">INPUTS</span></span>

### <span data-ttu-id="6887d-122">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="6887d-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="6887d-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6887d-123">OUTPUTS</span></span>

### <span data-ttu-id="6887d-124">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="6887d-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="6887d-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6887d-125">NOTES</span></span>

## <span data-ttu-id="6887d-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6887d-126">RELATED LINKS</span></span>

[<span data-ttu-id="6887d-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6887d-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="6887d-128">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6887d-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="6887d-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6887d-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="6887d-130">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6887d-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="6887d-131">Stopp-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6887d-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


