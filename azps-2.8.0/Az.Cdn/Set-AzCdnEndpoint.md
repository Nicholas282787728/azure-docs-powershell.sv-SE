---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: c84b91e70d428a7ba05aa3766bf1a63840b6ffa4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745295"
---
# <span data-ttu-id="8c41c-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c41c-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="8c41c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8c41c-102">SYNOPSIS</span></span>
<span data-ttu-id="8c41c-103">Uppdaterar en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="8c41c-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="8c41c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8c41c-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c41c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8c41c-105">DESCRIPTION</span></span>
<span data-ttu-id="8c41c-106">Cmdleten **set-AzCdnEndpoint** uppdaterar en CDN-slutpunkt (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="8c41c-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="8c41c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8c41c-107">EXAMPLES</span></span>

## <span data-ttu-id="8c41c-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8c41c-108">PARAMETERS</span></span>

### <span data-ttu-id="8c41c-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c41c-109">-CdnEndpoint</span></span>
<span data-ttu-id="8c41c-110">Anger slut punkten som den här cmdleten uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="8c41c-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="8c41c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c41c-111">-DefaultProfile</span></span>
<span data-ttu-id="8c41c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8c41c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c41c-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8c41c-113">-Confirm</span></span>
<span data-ttu-id="8c41c-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8c41c-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c41c-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c41c-115">-WhatIf</span></span>
<span data-ttu-id="8c41c-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8c41c-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c41c-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8c41c-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c41c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c41c-118">CommonParameters</span></span>
<span data-ttu-id="8c41c-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c41c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c41c-120">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c41c-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c41c-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8c41c-121">INPUTS</span></span>

### <span data-ttu-id="8c41c-122">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c41c-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="8c41c-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8c41c-123">OUTPUTS</span></span>

### <span data-ttu-id="8c41c-124">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c41c-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="8c41c-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8c41c-125">NOTES</span></span>

## <span data-ttu-id="8c41c-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8c41c-126">RELATED LINKS</span></span>

[<span data-ttu-id="8c41c-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c41c-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="8c41c-128">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c41c-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="8c41c-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c41c-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="8c41c-130">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c41c-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="8c41c-131">Stopp-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c41c-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


