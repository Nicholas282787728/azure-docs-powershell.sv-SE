---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
ms.openlocfilehash: 83229b9251e7cbbbe4bd17d73004b9bc64800511
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578436"
---
# <span data-ttu-id="2c3c2-101">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c3c2-101">Stop-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="2c3c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c3c2-102">SYNOPSIS</span></span>
<span data-ttu-id="2c3c2-103">Stoppar CDN-slutpunkten.</span><span class="sxs-lookup"><span data-stu-id="2c3c2-103">Stops the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c3c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c3c2-104">SYNTAX</span></span>

### <span data-ttu-id="2c3c2-105">Parameter uppsättning för fält parametrar (standard)</span><span class="sxs-lookup"><span data-stu-id="2c3c2-105">Parameter Set for fields parameters (Default)</span></span>
```
Stop-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c3c2-106">Parameter uppsättning för objekt parametrar</span><span class="sxs-lookup"><span data-stu-id="2c3c2-106">Parameter Set for object parameters</span></span>
```
Stop-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c3c2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c3c2-107">DESCRIPTION</span></span>
<span data-ttu-id="2c3c2-108">Cmdleten **Stop-AzureRmCdnEndpoint** stoppar slut punkten för Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="2c3c2-108">The **Stop-AzureRmCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="2c3c2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c3c2-109">EXAMPLES</span></span>

## <span data-ttu-id="2c3c2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c3c2-110">PARAMETERS</span></span>

### <span data-ttu-id="2c3c2-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c3c2-111">-CdnEndpoint</span></span>
<span data-ttu-id="2c3c2-112">Anger det slut punkts objekt som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="2c3c2-112">Specifies the endpoint object that this cmdlet stops.</span></span>

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

### <span data-ttu-id="2c3c2-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2c3c2-113">-EndpointName</span></span>
<span data-ttu-id="2c3c2-114">Anger namnet på slut punkten som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="2c3c2-114">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="2c3c2-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c3c2-115">-PassThru</span></span>
<span data-ttu-id="2c3c2-116">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="2c3c2-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2c3c2-117">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="2c3c2-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2c3c2-118">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="2c3c2-118">-ProfileName</span></span>
<span data-ttu-id="2c3c2-119">Anger namnet på den profil som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="2c3c2-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="2c3c2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c3c2-120">-ResourceGroupName</span></span>
<span data-ttu-id="2c3c2-121">Anger namnet på resurs gruppen som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="2c3c2-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="2c3c2-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2c3c2-122">-Confirm</span></span>
<span data-ttu-id="2c3c2-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2c3c2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c3c2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c3c2-124">-WhatIf</span></span>
<span data-ttu-id="2c3c2-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2c3c2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c3c2-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2c3c2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c3c2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c3c2-127">-DefaultProfile</span></span>
<span data-ttu-id="2c3c2-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2c3c2-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c3c2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c3c2-129">CommonParameters</span></span>
<span data-ttu-id="2c3c2-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c3c2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c3c2-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c3c2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c3c2-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c3c2-132">INPUTS</span></span>

### <span data-ttu-id="2c3c2-133">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c3c2-133">PSEndpoint</span></span>
<span data-ttu-id="2c3c2-134">Parametern ' CdnEndpoint ' godkänner värdet av typen ' PSEndpoint ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="2c3c2-134">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="2c3c2-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c3c2-135">OUTPUTS</span></span>

### <span data-ttu-id="2c3c2-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2c3c2-136">System.Boolean</span></span>

## <span data-ttu-id="2c3c2-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c3c2-137">NOTES</span></span>

## <span data-ttu-id="2c3c2-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c3c2-138">RELATED LINKS</span></span>

[<span data-ttu-id="2c3c2-139">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c3c2-139">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="2c3c2-140">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c3c2-140">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="2c3c2-141">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c3c2-141">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="2c3c2-142">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c3c2-142">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="2c3c2-143">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c3c2-143">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)


