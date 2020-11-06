---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
ms.openlocfilehash: 5423844d7f466a827f3a452a05cf3999236198d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574388"
---
# <span data-ttu-id="c0ec5-101">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c0ec5-101">New-AzureRmCdnProfile</span></span>

## <span data-ttu-id="c0ec5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0ec5-102">SYNOPSIS</span></span>
<span data-ttu-id="c0ec5-103">Skapar en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="c0ec5-103">Creates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0ec5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0ec5-104">SYNTAX</span></span>

```
New-AzureRmCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0ec5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0ec5-105">DESCRIPTION</span></span>
<span data-ttu-id="c0ec5-106">Cmdleten **New-AzureRmCdnProfile** skapar en CDN-profil (Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="c0ec5-106">The **New-AzureRmCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="c0ec5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0ec5-107">EXAMPLES</span></span>

## <span data-ttu-id="c0ec5-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0ec5-108">PARAMETERS</span></span>

### <span data-ttu-id="c0ec5-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0ec5-109">-DefaultProfile</span></span>
<span data-ttu-id="c0ec5-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c0ec5-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0ec5-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="c0ec5-111">-Location</span></span>
<span data-ttu-id="c0ec5-112">Anger resurs platsen för profilen.</span><span class="sxs-lookup"><span data-stu-id="c0ec5-112">Specifies the resource location of the profile.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0ec5-113">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="c0ec5-113">-ProfileName</span></span>
<span data-ttu-id="c0ec5-114">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="c0ec5-114">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0ec5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0ec5-115">-ResourceGroupName</span></span>
<span data-ttu-id="c0ec5-116">Anger namnet på den resurs grupp som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="c0ec5-116">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0ec5-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="c0ec5-117">-Sku</span></span>
<span data-ttu-id="c0ec5-118">Anger SKU för profilen.</span><span class="sxs-lookup"><span data-stu-id="c0ec5-118">Specifies the SKU of the profile.</span></span>

```yaml
Type: PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0ec5-119">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c0ec5-119">-Tag</span></span>
<span data-ttu-id="c0ec5-120">De taggar som ska kopplas till Azure CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="c0ec5-120">The tags to associate with the Azure CDN profile.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0ec5-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c0ec5-121">-Confirm</span></span>
<span data-ttu-id="c0ec5-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c0ec5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0ec5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0ec5-123">-WhatIf</span></span>
<span data-ttu-id="c0ec5-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c0ec5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0ec5-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c0ec5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0ec5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0ec5-126">CommonParameters</span></span>
<span data-ttu-id="c0ec5-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0ec5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0ec5-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0ec5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0ec5-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0ec5-129">INPUTS</span></span>

### <span data-ttu-id="c0ec5-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="c0ec5-130">None</span></span>
<span data-ttu-id="c0ec5-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c0ec5-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c0ec5-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0ec5-132">OUTPUTS</span></span>

### <span data-ttu-id="c0ec5-133">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="c0ec5-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="c0ec5-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0ec5-134">NOTES</span></span>

## <span data-ttu-id="c0ec5-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0ec5-135">RELATED LINKS</span></span>

[<span data-ttu-id="c0ec5-136">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c0ec5-136">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="c0ec5-137">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c0ec5-137">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="c0ec5-138">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c0ec5-138">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


