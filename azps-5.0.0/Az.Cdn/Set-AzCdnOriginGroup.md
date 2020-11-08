---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
ms.openlocfilehash: 58a9d45c29a9a11b31bff510e6b4e1c63844dd5d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270869"
---
# <span data-ttu-id="15ed0-101">Set-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="15ed0-101">Set-AzCdnOriginGroup</span></span>

## <span data-ttu-id="15ed0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="15ed0-102">SYNOPSIS</span></span>
<span data-ttu-id="15ed0-103">Uppdaterar gruppen CDN-ursprung</span><span class="sxs-lookup"><span data-stu-id="15ed0-103">Updates the CDN origin group</span></span>

## <span data-ttu-id="15ed0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="15ed0-104">SYNTAX</span></span>

### <span data-ttu-id="15ed0-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="15ed0-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15ed0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15ed0-106">ByObjectParameterSet</span></span>
```
Set-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15ed0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="15ed0-107">DESCRIPTION</span></span>
<span data-ttu-id="15ed0-108">Set-AzCdnOriginGroup uppdaterar den angivna ursprungs gruppen inom den angivna slut punkten.</span><span class="sxs-lookup"><span data-stu-id="15ed0-108">Set-AzCdnOriginGroup will update the specified origin group within the given endpoint.</span></span> 

## <span data-ttu-id="15ed0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="15ed0-109">EXAMPLES</span></span>

### <span data-ttu-id="15ed0-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="15ed0-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originIds -ProbeIntervalInSeconds $probeInterval 
```
<span data-ttu-id="15ed0-111">Denna cmdlet uppdaterar egenskapen ProbeIntervalInSeconds i gruppen ursprung.</span><span class="sxs-lookup"><span data-stu-id="15ed0-111">This cmdlet will update the ProbeIntervalInSeconds property in the origin group.</span></span> 

## <span data-ttu-id="15ed0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="15ed0-112">PARAMETERS</span></span>

### <span data-ttu-id="15ed0-113">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="15ed0-113">-CdnOriginGroup</span></span>
<span data-ttu-id="15ed0-114">Gruppobjektet CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="15ed0-114">The CDN origin group object.</span></span>

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

### <span data-ttu-id="15ed0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15ed0-115">-DefaultProfile</span></span>
<span data-ttu-id="15ed0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="15ed0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15ed0-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="15ed0-117">-EndpointName</span></span>
<span data-ttu-id="15ed0-118">Namn på Azure CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="15ed0-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="15ed0-119">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="15ed0-119">-OriginGroupName</span></span>
<span data-ttu-id="15ed0-120">Namn på en grupp med Azure CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="15ed0-120">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="15ed0-121">-OriginId</span><span class="sxs-lookup"><span data-stu-id="15ed0-121">-OriginId</span></span>
<span data-ttu-id="15ed0-122">Grupp-ID: n för Azure CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="15ed0-122">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="15ed0-123">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="15ed0-123">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="15ed0-124">Antal sekunder mellan hälso avsökningarna.</span><span class="sxs-lookup"><span data-stu-id="15ed0-124">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="15ed0-125">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="15ed0-125">-ProbePath</span></span>
<span data-ttu-id="15ed0-126">Sökvägen i förhållande till ursprunget som används för att fastställa statusen för origo.</span><span class="sxs-lookup"><span data-stu-id="15ed0-126">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="15ed0-127">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="15ed0-127">-ProbeProtocol</span></span>
<span data-ttu-id="15ed0-128">Protokoll som ska användas för hälso sökning.</span><span class="sxs-lookup"><span data-stu-id="15ed0-128">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="15ed0-129">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="15ed0-129">-ProbeRequestType</span></span>
<span data-ttu-id="15ed0-130">Typ av begäran om hälso sökning.</span><span class="sxs-lookup"><span data-stu-id="15ed0-130">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="15ed0-131">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="15ed0-131">-ProfileName</span></span>
<span data-ttu-id="15ed0-132">Namn på Azure CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="15ed0-132">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="15ed0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15ed0-133">-ResourceGroupName</span></span>
<span data-ttu-id="15ed0-134">Resurs gruppen för Azure CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="15ed0-134">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="15ed0-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="15ed0-135">-Confirm</span></span>
<span data-ttu-id="15ed0-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="15ed0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15ed0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15ed0-137">-WhatIf</span></span>
<span data-ttu-id="15ed0-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="15ed0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15ed0-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="15ed0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15ed0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15ed0-140">CommonParameters</span></span>
<span data-ttu-id="15ed0-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15ed0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15ed0-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15ed0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15ed0-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="15ed0-143">INPUTS</span></span>

### <span data-ttu-id="15ed0-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="15ed0-144">System.Object</span></span>

## <span data-ttu-id="15ed0-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="15ed0-145">OUTPUTS</span></span>

### <span data-ttu-id="15ed0-146">System. Object</span><span class="sxs-lookup"><span data-stu-id="15ed0-146">System.Object</span></span>

## <span data-ttu-id="15ed0-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="15ed0-147">NOTES</span></span>

## <span data-ttu-id="15ed0-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="15ed0-148">RELATED LINKS</span></span>
