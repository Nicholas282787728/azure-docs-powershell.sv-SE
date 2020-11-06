---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Start-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Start-AzureRmCdnEndpoint.md
ms.openlocfilehash: 742fe2795f16ed0a626e071520977ead66a491f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578439"
---
# <span data-ttu-id="dc67f-101">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc67f-101">Start-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="dc67f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc67f-102">SYNOPSIS</span></span>
<span data-ttu-id="dc67f-103">Startar en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="dc67f-103">Starts a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc67f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc67f-104">SYNTAX</span></span>

### <span data-ttu-id="dc67f-105">Parameter uppsättning för fält parametrar (standard)</span><span class="sxs-lookup"><span data-stu-id="dc67f-105">Parameter Set for fields parameters (Default)</span></span>
```
Start-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc67f-106">Parameter uppsättning för objekt parametrar</span><span class="sxs-lookup"><span data-stu-id="dc67f-106">Parameter Set for object parameters</span></span>
```
Start-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc67f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc67f-107">DESCRIPTION</span></span>
<span data-ttu-id="dc67f-108">Cmdleten **Start-AzureRmCdnEndpoint** startar en CDN-slutpunkt (innehåll).</span><span class="sxs-lookup"><span data-stu-id="dc67f-108">The **Start-AzureRmCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="dc67f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc67f-109">EXAMPLES</span></span>

## <span data-ttu-id="dc67f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc67f-110">PARAMETERS</span></span>

### <span data-ttu-id="dc67f-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc67f-111">-CdnEndpoint</span></span>
<span data-ttu-id="dc67f-112">Anger slut punkten som den här cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="dc67f-112">Specifies the endpoint that this cmdlet starts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc67f-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="dc67f-113">-EndpointName</span></span>
<span data-ttu-id="dc67f-114">Anger namnet på den slut punkt som cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="dc67f-114">Specifies the name of the endpoint that this cmdlet starts.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc67f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc67f-115">-PassThru</span></span>
<span data-ttu-id="dc67f-116">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="dc67f-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dc67f-117">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="dc67f-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dc67f-118">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="dc67f-118">-ProfileName</span></span>
<span data-ttu-id="dc67f-119">Anger namnet på den profil som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="dc67f-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc67f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc67f-120">-ResourceGroupName</span></span>
<span data-ttu-id="dc67f-121">Anger namnet på resurs gruppen som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="dc67f-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc67f-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dc67f-122">-Confirm</span></span>
<span data-ttu-id="dc67f-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dc67f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc67f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc67f-124">-WhatIf</span></span>
<span data-ttu-id="dc67f-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dc67f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc67f-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dc67f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc67f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc67f-127">-DefaultProfile</span></span>
<span data-ttu-id="dc67f-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dc67f-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc67f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc67f-129">CommonParameters</span></span>
<span data-ttu-id="dc67f-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc67f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc67f-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc67f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc67f-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc67f-132">INPUTS</span></span>

### <span data-ttu-id="dc67f-133">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc67f-133">PSEndpoint</span></span>
<span data-ttu-id="dc67f-134">Parametern ' CdnEndpoint ' godkänner värdet av typen ' PSEndpoint ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="dc67f-134">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="dc67f-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc67f-135">OUTPUTS</span></span>

### <span data-ttu-id="dc67f-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc67f-136">System.Boolean</span></span>

## <span data-ttu-id="dc67f-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc67f-137">NOTES</span></span>

## <span data-ttu-id="dc67f-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc67f-138">RELATED LINKS</span></span>

[<span data-ttu-id="dc67f-139">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc67f-139">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="dc67f-140">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc67f-140">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="dc67f-141">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc67f-141">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="dc67f-142">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc67f-142">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="dc67f-143">Stopp-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc67f-143">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


