---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
ms.openlocfilehash: 6b8a5d9bd25c6f79cbfd70c509c9683b80453fe9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745299"
---
# <span data-ttu-id="3f55b-101">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="3f55b-101">Remove-AzCdnProfile</span></span>

## <span data-ttu-id="3f55b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f55b-102">SYNOPSIS</span></span>
<span data-ttu-id="3f55b-103">Tar bort en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="3f55b-103">Removes a CDN profile.</span></span>

## <span data-ttu-id="3f55b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f55b-104">SYNTAX</span></span>

### <span data-ttu-id="3f55b-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f55b-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f55b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f55b-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f55b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f55b-107">DESCRIPTION</span></span>
<span data-ttu-id="3f55b-108">Cmdleten **Remove-AzCdnProfile** tar bort en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="3f55b-108">The **Remove-AzCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="3f55b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f55b-109">EXAMPLES</span></span>

## <span data-ttu-id="3f55b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f55b-110">PARAMETERS</span></span>

### <span data-ttu-id="3f55b-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="3f55b-111">-CdnProfile</span></span>
<span data-ttu-id="3f55b-112">Anger den profil som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="3f55b-112">Specifies the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3f55b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f55b-113">-DefaultProfile</span></span>
<span data-ttu-id="3f55b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3f55b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f55b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3f55b-115">-Force</span></span>
<span data-ttu-id="3f55b-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3f55b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3f55b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f55b-117">-PassThru</span></span>
<span data-ttu-id="3f55b-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="3f55b-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3f55b-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="3f55b-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3f55b-120">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="3f55b-120">-ProfileName</span></span>
<span data-ttu-id="3f55b-121">Anger namnet på den profil som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="3f55b-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3f55b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f55b-122">-ResourceGroupName</span></span>
<span data-ttu-id="3f55b-123">Anger namnet på den resurs grupp som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="3f55b-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="3f55b-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3f55b-124">-Confirm</span></span>
<span data-ttu-id="3f55b-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3f55b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f55b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f55b-126">-WhatIf</span></span>
<span data-ttu-id="3f55b-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3f55b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f55b-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3f55b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f55b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f55b-129">CommonParameters</span></span>
<span data-ttu-id="3f55b-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f55b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f55b-131">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f55b-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f55b-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f55b-132">INPUTS</span></span>

### <span data-ttu-id="3f55b-133">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="3f55b-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

### <span data-ttu-id="3f55b-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3f55b-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3f55b-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f55b-135">OUTPUTS</span></span>

### <span data-ttu-id="3f55b-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3f55b-136">System.Boolean</span></span>

## <span data-ttu-id="3f55b-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f55b-137">NOTES</span></span>

## <span data-ttu-id="3f55b-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f55b-138">RELATED LINKS</span></span>

[<span data-ttu-id="3f55b-139">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="3f55b-139">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="3f55b-140">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="3f55b-140">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="3f55b-141">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="3f55b-141">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


