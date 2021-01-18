---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 503f274b07b13bc19b4994f8b440ffc853f69bc5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526319"
---
# <span data-ttu-id="77e2a-101">Set-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="77e2a-101">Set-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="77e2a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="77e2a-102">SYNOPSIS</span></span>
<span data-ttu-id="77e2a-103">Uppdaterar ett bandbredds schema.</span><span class="sxs-lookup"><span data-stu-id="77e2a-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="77e2a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="77e2a-104">SYNTAX</span></span>

### <span data-ttu-id="77e2a-105">UpdateByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="77e2a-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77e2a-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77e2a-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77e2a-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="77e2a-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77e2a-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="77e2a-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77e2a-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77e2a-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77e2a-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="77e2a-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77e2a-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="77e2a-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77e2a-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="77e2a-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77e2a-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="77e2a-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77e2a-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="77e2a-114">DESCRIPTION</span></span>
<span data-ttu-id="77e2a-115">Cmdleten **set-AzDataBoxEdgeBandwidthSchedule** uppdaterar ett bandbredds schema för Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="77e2a-115">The **Set-AzDataBoxEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Data Box Edge device.</span></span>

## <span data-ttu-id="77e2a-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="77e2a-116">EXAMPLES</span></span>

### <span data-ttu-id="77e2a-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="77e2a-117">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="77e2a-118">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="77e2a-118">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="77e2a-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="77e2a-119">PARAMETERS</span></span>

### <span data-ttu-id="77e2a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77e2a-120">-AsJob</span></span>
<span data-ttu-id="77e2a-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="77e2a-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77e2a-122">-Bandbredd</span><span class="sxs-lookup"><span data-stu-id="77e2a-122">-Bandwidth</span></span>
<span data-ttu-id="77e2a-123">Bandbredd i Mbps</span><span class="sxs-lookup"><span data-stu-id="77e2a-123">Bandwidth in Mbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateByResourceIdParameterBandwidthSet, UpdateByInputObjectParameterBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e2a-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="77e2a-124">-DaysOfWeek</span></span>
<span data-ttu-id="77e2a-125">Schemalagd DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="77e2a-125">Scheduled DaysOfWeek</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e2a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77e2a-126">-DefaultProfile</span></span>
<span data-ttu-id="77e2a-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="77e2a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77e2a-128">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="77e2a-128">-DeviceName</span></span>
<span data-ttu-id="77e2a-129">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="77e2a-129">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e2a-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77e2a-130">-InputObject</span></span>
<span data-ttu-id="77e2a-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="77e2a-131">Azure ResourceId</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule
Parameter Sets: UpdateByInputObjectParameterSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e2a-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="77e2a-132">-Name</span></span>
<span data-ttu-id="77e2a-133">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="77e2a-133">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e2a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77e2a-134">-ResourceGroupName</span></span>
<span data-ttu-id="77e2a-135">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="77e2a-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e2a-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77e2a-136">-ResourceId</span></span>
<span data-ttu-id="77e2a-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="77e2a-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet, UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByResourceIdParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e2a-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="77e2a-138">-StartTime</span></span>
<span data-ttu-id="77e2a-139">Schemalägg start tid</span><span class="sxs-lookup"><span data-stu-id="77e2a-139">Schedule Start Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e2a-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="77e2a-140">-StopTime</span></span>
<span data-ttu-id="77e2a-141">Schemalägg stopptid</span><span class="sxs-lookup"><span data-stu-id="77e2a-141">Schedule Stop Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e2a-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="77e2a-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="77e2a-143">Ger obegränsad bandbredd</span><span class="sxs-lookup"><span data-stu-id="77e2a-143">Will Set Unlimited Bandwidth</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByNameParameterUnlimitedBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e2a-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="77e2a-144">-Confirm</span></span>
<span data-ttu-id="77e2a-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="77e2a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77e2a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77e2a-146">-WhatIf</span></span>
<span data-ttu-id="77e2a-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="77e2a-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77e2a-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="77e2a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77e2a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77e2a-149">CommonParameters</span></span>
<span data-ttu-id="77e2a-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77e2a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77e2a-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77e2a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77e2a-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="77e2a-152">INPUTS</span></span>

### <span data-ttu-id="77e2a-153">Ingen</span><span class="sxs-lookup"><span data-stu-id="77e2a-153">None</span></span>

## <span data-ttu-id="77e2a-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="77e2a-154">OUTPUTS</span></span>

### <span data-ttu-id="77e2a-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="77e2a-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="77e2a-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="77e2a-156">NOTES</span></span>

## <span data-ttu-id="77e2a-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="77e2a-157">RELATED LINKS</span></span>
