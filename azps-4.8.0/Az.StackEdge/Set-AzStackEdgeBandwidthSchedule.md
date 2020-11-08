---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: db54799f13ca7524ccf42ade8b7e33c61a134ae9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260929"
---
# <span data-ttu-id="08007-101">Set-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="08007-101">Set-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="08007-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08007-102">SYNOPSIS</span></span>
<span data-ttu-id="08007-103">Uppdaterar ett bandbredds schema.</span><span class="sxs-lookup"><span data-stu-id="08007-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="08007-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08007-104">SYNTAX</span></span>

### <span data-ttu-id="08007-105">UpdateByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="08007-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08007-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08007-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08007-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="08007-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08007-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="08007-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08007-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08007-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08007-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="08007-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08007-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="08007-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08007-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="08007-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08007-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="08007-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08007-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08007-114">DESCRIPTION</span></span>
<span data-ttu-id="08007-115">Cmdleten **set-AzStackEdgeBandwidthSchedule** uppdaterar ett bandbredds schema för en trave Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="08007-115">The **Set-AzStackEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Stack Edge device.</span></span>

## <span data-ttu-id="08007-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08007-116">EXAMPLES</span></span>

### <span data-ttu-id="08007-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="08007-117">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="08007-118">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="08007-118">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="08007-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08007-119">PARAMETERS</span></span>

### <span data-ttu-id="08007-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08007-120">-AsJob</span></span>
<span data-ttu-id="08007-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="08007-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="08007-122">-Bandbredd</span><span class="sxs-lookup"><span data-stu-id="08007-122">-Bandwidth</span></span>
<span data-ttu-id="08007-123">Bandbredd i Mbps</span><span class="sxs-lookup"><span data-stu-id="08007-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="08007-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="08007-124">-DaysOfWeek</span></span>
<span data-ttu-id="08007-125">Schemalagd DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="08007-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="08007-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08007-126">-DefaultProfile</span></span>
<span data-ttu-id="08007-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="08007-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08007-128">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="08007-128">-DeviceName</span></span>
<span data-ttu-id="08007-129">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="08007-129">Device Name</span></span>

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

### <span data-ttu-id="08007-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08007-130">-InputObject</span></span>
<span data-ttu-id="08007-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="08007-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="08007-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="08007-132">-Name</span></span>
<span data-ttu-id="08007-133">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="08007-133">Resource Name</span></span>

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

### <span data-ttu-id="08007-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08007-134">-ResourceGroupName</span></span>
<span data-ttu-id="08007-135">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="08007-135">Resource Group Name</span></span>

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

### <span data-ttu-id="08007-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08007-136">-ResourceId</span></span>
<span data-ttu-id="08007-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="08007-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="08007-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="08007-138">-StartTime</span></span>
<span data-ttu-id="08007-139">Schemalägg start tid</span><span class="sxs-lookup"><span data-stu-id="08007-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="08007-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="08007-140">-StopTime</span></span>
<span data-ttu-id="08007-141">Schemalägg stopptid</span><span class="sxs-lookup"><span data-stu-id="08007-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="08007-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="08007-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="08007-143">Ger obegränsad bandbredd</span><span class="sxs-lookup"><span data-stu-id="08007-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="08007-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="08007-144">-Confirm</span></span>
<span data-ttu-id="08007-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="08007-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08007-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08007-146">-WhatIf</span></span>
<span data-ttu-id="08007-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="08007-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08007-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="08007-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08007-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08007-149">CommonParameters</span></span>
<span data-ttu-id="08007-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08007-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08007-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08007-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08007-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08007-152">INPUTS</span></span>

### <span data-ttu-id="08007-153">Ingen</span><span class="sxs-lookup"><span data-stu-id="08007-153">None</span></span>

## <span data-ttu-id="08007-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08007-154">OUTPUTS</span></span>

### <span data-ttu-id="08007-155">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="08007-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="08007-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08007-156">NOTES</span></span>

## <span data-ttu-id="08007-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08007-157">RELATED LINKS</span></span>
