---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
ms.openlocfilehash: 9c499fe716df97edc4644729dc996bd4f9bae992
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527115"
---
# <span data-ttu-id="d4629-101">New-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="d4629-101">New-AzCdnOriginGroup</span></span>

## <span data-ttu-id="d4629-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4629-102">SYNOPSIS</span></span>
<span data-ttu-id="d4629-103">Skapar en ny CDN-ursprungs grupp</span><span class="sxs-lookup"><span data-stu-id="d4629-103">Creates a new CDN origin group</span></span>

## <span data-ttu-id="d4629-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d4629-104">SYNTAX</span></span>

### <span data-ttu-id="d4629-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d4629-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4629-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4629-106">ByObjectParameterSet</span></span>
```
New-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4629-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d4629-107">DESCRIPTION</span></span>
<span data-ttu-id="d4629-108">New-AzCdnOriginGroup skapar en ny ursprungs grupp inom den angivna slut punkten.</span><span class="sxs-lookup"><span data-stu-id="d4629-108">The New-AzCdnOriginGroup will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="d4629-109">Om det här är den första start gruppen för slut punkten måste också egenskapen DefaultOriginGroup vara inställd.</span><span class="sxs-lookup"><span data-stu-id="d4629-109">If this is the first origin group for endpoint, then the DefaultOriginGroup property must also be set.</span></span>

## <span data-ttu-id="d4629-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d4629-110">EXAMPLES</span></span>

### <span data-ttu-id="d4629-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d4629-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originId
```
<span data-ttu-id="d4629-112">Denna cmdlet kommer att skapa en ny ursprungs grupp för den angivna slut punkten.</span><span class="sxs-lookup"><span data-stu-id="d4629-112">This cmdlet will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="d4629-113">Det kommer att använda de angivna ursprungs-ID: na.</span><span class="sxs-lookup"><span data-stu-id="d4629-113">It will utilize the given origin ids as the set of origins.</span></span>

## <span data-ttu-id="d4629-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d4629-114">PARAMETERS</span></span>

### <span data-ttu-id="d4629-115">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="d4629-115">-CdnOriginGroup</span></span>
<span data-ttu-id="d4629-116">Gruppobjektet CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="d4629-116">The CDN origin group object.</span></span>

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

### <span data-ttu-id="d4629-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4629-117">-DefaultProfile</span></span>
<span data-ttu-id="d4629-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d4629-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4629-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d4629-119">-EndpointName</span></span>
<span data-ttu-id="d4629-120">Namn på Azure CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="d4629-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="d4629-121">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="d4629-121">-OriginGroupName</span></span>
<span data-ttu-id="d4629-122">Namn på en grupp med Azure CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="d4629-122">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="d4629-123">-OriginId</span><span class="sxs-lookup"><span data-stu-id="d4629-123">-OriginId</span></span>
<span data-ttu-id="d4629-124">Grupp-ID: n för Azure CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="d4629-124">Azure CDN origin group ids.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4629-125">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="d4629-125">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="d4629-126">Antal sekunder mellan hälso avsökningarna.</span><span class="sxs-lookup"><span data-stu-id="d4629-126">The number of seconds between health probes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4629-127">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="d4629-127">-ProbePath</span></span>
<span data-ttu-id="d4629-128">Sökvägen i förhållande till ursprunget som används för att fastställa statusen för origo.</span><span class="sxs-lookup"><span data-stu-id="d4629-128">The path relative to the origin that is used to determine the health of the origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4629-129">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="d4629-129">-ProbeProtocol</span></span>
<span data-ttu-id="d4629-130">Protokoll som ska användas för hälso sökning.</span><span class="sxs-lookup"><span data-stu-id="d4629-130">Protocol to use for health probe.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4629-131">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="d4629-131">-ProbeRequestType</span></span>
<span data-ttu-id="d4629-132">Typ av begäran om hälso sökning.</span><span class="sxs-lookup"><span data-stu-id="d4629-132">The type of health probe request that is made.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4629-133">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="d4629-133">-ProfileName</span></span>
<span data-ttu-id="d4629-134">Namn på Azure CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="d4629-134">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="d4629-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4629-135">-ResourceGroupName</span></span>
<span data-ttu-id="d4629-136">Resurs gruppen för Azure CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="d4629-136">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="d4629-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d4629-137">-Confirm</span></span>
<span data-ttu-id="d4629-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d4629-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4629-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4629-139">-WhatIf</span></span>
<span data-ttu-id="d4629-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d4629-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4629-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d4629-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4629-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4629-142">CommonParameters</span></span>
<span data-ttu-id="d4629-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4629-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4629-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4629-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4629-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d4629-145">INPUTS</span></span>

### <span data-ttu-id="d4629-146">System. Object</span><span class="sxs-lookup"><span data-stu-id="d4629-146">System.Object</span></span>

## <span data-ttu-id="d4629-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d4629-147">OUTPUTS</span></span>

### <span data-ttu-id="d4629-148">System. Object</span><span class="sxs-lookup"><span data-stu-id="d4629-148">System.Object</span></span>

## <span data-ttu-id="d4629-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d4629-149">NOTES</span></span>

## <span data-ttu-id="d4629-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d4629-150">RELATED LINKS</span></span>
