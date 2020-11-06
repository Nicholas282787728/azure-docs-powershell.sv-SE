---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
ms.openlocfilehash: 70a6e57b45e1703b06343cb66d5b83b526b55063
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578448"
---
# <span data-ttu-id="7b66d-101">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7b66d-101">Set-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="7b66d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7b66d-102">SYNOPSIS</span></span>
<span data-ttu-id="7b66d-103">Uppdaterar en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="7b66d-103">Updates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b66d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7b66d-104">SYNTAX</span></span>

```
Set-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b66d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7b66d-105">DESCRIPTION</span></span>
<span data-ttu-id="7b66d-106">Cmdleten **set-AzureRmCdnEndpoint** uppdaterar en CDN-slutpunkt (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="7b66d-106">The **Set-AzureRmCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="7b66d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7b66d-107">EXAMPLES</span></span>

## <span data-ttu-id="7b66d-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7b66d-108">PARAMETERS</span></span>

### <span data-ttu-id="7b66d-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7b66d-109">-CdnEndpoint</span></span>
<span data-ttu-id="7b66d-110">Anger slut punkten som den här cmdleten uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="7b66d-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="7b66d-111">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7b66d-111">-Confirm</span></span>
<span data-ttu-id="7b66d-112">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7b66d-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b66d-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b66d-113">-WhatIf</span></span>
<span data-ttu-id="7b66d-114">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7b66d-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b66d-115">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7b66d-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b66d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b66d-116">-DefaultProfile</span></span>
<span data-ttu-id="7b66d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7b66d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b66d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b66d-118">CommonParameters</span></span>
<span data-ttu-id="7b66d-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b66d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b66d-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b66d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b66d-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7b66d-121">INPUTS</span></span>

### <span data-ttu-id="7b66d-122">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7b66d-122">PSEndpoint</span></span>
<span data-ttu-id="7b66d-123">Parametern ' CdnEndpoint ' godkänner värdet av typen ' PSEndpoint ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="7b66d-123">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="7b66d-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7b66d-124">OUTPUTS</span></span>

### <span data-ttu-id="7b66d-125">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7b66d-125">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="7b66d-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7b66d-126">NOTES</span></span>

## <span data-ttu-id="7b66d-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7b66d-127">RELATED LINKS</span></span>

[<span data-ttu-id="7b66d-128">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7b66d-128">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="7b66d-129">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7b66d-129">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="7b66d-130">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7b66d-130">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="7b66d-131">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7b66d-131">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="7b66d-132">Stopp-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7b66d-132">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


