---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/stop-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
ms.openlocfilehash: e1afa87d1ab21222987a4eeecf68a3786934ef57
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103050"
---
# <span data-ttu-id="683df-101">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="683df-101">Stop-AzCdnEndpoint</span></span>

## <span data-ttu-id="683df-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="683df-102">SYNOPSIS</span></span>
<span data-ttu-id="683df-103">Stoppar CDN-slutpunkten.</span><span class="sxs-lookup"><span data-stu-id="683df-103">Stops the CDN endpoint.</span></span>

## <span data-ttu-id="683df-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="683df-104">SYNTAX</span></span>

### <span data-ttu-id="683df-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="683df-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="683df-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="683df-106">ByObjectParameterSet</span></span>
```
Stop-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="683df-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="683df-107">DESCRIPTION</span></span>
<span data-ttu-id="683df-108">Cmdleten **Stop-AzCdnEndpoint** stoppar slut punkten för Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="683df-108">The **Stop-AzCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="683df-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="683df-109">EXAMPLES</span></span>

## <span data-ttu-id="683df-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="683df-110">PARAMETERS</span></span>

### <span data-ttu-id="683df-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="683df-111">-CdnEndpoint</span></span>
<span data-ttu-id="683df-112">Anger det slut punkts objekt som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="683df-112">Specifies the endpoint object that this cmdlet stops.</span></span>

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

### <span data-ttu-id="683df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="683df-113">-DefaultProfile</span></span>
<span data-ttu-id="683df-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="683df-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="683df-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="683df-115">-EndpointName</span></span>
<span data-ttu-id="683df-116">Anger namnet på slut punkten som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="683df-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="683df-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="683df-117">-PassThru</span></span>
<span data-ttu-id="683df-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="683df-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="683df-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="683df-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="683df-120">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="683df-120">-ProfileName</span></span>
<span data-ttu-id="683df-121">Anger namnet på den profil som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="683df-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="683df-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="683df-122">-ResourceGroupName</span></span>
<span data-ttu-id="683df-123">Anger namnet på resurs gruppen som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="683df-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="683df-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="683df-124">-Confirm</span></span>
<span data-ttu-id="683df-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="683df-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="683df-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="683df-126">-WhatIf</span></span>
<span data-ttu-id="683df-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="683df-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="683df-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="683df-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="683df-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="683df-129">CommonParameters</span></span>
<span data-ttu-id="683df-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="683df-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="683df-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="683df-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="683df-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="683df-132">INPUTS</span></span>

### <span data-ttu-id="683df-133">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="683df-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="683df-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="683df-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="683df-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="683df-135">OUTPUTS</span></span>

### <span data-ttu-id="683df-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="683df-136">System.Boolean</span></span>

## <span data-ttu-id="683df-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="683df-137">NOTES</span></span>

## <span data-ttu-id="683df-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="683df-138">RELATED LINKS</span></span>

[<span data-ttu-id="683df-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="683df-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="683df-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="683df-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="683df-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="683df-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="683df-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="683df-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="683df-143">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="683df-143">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)


