---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/stop-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
ms.openlocfilehash: 20206ebf99d597a2961804bf3062cd4c049f8017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756701"
---
# <span data-ttu-id="b7706-101">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7706-101">Stop-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="b7706-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b7706-102">SYNOPSIS</span></span>
<span data-ttu-id="b7706-103">Stoppar CDN-slutpunkten.</span><span class="sxs-lookup"><span data-stu-id="b7706-103">Stops the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7706-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b7706-104">SYNTAX</span></span>

### <span data-ttu-id="b7706-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b7706-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7706-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7706-106">ByObjectParameterSet</span></span>
```
Stop-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7706-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b7706-107">DESCRIPTION</span></span>
<span data-ttu-id="b7706-108">Cmdleten **Stop-AzureRmCdnEndpoint** stoppar slut punkten för Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="b7706-108">The **Stop-AzureRmCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="b7706-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b7706-109">EXAMPLES</span></span>

## <span data-ttu-id="b7706-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b7706-110">PARAMETERS</span></span>

### <span data-ttu-id="b7706-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7706-111">-CdnEndpoint</span></span>
<span data-ttu-id="b7706-112">Anger det slut punkts objekt som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="b7706-112">Specifies the endpoint object that this cmdlet stops.</span></span>

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

### <span data-ttu-id="b7706-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7706-113">-DefaultProfile</span></span>
<span data-ttu-id="b7706-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b7706-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7706-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b7706-115">-EndpointName</span></span>
<span data-ttu-id="b7706-116">Anger namnet på slut punkten som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="b7706-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="b7706-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7706-117">-PassThru</span></span>
<span data-ttu-id="b7706-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="b7706-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b7706-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="b7706-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b7706-120">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="b7706-120">-ProfileName</span></span>
<span data-ttu-id="b7706-121">Anger namnet på den profil som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="b7706-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="b7706-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7706-122">-ResourceGroupName</span></span>
<span data-ttu-id="b7706-123">Anger namnet på resurs gruppen som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="b7706-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="b7706-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b7706-124">-Confirm</span></span>
<span data-ttu-id="b7706-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b7706-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7706-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7706-126">-WhatIf</span></span>
<span data-ttu-id="b7706-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b7706-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7706-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b7706-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7706-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7706-129">CommonParameters</span></span>
<span data-ttu-id="b7706-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7706-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7706-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7706-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7706-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b7706-132">INPUTS</span></span>

### <span data-ttu-id="b7706-133">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7706-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="b7706-134">Parametrar: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b7706-134">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="b7706-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b7706-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b7706-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b7706-136">OUTPUTS</span></span>

### <span data-ttu-id="b7706-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b7706-137">System.Boolean</span></span>

## <span data-ttu-id="b7706-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b7706-138">NOTES</span></span>

## <span data-ttu-id="b7706-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b7706-139">RELATED LINKS</span></span>

[<span data-ttu-id="b7706-140">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7706-140">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="b7706-141">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7706-141">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="b7706-142">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7706-142">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="b7706-143">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7706-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="b7706-144">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7706-144">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)


