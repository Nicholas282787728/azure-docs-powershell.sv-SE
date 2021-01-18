---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
ms.openlocfilehash: 081d5a73d6bd3cefff6f0c3bc57d3e0190f785a7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527104"
---
# <span data-ttu-id="7d68e-101">Remove-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="7d68e-101">Remove-AzCdnOriginGroup</span></span>

## <span data-ttu-id="7d68e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d68e-102">SYNOPSIS</span></span>
<span data-ttu-id="7d68e-103">Tar bort en CDN-Origine</span><span class="sxs-lookup"><span data-stu-id="7d68e-103">Removes a CDN origin group</span></span>

## <span data-ttu-id="7d68e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d68e-104">SYNTAX</span></span>

### <span data-ttu-id="7d68e-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7d68e-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOriginGroup -OriginGroupName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d68e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d68e-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOriginGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d68e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d68e-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOriginGroup [-PassThru] -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d68e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d68e-108">DESCRIPTION</span></span>
<span data-ttu-id="7d68e-109">Remove-AzCdnOriginGroup tar bort en CDN-ursprung från den angivna slut punkten.</span><span class="sxs-lookup"><span data-stu-id="7d68e-109">Remove-AzCdnOriginGroup will remove a CDN origin group from the specified endpoint.</span></span> 

## <span data-ttu-id="7d68e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d68e-110">EXAMPLES</span></span>

### <span data-ttu-id="7d68e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7d68e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="7d68e-112">Denna cmdlet tar bort den angivna ursprungs gruppen från den angivna slut punkten.</span><span class="sxs-lookup"><span data-stu-id="7d68e-112">This cmdlet will remove the specified origin group from the given endpoint.</span></span> 

## <span data-ttu-id="7d68e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d68e-113">PARAMETERS</span></span>

### <span data-ttu-id="7d68e-114">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="7d68e-114">-CdnOriginGroup</span></span>
<span data-ttu-id="7d68e-115">Gruppobjektet CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="7d68e-115">The CDN origin group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.OriginGroup.PSOriginGroup
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d68e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d68e-116">-DefaultProfile</span></span>
<span data-ttu-id="7d68e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7d68e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d68e-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7d68e-118">-EndpointName</span></span>
<span data-ttu-id="7d68e-119">Namn på Azure CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="7d68e-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="7d68e-120">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="7d68e-120">-OriginGroupName</span></span>
<span data-ttu-id="7d68e-121">Namn på en grupp med Azure CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="7d68e-121">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="7d68e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d68e-122">-PassThru</span></span>
<span data-ttu-id="7d68e-123">Returnera objekt om det anges.</span><span class="sxs-lookup"><span data-stu-id="7d68e-123">Return object if specified.</span></span>

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

### <span data-ttu-id="7d68e-124">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="7d68e-124">-ProfileName</span></span>
<span data-ttu-id="7d68e-125">Namn på Azure CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="7d68e-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="7d68e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d68e-126">-ResourceGroupName</span></span>
<span data-ttu-id="7d68e-127">Resurs gruppen för Azure CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="7d68e-127">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="7d68e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d68e-128">-ResourceId</span></span>
<span data-ttu-id="7d68e-129">Resurs-ID för Azure CDN Origin-gruppen.</span><span class="sxs-lookup"><span data-stu-id="7d68e-129">The resource id of the Azure CDN origin group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d68e-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7d68e-130">-Confirm</span></span>
<span data-ttu-id="7d68e-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7d68e-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d68e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d68e-132">-WhatIf</span></span>
<span data-ttu-id="7d68e-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7d68e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d68e-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7d68e-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d68e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d68e-135">CommonParameters</span></span>
<span data-ttu-id="7d68e-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d68e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d68e-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d68e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d68e-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d68e-138">INPUTS</span></span>

### <span data-ttu-id="7d68e-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="7d68e-139">None</span></span>

## <span data-ttu-id="7d68e-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d68e-140">OUTPUTS</span></span>

### <span data-ttu-id="7d68e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7d68e-141">System.Boolean</span></span>

## <span data-ttu-id="7d68e-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d68e-142">NOTES</span></span>

## <span data-ttu-id="7d68e-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d68e-143">RELATED LINKS</span></span>
