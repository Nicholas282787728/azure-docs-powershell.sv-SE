---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
ms.openlocfilehash: 8198d189d9619528bdc7fb80d30285ce9126dfed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524612"
---
# <span data-ttu-id="3adba-101">Remove-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="3adba-101">Remove-AzCdnOrigin</span></span>

## <span data-ttu-id="3adba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3adba-102">SYNOPSIS</span></span>
<span data-ttu-id="3adba-103">Tar bort ett CDN-ursprung</span><span class="sxs-lookup"><span data-stu-id="3adba-103">Removes a CDN origin</span></span>

## <span data-ttu-id="3adba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3adba-104">SYNTAX</span></span>

### <span data-ttu-id="3adba-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3adba-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOrigin -OriginName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3adba-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3adba-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOrigin -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3adba-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3adba-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOrigin [-PassThru] -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3adba-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3adba-108">DESCRIPTION</span></span>
<span data-ttu-id="3adba-109">Remove-AzCdnOrigin tar bort ett CDN-ursprung från den angivna slut punkten.</span><span class="sxs-lookup"><span data-stu-id="3adba-109">Remove-AzCdnOrigin will delete a CDN origin from the given endpoint.</span></span> <span data-ttu-id="3adba-110">Om Origo är det enda ursprunget inom den angivna slut punkten Miss lyckas borttagningen eftersom minst 1 Origo behövs.</span><span class="sxs-lookup"><span data-stu-id="3adba-110">If the origin is the only origin within the specified endpoint, then the deletion will fail since at least 1 origin is needed.</span></span> 

## <span data-ttu-id="3adba-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3adba-111">EXAMPLES</span></span>

### <span data-ttu-id="3adba-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3adba-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName 
```
<span data-ttu-id="3adba-113">Denna cmdlet tar bort angivet ursprung från den angivna slut punkten.</span><span class="sxs-lookup"><span data-stu-id="3adba-113">This cmdlet will remove the specified origin from the given endpoint.</span></span> 

## <span data-ttu-id="3adba-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3adba-114">PARAMETERS</span></span>

### <span data-ttu-id="3adba-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="3adba-115">-CdnOrigin</span></span>
<span data-ttu-id="3adba-116">Originalvärdet Origin-objekt.</span><span class="sxs-lookup"><span data-stu-id="3adba-116">The CDN origin object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3adba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3adba-117">-DefaultProfile</span></span>
<span data-ttu-id="3adba-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3adba-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3adba-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3adba-119">-EndpointName</span></span>
<span data-ttu-id="3adba-120">Namn på Azure CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="3adba-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="3adba-121">-OriginName</span><span class="sxs-lookup"><span data-stu-id="3adba-121">-OriginName</span></span>
<span data-ttu-id="3adba-122">Namn på Azure CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="3adba-122">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="3adba-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3adba-123">-PassThru</span></span>
<span data-ttu-id="3adba-124">Returnera objekt om det anges.</span><span class="sxs-lookup"><span data-stu-id="3adba-124">Return object if specified.</span></span>

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

### <span data-ttu-id="3adba-125">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="3adba-125">-ProfileName</span></span>
<span data-ttu-id="3adba-126">Namn på Azure CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="3adba-126">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="3adba-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3adba-127">-ResourceGroupName</span></span>
<span data-ttu-id="3adba-128">Resurs gruppen för Azure CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="3adba-128">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="3adba-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3adba-129">-ResourceId</span></span>
<span data-ttu-id="3adba-130">Resurs-ID för Azure CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="3adba-130">The resource id of the Azure CDN origin.</span></span>

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

### <span data-ttu-id="3adba-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3adba-131">-Confirm</span></span>
<span data-ttu-id="3adba-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3adba-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3adba-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3adba-133">-WhatIf</span></span>
<span data-ttu-id="3adba-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3adba-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3adba-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3adba-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3adba-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3adba-136">CommonParameters</span></span>
<span data-ttu-id="3adba-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3adba-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3adba-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3adba-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3adba-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3adba-139">INPUTS</span></span>

### <span data-ttu-id="3adba-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="3adba-140">None</span></span>

## <span data-ttu-id="3adba-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3adba-141">OUTPUTS</span></span>

### <span data-ttu-id="3adba-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3adba-142">System.Boolean</span></span>

## <span data-ttu-id="3adba-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3adba-143">NOTES</span></span>

## <span data-ttu-id="3adba-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3adba-144">RELATED LINKS</span></span>
