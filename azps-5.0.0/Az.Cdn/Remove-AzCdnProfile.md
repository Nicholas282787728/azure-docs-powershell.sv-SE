---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
ms.openlocfilehash: ba45ea8d4c1b58290623f7f415f09cdb7663f575
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270880"
---
# <span data-ttu-id="7b729-101">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="7b729-101">Remove-AzCdnProfile</span></span>

## <span data-ttu-id="7b729-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7b729-102">SYNOPSIS</span></span>
<span data-ttu-id="7b729-103">Tar bort en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="7b729-103">Removes a CDN profile.</span></span>

## <span data-ttu-id="7b729-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7b729-104">SYNTAX</span></span>

### <span data-ttu-id="7b729-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b729-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b729-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b729-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b729-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7b729-107">DESCRIPTION</span></span>
<span data-ttu-id="7b729-108">Cmdleten **Remove-AzCdnProfile** tar bort en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="7b729-108">The **Remove-AzCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="7b729-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7b729-109">EXAMPLES</span></span>

## <span data-ttu-id="7b729-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7b729-110">PARAMETERS</span></span>

### <span data-ttu-id="7b729-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="7b729-111">-CdnProfile</span></span>
<span data-ttu-id="7b729-112">Anger den profil som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="7b729-112">Specifies the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7b729-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b729-113">-DefaultProfile</span></span>
<span data-ttu-id="7b729-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7b729-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b729-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7b729-115">-Force</span></span>
<span data-ttu-id="7b729-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="7b729-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7b729-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b729-117">-PassThru</span></span>
<span data-ttu-id="7b729-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="7b729-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7b729-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="7b729-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7b729-120">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="7b729-120">-ProfileName</span></span>
<span data-ttu-id="7b729-121">Anger namnet på den profil som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="7b729-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7b729-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b729-122">-ResourceGroupName</span></span>
<span data-ttu-id="7b729-123">Anger namnet på den resurs grupp som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="7b729-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="7b729-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7b729-124">-Confirm</span></span>
<span data-ttu-id="7b729-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7b729-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b729-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b729-126">-WhatIf</span></span>
<span data-ttu-id="7b729-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7b729-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b729-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7b729-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b729-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b729-129">CommonParameters</span></span>
<span data-ttu-id="7b729-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b729-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b729-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b729-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b729-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7b729-132">INPUTS</span></span>

### <span data-ttu-id="7b729-133">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="7b729-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

### <span data-ttu-id="7b729-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7b729-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7b729-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7b729-135">OUTPUTS</span></span>

### <span data-ttu-id="7b729-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7b729-136">System.Boolean</span></span>

## <span data-ttu-id="7b729-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7b729-137">NOTES</span></span>

## <span data-ttu-id="7b729-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7b729-138">RELATED LINKS</span></span>

[<span data-ttu-id="7b729-139">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="7b729-139">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="7b729-140">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="7b729-140">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="7b729-141">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="7b729-141">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


