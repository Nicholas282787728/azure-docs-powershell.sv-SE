---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
ms.openlocfilehash: 0c39e6ee26faffc9c12e2fc3b5f00ccaadfa9389
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578951"
---
# <span data-ttu-id="fd491-101">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="fd491-101">Remove-AzureRmCdnProfile</span></span>

## <span data-ttu-id="fd491-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fd491-102">SYNOPSIS</span></span>
<span data-ttu-id="fd491-103">Tar bort en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="fd491-103">Removes a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd491-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fd491-104">SYNTAX</span></span>

### <span data-ttu-id="fd491-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd491-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd491-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd491-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd491-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fd491-107">DESCRIPTION</span></span>
<span data-ttu-id="fd491-108">Cmdleten **Remove-AzureRmCdnProfile** tar bort en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="fd491-108">The **Remove-AzureRmCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="fd491-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fd491-109">EXAMPLES</span></span>

## <span data-ttu-id="fd491-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fd491-110">PARAMETERS</span></span>

### <span data-ttu-id="fd491-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="fd491-111">-CdnProfile</span></span>
<span data-ttu-id="fd491-112">Anger den profil som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="fd491-112">Specifies the profile that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd491-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd491-113">-DefaultProfile</span></span>
<span data-ttu-id="fd491-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fd491-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd491-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fd491-115">-Force</span></span>
<span data-ttu-id="fd491-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="fd491-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd491-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd491-117">-PassThru</span></span>
<span data-ttu-id="fd491-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="fd491-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fd491-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="fd491-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fd491-120">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="fd491-120">-ProfileName</span></span>
<span data-ttu-id="fd491-121">Anger namnet på den profil som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="fd491-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fd491-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd491-122">-ResourceGroupName</span></span>
<span data-ttu-id="fd491-123">Anger namnet på den resurs grupp som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="fd491-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="fd491-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fd491-124">-Confirm</span></span>
<span data-ttu-id="fd491-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fd491-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd491-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd491-126">-WhatIf</span></span>
<span data-ttu-id="fd491-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fd491-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd491-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fd491-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd491-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd491-129">CommonParameters</span></span>
<span data-ttu-id="fd491-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd491-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd491-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd491-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd491-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fd491-132">INPUTS</span></span>

### <span data-ttu-id="fd491-133">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="fd491-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="fd491-134">Parametrar: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fd491-134">Parameters: CdnProfile (ByValue)</span></span>

### <span data-ttu-id="fd491-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fd491-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fd491-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fd491-136">OUTPUTS</span></span>

### <span data-ttu-id="fd491-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd491-137">System.Boolean</span></span>

## <span data-ttu-id="fd491-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fd491-138">NOTES</span></span>

## <span data-ttu-id="fd491-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fd491-139">RELATED LINKS</span></span>

[<span data-ttu-id="fd491-140">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="fd491-140">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="fd491-141">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="fd491-141">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="fd491-142">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="fd491-142">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


