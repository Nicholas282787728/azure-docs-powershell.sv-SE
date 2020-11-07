---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
ms.openlocfilehash: c64f84c9f41dba29e54b14a69235bccd764ea750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756700"
---
# <span data-ttu-id="3a8db-101">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="3a8db-101">New-AzureRmCdnProfile</span></span>

## <span data-ttu-id="3a8db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3a8db-102">SYNOPSIS</span></span>
<span data-ttu-id="3a8db-103">Skapar en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="3a8db-103">Creates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a8db-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3a8db-104">SYNTAX</span></span>

```
New-AzureRmCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a8db-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3a8db-105">DESCRIPTION</span></span>
<span data-ttu-id="3a8db-106">Cmdleten **New-AzureRmCdnProfile** skapar en CDN-profil (Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="3a8db-106">The **New-AzureRmCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="3a8db-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3a8db-107">EXAMPLES</span></span>

## <span data-ttu-id="3a8db-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3a8db-108">PARAMETERS</span></span>

### <span data-ttu-id="3a8db-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a8db-109">-DefaultProfile</span></span>
<span data-ttu-id="3a8db-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3a8db-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a8db-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="3a8db-111">-Location</span></span>
<span data-ttu-id="3a8db-112">Anger resurs platsen för profilen.</span><span class="sxs-lookup"><span data-stu-id="3a8db-112">Specifies the resource location of the profile.</span></span>

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

### <span data-ttu-id="3a8db-113">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="3a8db-113">-ProfileName</span></span>
<span data-ttu-id="3a8db-114">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="3a8db-114">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="3a8db-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a8db-115">-ResourceGroupName</span></span>
<span data-ttu-id="3a8db-116">Anger namnet på den resurs grupp som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="3a8db-116">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="3a8db-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="3a8db-117">-Sku</span></span>
<span data-ttu-id="3a8db-118">Anger SKU för profilen.</span><span class="sxs-lookup"><span data-stu-id="3a8db-118">Specifies the SKU of the profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a8db-119">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3a8db-119">-Tag</span></span>
<span data-ttu-id="3a8db-120">De taggar som ska kopplas till Azure CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="3a8db-120">The tags to associate with the Azure CDN profile.</span></span>

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

### <span data-ttu-id="3a8db-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3a8db-121">-Confirm</span></span>
<span data-ttu-id="3a8db-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3a8db-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a8db-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a8db-123">-WhatIf</span></span>
<span data-ttu-id="3a8db-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3a8db-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a8db-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3a8db-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a8db-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a8db-126">CommonParameters</span></span>
<span data-ttu-id="3a8db-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a8db-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a8db-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a8db-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a8db-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3a8db-129">INPUTS</span></span>

### <span data-ttu-id="3a8db-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3a8db-130">System.String</span></span>

## <span data-ttu-id="3a8db-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3a8db-131">OUTPUTS</span></span>

### <span data-ttu-id="3a8db-132">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="3a8db-132">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="3a8db-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3a8db-133">NOTES</span></span>

## <span data-ttu-id="3a8db-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3a8db-134">RELATED LINKS</span></span>

[<span data-ttu-id="3a8db-135">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="3a8db-135">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="3a8db-136">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="3a8db-136">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="3a8db-137">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="3a8db-137">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


