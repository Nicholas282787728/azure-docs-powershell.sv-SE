---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: e15e6ee6186dc19f9f85264548c1b735ea242b98
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924669"
---
# <span data-ttu-id="890ac-101">New-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="890ac-101">New-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="890ac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="890ac-102">SYNOPSIS</span></span>
<span data-ttu-id="890ac-103">Skapar ett nytt bandbredds schema</span><span class="sxs-lookup"><span data-stu-id="890ac-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="890ac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="890ac-104">SYNTAX</span></span>

### <span data-ttu-id="890ac-105">BandwidthParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="890ac-105">BandwidthParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="890ac-106">UnlimitedBandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="890ac-106">UnlimitedBandwidthParameterSet</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="890ac-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="890ac-107">DESCRIPTION</span></span>
<span data-ttu-id="890ac-108">**New-AzDataBoxEdgeBandwidthSchedule-** cmdleten skapar ett nytt bandbredds schema för Edge-enheten för att hantera bandbredds användning.</span><span class="sxs-lookup"><span data-stu-id="890ac-108">The **New-AzDataBoxEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Data Box Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="890ac-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="890ac-109">EXAMPLES</span></span>

### <span data-ttu-id="890ac-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="890ac-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="890ac-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="890ac-111">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="890ac-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="890ac-112">PARAMETERS</span></span>

### <span data-ttu-id="890ac-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="890ac-113">-AsJob</span></span>
<span data-ttu-id="890ac-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="890ac-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="890ac-115">-Bandbredd</span><span class="sxs-lookup"><span data-stu-id="890ac-115">-Bandwidth</span></span>
<span data-ttu-id="890ac-116">Bandbredd i Mbps</span><span class="sxs-lookup"><span data-stu-id="890ac-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="890ac-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="890ac-117">-DaysOfWeek</span></span>
<span data-ttu-id="890ac-118">Schemalagd DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="890ac-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="890ac-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="890ac-119">-DefaultProfile</span></span>
<span data-ttu-id="890ac-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="890ac-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="890ac-121">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="890ac-121">-DeviceName</span></span>
<span data-ttu-id="890ac-122">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="890ac-122">Device Name</span></span>

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

### <span data-ttu-id="890ac-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="890ac-123">-Name</span></span>
<span data-ttu-id="890ac-124">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="890ac-124">Resource Name</span></span>

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

### <span data-ttu-id="890ac-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="890ac-125">-ResourceGroupName</span></span>
<span data-ttu-id="890ac-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="890ac-126">Resource Group Name</span></span>

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

### <span data-ttu-id="890ac-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="890ac-127">-StartTime</span></span>
<span data-ttu-id="890ac-128">Schemalägg start tid</span><span class="sxs-lookup"><span data-stu-id="890ac-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="890ac-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="890ac-129">-StopTime</span></span>
<span data-ttu-id="890ac-130">Schemalägg stopptid</span><span class="sxs-lookup"><span data-stu-id="890ac-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="890ac-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="890ac-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="890ac-132">Obegränsad bandbredd anges om värdet är false Anger standardvärdet till 20 Mbps</span><span class="sxs-lookup"><span data-stu-id="890ac-132">Will Set Unlimited Bandwidth, if set to false will set default value as 20 Mbps</span></span>

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

### <span data-ttu-id="890ac-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="890ac-133">-Confirm</span></span>
<span data-ttu-id="890ac-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="890ac-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="890ac-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="890ac-135">-WhatIf</span></span>
<span data-ttu-id="890ac-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="890ac-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="890ac-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="890ac-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="890ac-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="890ac-138">CommonParameters</span></span>
<span data-ttu-id="890ac-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="890ac-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="890ac-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="890ac-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="890ac-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="890ac-141">INPUTS</span></span>

### <span data-ttu-id="890ac-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="890ac-142">None</span></span>

## <span data-ttu-id="890ac-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="890ac-143">OUTPUTS</span></span>

### <span data-ttu-id="890ac-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="890ac-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="890ac-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="890ac-145">NOTES</span></span>

## <span data-ttu-id="890ac-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="890ac-146">RELATED LINKS</span></span>
