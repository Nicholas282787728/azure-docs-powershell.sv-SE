---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 8c6e3629d4ac6e8592370393b94727234a6eb12a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574382"
---
# <span data-ttu-id="7fd48-101">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7fd48-101">Remove-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="7fd48-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7fd48-102">SYNOPSIS</span></span>
<span data-ttu-id="7fd48-103">Tar bort en egen domän.</span><span class="sxs-lookup"><span data-stu-id="7fd48-103">Removes a custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fd48-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7fd48-104">SYNTAX</span></span>

### <span data-ttu-id="7fd48-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7fd48-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7fd48-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fd48-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fd48-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7fd48-107">DESCRIPTION</span></span>
<span data-ttu-id="7fd48-108">Cmdleten **Remove-AzureRmCdnCustomDomain** tar bort den anpassade domänen från en slut punkt för Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="7fd48-108">The **Remove-AzureRmCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="7fd48-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7fd48-109">EXAMPLES</span></span>

## <span data-ttu-id="7fd48-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7fd48-110">PARAMETERS</span></span>

### <span data-ttu-id="7fd48-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7fd48-111">-CdnCustomDomain</span></span>
<span data-ttu-id="7fd48-112">Anger den anpassade domän som ska tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fd48-112">Specifies the custom domain that this cmdlet removes.</span></span>

```yaml
Type: PSCustomDomain
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fd48-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="7fd48-113">-CustomDomainName</span></span>
<span data-ttu-id="7fd48-114">Anger resurs namnet på den anpassade domän där denna cmdlet ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="7fd48-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7fd48-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fd48-115">-DefaultProfile</span></span>
<span data-ttu-id="7fd48-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7fd48-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7fd48-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7fd48-117">-EndpointName</span></span>
<span data-ttu-id="7fd48-118">Anger namnet på den slut punkt från vilken denna cmdlet tar bort en egen domän.</span><span class="sxs-lookup"><span data-stu-id="7fd48-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="7fd48-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7fd48-119">-PassThru</span></span>
<span data-ttu-id="7fd48-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="7fd48-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7fd48-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="7fd48-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7fd48-122">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="7fd48-122">-ProfileName</span></span>
<span data-ttu-id="7fd48-123">Anger namnet på den profil som cmdleten tar bort en egen domän från.</span><span class="sxs-lookup"><span data-stu-id="7fd48-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="7fd48-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fd48-124">-ResourceGroupName</span></span>
<span data-ttu-id="7fd48-125">Anger namnet på den resurs grupp från vilken denna cmdlet tar bort en egen domän.</span><span class="sxs-lookup"><span data-stu-id="7fd48-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="7fd48-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7fd48-126">-Confirm</span></span>
<span data-ttu-id="7fd48-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7fd48-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fd48-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fd48-128">-WhatIf</span></span>
<span data-ttu-id="7fd48-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7fd48-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fd48-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7fd48-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fd48-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fd48-131">CommonParameters</span></span>
<span data-ttu-id="7fd48-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fd48-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fd48-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fd48-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fd48-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7fd48-134">INPUTS</span></span>

### <span data-ttu-id="7fd48-135">PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7fd48-135">PSCustomDomain</span></span>
<span data-ttu-id="7fd48-136">Parametern ' CdnCustomDomain ' godkänner värdet av typen ' PSCustomDomain ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="7fd48-136">Parameter 'CdnCustomDomain' accepts value of type 'PSCustomDomain' from the pipeline</span></span>

## <span data-ttu-id="7fd48-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7fd48-137">OUTPUTS</span></span>

### <span data-ttu-id="7fd48-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7fd48-138">System.Boolean</span></span>

## <span data-ttu-id="7fd48-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7fd48-139">NOTES</span></span>

## <span data-ttu-id="7fd48-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7fd48-140">RELATED LINKS</span></span>

[<span data-ttu-id="7fd48-141">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7fd48-141">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="7fd48-142">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7fd48-142">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="7fd48-143">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7fd48-143">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


