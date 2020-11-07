---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
ms.openlocfilehash: 76c1f255b2d8dc3275ec3a691337019a7fd1e3e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757719"
---
# <span data-ttu-id="0a877-101">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0a877-101">Remove-AzureRmCdnProfile</span></span>

## <span data-ttu-id="0a877-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0a877-102">SYNOPSIS</span></span>
<span data-ttu-id="0a877-103">Tar bort en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="0a877-103">Removes a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a877-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0a877-104">SYNTAX</span></span>

### <span data-ttu-id="0a877-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a877-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a877-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a877-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a877-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0a877-107">DESCRIPTION</span></span>
<span data-ttu-id="0a877-108">Cmdleten **Remove-AzureRmCdnProfile** tar bort en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="0a877-108">The **Remove-AzureRmCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="0a877-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0a877-109">EXAMPLES</span></span>

## <span data-ttu-id="0a877-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0a877-110">PARAMETERS</span></span>

### <span data-ttu-id="0a877-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="0a877-111">-CdnProfile</span></span>
<span data-ttu-id="0a877-112">Anger den profil som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="0a877-112">Specifies the profile that this cmdlet removes.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a877-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a877-113">-DefaultProfile</span></span>
<span data-ttu-id="0a877-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0a877-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a877-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0a877-115">-Force</span></span>
<span data-ttu-id="0a877-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="0a877-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0a877-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a877-117">-PassThru</span></span>
<span data-ttu-id="0a877-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="0a877-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0a877-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="0a877-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0a877-120">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="0a877-120">-ProfileName</span></span>
<span data-ttu-id="0a877-121">Anger namnet på den profil som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="0a877-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0a877-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a877-122">-ResourceGroupName</span></span>
<span data-ttu-id="0a877-123">Anger namnet på den resurs grupp som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="0a877-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="0a877-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0a877-124">-Confirm</span></span>
<span data-ttu-id="0a877-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0a877-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a877-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a877-126">-WhatIf</span></span>
<span data-ttu-id="0a877-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0a877-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a877-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0a877-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a877-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a877-129">CommonParameters</span></span>
<span data-ttu-id="0a877-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a877-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a877-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a877-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a877-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0a877-132">INPUTS</span></span>

### <span data-ttu-id="0a877-133">PSProfile</span><span class="sxs-lookup"><span data-stu-id="0a877-133">PSProfile</span></span>
<span data-ttu-id="0a877-134">Parametern ' CdnProfile ' godkänner värdet av typen ' PSProfile ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="0a877-134">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="0a877-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0a877-135">OUTPUTS</span></span>

### <span data-ttu-id="0a877-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0a877-136">System.Boolean</span></span>

## <span data-ttu-id="0a877-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0a877-137">NOTES</span></span>

## <span data-ttu-id="0a877-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0a877-138">RELATED LINKS</span></span>

[<span data-ttu-id="0a877-139">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0a877-139">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="0a877-140">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0a877-140">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="0a877-141">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0a877-141">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


