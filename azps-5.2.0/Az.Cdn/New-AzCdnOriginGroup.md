---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
ms.openlocfilehash: 9c499fe716df97edc4644729dc996bd4f9bae992
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412395"
---
# <span data-ttu-id="cadcc-101">New-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="cadcc-101">New-AzCdnOriginGroup</span></span>

## <span data-ttu-id="cadcc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cadcc-102">SYNOPSIS</span></span>
<span data-ttu-id="cadcc-103">Skapar en ny CDN-ursprungs grupp</span><span class="sxs-lookup"><span data-stu-id="cadcc-103">Creates a new CDN origin group</span></span>

## <span data-ttu-id="cadcc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cadcc-104">SYNTAX</span></span>

### <span data-ttu-id="cadcc-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="cadcc-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cadcc-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cadcc-106">ByObjectParameterSet</span></span>
```
New-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cadcc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cadcc-107">DESCRIPTION</span></span>
<span data-ttu-id="cadcc-108">New-AzCdnOriginGroup skapar en ny ursprungs grupp inom den angivna slut punkten.</span><span class="sxs-lookup"><span data-stu-id="cadcc-108">The New-AzCdnOriginGroup will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="cadcc-109">Om det här är den första start gruppen för slut punkten måste också egenskapen DefaultOriginGroup vara inställd.</span><span class="sxs-lookup"><span data-stu-id="cadcc-109">If this is the first origin group for endpoint, then the DefaultOriginGroup property must also be set.</span></span>

## <span data-ttu-id="cadcc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cadcc-110">EXAMPLES</span></span>

### <span data-ttu-id="cadcc-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cadcc-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originId
```
<span data-ttu-id="cadcc-112">Denna cmdlet kommer att skapa en ny ursprungs grupp för den angivna slut punkten.</span><span class="sxs-lookup"><span data-stu-id="cadcc-112">This cmdlet will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="cadcc-113">Det kommer att använda de angivna ursprungs-ID: na.</span><span class="sxs-lookup"><span data-stu-id="cadcc-113">It will utilize the given origin ids as the set of origins.</span></span>

## <span data-ttu-id="cadcc-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cadcc-114">PARAMETERS</span></span>

### <span data-ttu-id="cadcc-115">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="cadcc-115">-CdnOriginGroup</span></span>
<span data-ttu-id="cadcc-116">Gruppobjektet CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="cadcc-116">The CDN origin group object.</span></span>

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

### <span data-ttu-id="cadcc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cadcc-117">-DefaultProfile</span></span>
<span data-ttu-id="cadcc-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cadcc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cadcc-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="cadcc-119">-EndpointName</span></span>
<span data-ttu-id="cadcc-120">Namn på Azure CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="cadcc-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="cadcc-121">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="cadcc-121">-OriginGroupName</span></span>
<span data-ttu-id="cadcc-122">Namn på en grupp med Azure CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="cadcc-122">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="cadcc-123">-OriginId</span><span class="sxs-lookup"><span data-stu-id="cadcc-123">-OriginId</span></span>
<span data-ttu-id="cadcc-124">Grupp-ID: n för Azure CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="cadcc-124">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="cadcc-125">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="cadcc-125">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="cadcc-126">Antal sekunder mellan hälso avsökningarna.</span><span class="sxs-lookup"><span data-stu-id="cadcc-126">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="cadcc-127">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="cadcc-127">-ProbePath</span></span>
<span data-ttu-id="cadcc-128">Sökvägen i förhållande till ursprunget som används för att fastställa statusen för origo.</span><span class="sxs-lookup"><span data-stu-id="cadcc-128">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="cadcc-129">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="cadcc-129">-ProbeProtocol</span></span>
<span data-ttu-id="cadcc-130">Protokoll som ska användas för hälso sökning.</span><span class="sxs-lookup"><span data-stu-id="cadcc-130">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="cadcc-131">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="cadcc-131">-ProbeRequestType</span></span>
<span data-ttu-id="cadcc-132">Typ av begäran om hälso sökning.</span><span class="sxs-lookup"><span data-stu-id="cadcc-132">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="cadcc-133">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="cadcc-133">-ProfileName</span></span>
<span data-ttu-id="cadcc-134">Namn på Azure CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="cadcc-134">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="cadcc-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cadcc-135">-ResourceGroupName</span></span>
<span data-ttu-id="cadcc-136">Resurs gruppen för Azure CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="cadcc-136">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="cadcc-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cadcc-137">-Confirm</span></span>
<span data-ttu-id="cadcc-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cadcc-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cadcc-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cadcc-139">-WhatIf</span></span>
<span data-ttu-id="cadcc-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cadcc-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cadcc-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cadcc-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cadcc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cadcc-142">CommonParameters</span></span>
<span data-ttu-id="cadcc-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cadcc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cadcc-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cadcc-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cadcc-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cadcc-145">INPUTS</span></span>

### <span data-ttu-id="cadcc-146">System. Object</span><span class="sxs-lookup"><span data-stu-id="cadcc-146">System.Object</span></span>

## <span data-ttu-id="cadcc-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cadcc-147">OUTPUTS</span></span>

### <span data-ttu-id="cadcc-148">System. Object</span><span class="sxs-lookup"><span data-stu-id="cadcc-148">System.Object</span></span>

## <span data-ttu-id="cadcc-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cadcc-149">NOTES</span></span>

## <span data-ttu-id="cadcc-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cadcc-150">RELATED LINKS</span></span>
