---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 68522dbd90593bdbc37afe333144431b997cc70c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321195"
---
# <span data-ttu-id="51e91-101">New-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="51e91-101">New-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="51e91-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51e91-102">SYNOPSIS</span></span>
<span data-ttu-id="51e91-103">Skapar ett nytt bandbredds schema</span><span class="sxs-lookup"><span data-stu-id="51e91-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="51e91-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51e91-104">SYNTAX</span></span>

### <span data-ttu-id="51e91-105">BandwidthParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="51e91-105">BandwidthParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51e91-106">UnlimitedBandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="51e91-106">UnlimitedBandwidthParameterSet</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51e91-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51e91-107">DESCRIPTION</span></span>
<span data-ttu-id="51e91-108">**New-AzDataBoxEdgeBandwidthSchedule-** cmdleten skapar ett nytt bandbredds schema för Edge-enheten för att hantera bandbredds användning.</span><span class="sxs-lookup"><span data-stu-id="51e91-108">The **New-AzDataBoxEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Data Box Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="51e91-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51e91-109">EXAMPLES</span></span>

### <span data-ttu-id="51e91-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="51e91-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="51e91-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="51e91-111">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="51e91-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51e91-112">PARAMETERS</span></span>

### <span data-ttu-id="51e91-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51e91-113">-AsJob</span></span>
<span data-ttu-id="51e91-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="51e91-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51e91-115">-Bandbredd</span><span class="sxs-lookup"><span data-stu-id="51e91-115">-Bandwidth</span></span>
<span data-ttu-id="51e91-116">Bandbredd i Mbps</span><span class="sxs-lookup"><span data-stu-id="51e91-116">Bandwidth in Mbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: BandwidthParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e91-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="51e91-117">-DaysOfWeek</span></span>
<span data-ttu-id="51e91-118">Schemalagd DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="51e91-118">Scheduled DaysOfWeek</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e91-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51e91-119">-DefaultProfile</span></span>
<span data-ttu-id="51e91-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="51e91-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51e91-121">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="51e91-121">-DeviceName</span></span>
<span data-ttu-id="51e91-122">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="51e91-122">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e91-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="51e91-123">-Name</span></span>
<span data-ttu-id="51e91-124">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="51e91-124">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e91-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51e91-125">-ResourceGroupName</span></span>
<span data-ttu-id="51e91-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="51e91-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e91-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="51e91-127">-StartTime</span></span>
<span data-ttu-id="51e91-128">Schemalägg start tid</span><span class="sxs-lookup"><span data-stu-id="51e91-128">Schedule Start Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e91-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="51e91-129">-StopTime</span></span>
<span data-ttu-id="51e91-130">Schemalägg stopptid</span><span class="sxs-lookup"><span data-stu-id="51e91-130">Schedule Stop Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e91-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="51e91-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="51e91-132">Obegränsad bandbredd anges om värdet är false Anger standardvärdet till 20 Mbps</span><span class="sxs-lookup"><span data-stu-id="51e91-132">Will Set Unlimited Bandwidth, if set to false will set default value as 20 Mbps</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UnlimitedBandwidthParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e91-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="51e91-133">-Confirm</span></span>
<span data-ttu-id="51e91-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="51e91-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51e91-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51e91-135">-WhatIf</span></span>
<span data-ttu-id="51e91-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="51e91-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51e91-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="51e91-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51e91-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51e91-138">CommonParameters</span></span>
<span data-ttu-id="51e91-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51e91-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51e91-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51e91-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51e91-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51e91-141">INPUTS</span></span>

### <span data-ttu-id="51e91-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="51e91-142">None</span></span>

## <span data-ttu-id="51e91-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51e91-143">OUTPUTS</span></span>

### <span data-ttu-id="51e91-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="51e91-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="51e91-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51e91-145">NOTES</span></span>

## <span data-ttu-id="51e91-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51e91-146">RELATED LINKS</span></span>