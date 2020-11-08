---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: db54799f13ca7524ccf42ade8b7e33c61a134ae9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270438"
---
# <span data-ttu-id="dfa74-101">Set-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="dfa74-101">Set-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="dfa74-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dfa74-102">SYNOPSIS</span></span>
<span data-ttu-id="dfa74-103">Uppdaterar ett bandbredds schema.</span><span class="sxs-lookup"><span data-stu-id="dfa74-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="dfa74-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dfa74-104">SYNTAX</span></span>

### <span data-ttu-id="dfa74-105">UpdateByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="dfa74-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfa74-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfa74-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dfa74-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="dfa74-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfa74-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="dfa74-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfa74-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfa74-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfa74-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="dfa74-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfa74-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="dfa74-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfa74-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="dfa74-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfa74-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="dfa74-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfa74-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dfa74-114">DESCRIPTION</span></span>
<span data-ttu-id="dfa74-115">Cmdleten **set-AzStackEdgeBandwidthSchedule** uppdaterar ett bandbredds schema för en trave Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="dfa74-115">The **Set-AzStackEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Stack Edge device.</span></span>

## <span data-ttu-id="dfa74-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dfa74-116">EXAMPLES</span></span>

### <span data-ttu-id="dfa74-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dfa74-117">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="dfa74-118">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="dfa74-118">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="dfa74-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dfa74-119">PARAMETERS</span></span>

### <span data-ttu-id="dfa74-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dfa74-120">-AsJob</span></span>
<span data-ttu-id="dfa74-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="dfa74-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dfa74-122">-Bandbredd</span><span class="sxs-lookup"><span data-stu-id="dfa74-122">-Bandwidth</span></span>
<span data-ttu-id="dfa74-123">Bandbredd i Mbps</span><span class="sxs-lookup"><span data-stu-id="dfa74-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="dfa74-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="dfa74-124">-DaysOfWeek</span></span>
<span data-ttu-id="dfa74-125">Schemalagd DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="dfa74-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="dfa74-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfa74-126">-DefaultProfile</span></span>
<span data-ttu-id="dfa74-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dfa74-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfa74-128">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="dfa74-128">-DeviceName</span></span>
<span data-ttu-id="dfa74-129">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="dfa74-129">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfa74-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfa74-130">-InputObject</span></span>
<span data-ttu-id="dfa74-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="dfa74-131">Azure ResourceId</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule
Parameter Sets: UpdateByInputObjectParameterSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterBandwidthSet
Aliases: BandwidthSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfa74-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="dfa74-132">-Name</span></span>
<span data-ttu-id="dfa74-133">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="dfa74-133">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa74-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfa74-134">-ResourceGroupName</span></span>
<span data-ttu-id="dfa74-135">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="dfa74-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfa74-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dfa74-136">-ResourceId</span></span>
<span data-ttu-id="dfa74-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="dfa74-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet, UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByResourceIdParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfa74-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="dfa74-138">-StartTime</span></span>
<span data-ttu-id="dfa74-139">Schemalägg start tid</span><span class="sxs-lookup"><span data-stu-id="dfa74-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="dfa74-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="dfa74-140">-StopTime</span></span>
<span data-ttu-id="dfa74-141">Schemalägg stopptid</span><span class="sxs-lookup"><span data-stu-id="dfa74-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="dfa74-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="dfa74-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="dfa74-143">Ger obegränsad bandbredd</span><span class="sxs-lookup"><span data-stu-id="dfa74-143">Will Set Unlimited Bandwidth</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByNameParameterUnlimitedBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa74-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dfa74-144">-Confirm</span></span>
<span data-ttu-id="dfa74-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dfa74-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfa74-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfa74-146">-WhatIf</span></span>
<span data-ttu-id="dfa74-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dfa74-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dfa74-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dfa74-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfa74-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfa74-149">CommonParameters</span></span>
<span data-ttu-id="dfa74-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfa74-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfa74-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfa74-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfa74-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dfa74-152">INPUTS</span></span>

### <span data-ttu-id="dfa74-153">Ingen</span><span class="sxs-lookup"><span data-stu-id="dfa74-153">None</span></span>

## <span data-ttu-id="dfa74-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dfa74-154">OUTPUTS</span></span>

### <span data-ttu-id="dfa74-155">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="dfa74-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="dfa74-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dfa74-156">NOTES</span></span>

## <span data-ttu-id="dfa74-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dfa74-157">RELATED LINKS</span></span>
