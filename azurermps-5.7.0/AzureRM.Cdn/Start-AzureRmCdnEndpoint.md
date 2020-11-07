---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/start-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Start-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Start-AzureRmCdnEndpoint.md
ms.openlocfilehash: cfa0eb8506230fe14b9ddf48bcd7562acf45a590
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755990"
---
# <span data-ttu-id="5e1c5-101">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5e1c5-101">Start-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="5e1c5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5e1c5-102">SYNOPSIS</span></span>
<span data-ttu-id="5e1c5-103">Startar en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="5e1c5-103">Starts a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e1c5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5e1c5-104">SYNTAX</span></span>

### <span data-ttu-id="5e1c5-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5e1c5-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e1c5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e1c5-106">ByObjectParameterSet</span></span>
```
Start-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e1c5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5e1c5-107">DESCRIPTION</span></span>
<span data-ttu-id="5e1c5-108">Cmdleten **Start-AzureRmCdnEndpoint** startar en CDN-slutpunkt (innehåll).</span><span class="sxs-lookup"><span data-stu-id="5e1c5-108">The **Start-AzureRmCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="5e1c5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5e1c5-109">EXAMPLES</span></span>

## <span data-ttu-id="5e1c5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5e1c5-110">PARAMETERS</span></span>

### <span data-ttu-id="5e1c5-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5e1c5-111">-CdnEndpoint</span></span>
<span data-ttu-id="5e1c5-112">Anger slut punkten som den här cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="5e1c5-112">Specifies the endpoint that this cmdlet starts.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e1c5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e1c5-113">-DefaultProfile</span></span>
<span data-ttu-id="5e1c5-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5e1c5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e1c5-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="5e1c5-115">-EndpointName</span></span>
<span data-ttu-id="5e1c5-116">Anger namnet på den slut punkt som cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="5e1c5-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e1c5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e1c5-117">-PassThru</span></span>
<span data-ttu-id="5e1c5-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="5e1c5-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5e1c5-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="5e1c5-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e1c5-120">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="5e1c5-120">-ProfileName</span></span>
<span data-ttu-id="5e1c5-121">Anger namnet på den profil som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="5e1c5-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e1c5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e1c5-122">-ResourceGroupName</span></span>
<span data-ttu-id="5e1c5-123">Anger namnet på resurs gruppen som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="5e1c5-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e1c5-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5e1c5-124">-Confirm</span></span>
<span data-ttu-id="5e1c5-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5e1c5-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e1c5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e1c5-126">-WhatIf</span></span>
<span data-ttu-id="5e1c5-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5e1c5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e1c5-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5e1c5-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e1c5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e1c5-129">CommonParameters</span></span>
<span data-ttu-id="5e1c5-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e1c5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e1c5-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e1c5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e1c5-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5e1c5-132">INPUTS</span></span>

### <span data-ttu-id="5e1c5-133">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="5e1c5-133">PSEndpoint</span></span>
<span data-ttu-id="5e1c5-134">Parametern ' CdnEndpoint ' godkänner värdet av typen ' PSEndpoint ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="5e1c5-134">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="5e1c5-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5e1c5-135">OUTPUTS</span></span>

### <span data-ttu-id="5e1c5-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e1c5-136">System.Boolean</span></span>

## <span data-ttu-id="5e1c5-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5e1c5-137">NOTES</span></span>

## <span data-ttu-id="5e1c5-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5e1c5-138">RELATED LINKS</span></span>

[<span data-ttu-id="5e1c5-139">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5e1c5-139">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5e1c5-140">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5e1c5-140">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5e1c5-141">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5e1c5-141">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5e1c5-142">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5e1c5-142">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5e1c5-143">Stopp-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5e1c5-143">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


