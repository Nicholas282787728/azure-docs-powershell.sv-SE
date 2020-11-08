---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/start-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
ms.openlocfilehash: 85fc0f0687ed3b32492f42f753f67ba1e85a4656
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090553"
---
# <span data-ttu-id="ff9ce-101">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff9ce-101">Start-AzCdnEndpoint</span></span>

## <span data-ttu-id="ff9ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff9ce-102">SYNOPSIS</span></span>
<span data-ttu-id="ff9ce-103">Startar en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="ff9ce-103">Starts a CDN endpoint.</span></span>

## <span data-ttu-id="ff9ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff9ce-104">SYNTAX</span></span>

### <span data-ttu-id="ff9ce-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ff9ce-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff9ce-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff9ce-106">ByObjectParameterSet</span></span>
```
Start-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff9ce-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff9ce-107">DESCRIPTION</span></span>
<span data-ttu-id="ff9ce-108">Cmdleten **Start-AzCdnEndpoint** startar en CDN-slutpunkt (innehåll).</span><span class="sxs-lookup"><span data-stu-id="ff9ce-108">The **Start-AzCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="ff9ce-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff9ce-109">EXAMPLES</span></span>

## <span data-ttu-id="ff9ce-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff9ce-110">PARAMETERS</span></span>

### <span data-ttu-id="ff9ce-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff9ce-111">-CdnEndpoint</span></span>
<span data-ttu-id="ff9ce-112">Anger slut punkten som den här cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="ff9ce-112">Specifies the endpoint that this cmdlet starts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff9ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff9ce-113">-DefaultProfile</span></span>
<span data-ttu-id="ff9ce-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ff9ce-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff9ce-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ff9ce-115">-EndpointName</span></span>
<span data-ttu-id="ff9ce-116">Anger namnet på den slut punkt som cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="ff9ce-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff9ce-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff9ce-117">-PassThru</span></span>
<span data-ttu-id="ff9ce-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="ff9ce-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ff9ce-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="ff9ce-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff9ce-120">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="ff9ce-120">-ProfileName</span></span>
<span data-ttu-id="ff9ce-121">Anger namnet på den profil som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="ff9ce-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff9ce-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff9ce-122">-ResourceGroupName</span></span>
<span data-ttu-id="ff9ce-123">Anger namnet på resurs gruppen som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="ff9ce-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff9ce-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ff9ce-124">-Confirm</span></span>
<span data-ttu-id="ff9ce-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ff9ce-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff9ce-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff9ce-126">-WhatIf</span></span>
<span data-ttu-id="ff9ce-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ff9ce-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff9ce-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ff9ce-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff9ce-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff9ce-129">CommonParameters</span></span>
<span data-ttu-id="ff9ce-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff9ce-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff9ce-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff9ce-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff9ce-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff9ce-132">INPUTS</span></span>

### <span data-ttu-id="ff9ce-133">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff9ce-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="ff9ce-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ff9ce-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ff9ce-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff9ce-135">OUTPUTS</span></span>

### <span data-ttu-id="ff9ce-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ff9ce-136">System.Boolean</span></span>

## <span data-ttu-id="ff9ce-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff9ce-137">NOTES</span></span>

## <span data-ttu-id="ff9ce-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff9ce-138">RELATED LINKS</span></span>

[<span data-ttu-id="ff9ce-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff9ce-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="ff9ce-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff9ce-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="ff9ce-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff9ce-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="ff9ce-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff9ce-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="ff9ce-143">Stopp-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff9ce-143">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


