---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
ms.openlocfilehash: 8748806346baa4f84550d15749e7792ae928ad34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576629"
---
# <span data-ttu-id="f48a7-101">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f48a7-101">Remove-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="f48a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f48a7-102">SYNOPSIS</span></span>
<span data-ttu-id="f48a7-103">Tar bort en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="f48a7-103">Removes a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f48a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f48a7-104">SYNTAX</span></span>

### <span data-ttu-id="f48a7-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="f48a7-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f48a7-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f48a7-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f48a7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f48a7-107">DESCRIPTION</span></span>
<span data-ttu-id="f48a7-108">Cmdleten **Remove-AzureRmCdnEndpoint** tar bort en slut punkt för Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="f48a7-108">The **Remove-AzureRmCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="f48a7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f48a7-109">EXAMPLES</span></span>

## <span data-ttu-id="f48a7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f48a7-110">PARAMETERS</span></span>

### <span data-ttu-id="f48a7-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f48a7-111">-CdnEndpoint</span></span>
<span data-ttu-id="f48a7-112">Anger slut punkten som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="f48a7-112">Specifies the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f48a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f48a7-113">-DefaultProfile</span></span>
<span data-ttu-id="f48a7-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f48a7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f48a7-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f48a7-115">-EndpointName</span></span>
<span data-ttu-id="f48a7-116">Anger namnet på den slut punkt som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="f48a7-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f48a7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f48a7-117">-Force</span></span>
<span data-ttu-id="f48a7-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f48a7-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f48a7-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f48a7-119">-PassThru</span></span>
<span data-ttu-id="f48a7-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="f48a7-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f48a7-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="f48a7-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f48a7-122">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="f48a7-122">-ProfileName</span></span>
<span data-ttu-id="f48a7-123">Anger namnet på den profil som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="f48a7-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="f48a7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f48a7-124">-ResourceGroupName</span></span>
<span data-ttu-id="f48a7-125">Anger namnet på resurs gruppen som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="f48a7-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="f48a7-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f48a7-126">-Confirm</span></span>
<span data-ttu-id="f48a7-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f48a7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f48a7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f48a7-128">-WhatIf</span></span>
<span data-ttu-id="f48a7-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f48a7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f48a7-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f48a7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f48a7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f48a7-131">CommonParameters</span></span>
<span data-ttu-id="f48a7-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f48a7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f48a7-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f48a7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f48a7-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f48a7-134">INPUTS</span></span>

### <span data-ttu-id="f48a7-135">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="f48a7-135">PSEndpoint</span></span>
<span data-ttu-id="f48a7-136">Parametern ' CdnEndpoint ' godkänner värdet av typen ' PSEndpoint ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f48a7-136">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="f48a7-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f48a7-137">OUTPUTS</span></span>

### <span data-ttu-id="f48a7-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f48a7-138">System.Boolean</span></span>

## <span data-ttu-id="f48a7-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f48a7-139">NOTES</span></span>

## <span data-ttu-id="f48a7-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f48a7-140">RELATED LINKS</span></span>

[<span data-ttu-id="f48a7-141">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f48a7-141">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="f48a7-142">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f48a7-142">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="f48a7-143">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f48a7-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="f48a7-144">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f48a7-144">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="f48a7-145">Stopp-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f48a7-145">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


