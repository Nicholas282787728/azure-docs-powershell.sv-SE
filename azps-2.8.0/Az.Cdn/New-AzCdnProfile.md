---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
ms.openlocfilehash: 7f62d12fbed217fa744ed5753c9234fb0e558caf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745304"
---
# <span data-ttu-id="bb241-101">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="bb241-101">New-AzCdnProfile</span></span>

## <span data-ttu-id="bb241-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bb241-102">SYNOPSIS</span></span>
<span data-ttu-id="bb241-103">Skapar en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="bb241-103">Creates a CDN profile.</span></span>

## <span data-ttu-id="bb241-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bb241-104">SYNTAX</span></span>

```
New-AzCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb241-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bb241-105">DESCRIPTION</span></span>
<span data-ttu-id="bb241-106">Cmdleten **New-AzCdnProfile** skapar en CDN-profil (Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="bb241-106">The **New-AzCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="bb241-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bb241-107">EXAMPLES</span></span>

## <span data-ttu-id="bb241-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bb241-108">PARAMETERS</span></span>

### <span data-ttu-id="bb241-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb241-109">-DefaultProfile</span></span>
<span data-ttu-id="bb241-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bb241-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb241-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="bb241-111">-Location</span></span>
<span data-ttu-id="bb241-112">Anger resurs platsen för profilen.</span><span class="sxs-lookup"><span data-stu-id="bb241-112">Specifies the resource location of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb241-113">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="bb241-113">-ProfileName</span></span>
<span data-ttu-id="bb241-114">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="bb241-114">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb241-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb241-115">-ResourceGroupName</span></span>
<span data-ttu-id="bb241-116">Anger namnet på den resurs grupp som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="bb241-116">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb241-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="bb241-117">-Sku</span></span>
<span data-ttu-id="bb241-118">Anger SKU för profilen.</span><span class="sxs-lookup"><span data-stu-id="bb241-118">Specifies the SKU of the profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn, Standard_Microsoft

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb241-119">-Tagg</span><span class="sxs-lookup"><span data-stu-id="bb241-119">-Tag</span></span>
<span data-ttu-id="bb241-120">De taggar som ska kopplas till Azure CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="bb241-120">The tags to associate with the Azure CDN profile.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb241-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bb241-121">-Confirm</span></span>
<span data-ttu-id="bb241-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bb241-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb241-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb241-123">-WhatIf</span></span>
<span data-ttu-id="bb241-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bb241-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb241-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bb241-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb241-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb241-126">CommonParameters</span></span>
<span data-ttu-id="bb241-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb241-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb241-128">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb241-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb241-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bb241-129">INPUTS</span></span>

### <span data-ttu-id="bb241-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bb241-130">System.String</span></span>

## <span data-ttu-id="bb241-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bb241-131">OUTPUTS</span></span>

### <span data-ttu-id="bb241-132">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="bb241-132">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="bb241-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bb241-133">NOTES</span></span>

## <span data-ttu-id="bb241-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bb241-134">RELATED LINKS</span></span>

[<span data-ttu-id="bb241-135">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="bb241-135">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="bb241-136">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="bb241-136">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="bb241-137">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="bb241-137">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


