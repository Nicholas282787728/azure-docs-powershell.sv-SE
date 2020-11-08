---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 27d1f77db385c04e50b67b9aa3a8d8d6bf921485
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088724"
---
# <span data-ttu-id="e08d4-101">New-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="e08d4-101">New-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="e08d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e08d4-102">SYNOPSIS</span></span>
<span data-ttu-id="e08d4-103">Skapar ett nytt bandbredds schema</span><span class="sxs-lookup"><span data-stu-id="e08d4-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="e08d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e08d4-104">SYNTAX</span></span>

### <span data-ttu-id="e08d4-105">UnlimitedBandwidthParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e08d4-105">UnlimitedBandwidthParameterSet (Default)</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e08d4-106">BandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="e08d4-106">BandwidthParameterSet</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e08d4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e08d4-107">DESCRIPTION</span></span>
<span data-ttu-id="e08d4-108">**New-AzStackEdgeBandwidthSchedule-** cmdleten skapar ett nytt bandbredds schema för en stack gräns enhet för att hantera bandbredds användning.</span><span class="sxs-lookup"><span data-stu-id="e08d4-108">The **New-AzStackEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Stack Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="e08d4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e08d4-109">EXAMPLES</span></span>

### <span data-ttu-id="e08d4-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e08d4-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="e08d4-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="e08d4-111">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="e08d4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e08d4-112">PARAMETERS</span></span>

### <span data-ttu-id="e08d4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e08d4-113">-AsJob</span></span>
<span data-ttu-id="e08d4-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e08d4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e08d4-115">-Bandbredd</span><span class="sxs-lookup"><span data-stu-id="e08d4-115">-Bandwidth</span></span>
<span data-ttu-id="e08d4-116">Bandbredd i Mbps</span><span class="sxs-lookup"><span data-stu-id="e08d4-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="e08d4-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="e08d4-117">-DaysOfWeek</span></span>
<span data-ttu-id="e08d4-118">Schemalagd DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="e08d4-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="e08d4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e08d4-119">-DefaultProfile</span></span>
<span data-ttu-id="e08d4-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e08d4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e08d4-121">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="e08d4-121">-DeviceName</span></span>
<span data-ttu-id="e08d4-122">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="e08d4-122">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e08d4-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="e08d4-123">-Name</span></span>
<span data-ttu-id="e08d4-124">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="e08d4-124">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e08d4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e08d4-125">-ResourceGroupName</span></span>
<span data-ttu-id="e08d4-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="e08d4-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e08d4-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e08d4-127">-StartTime</span></span>
<span data-ttu-id="e08d4-128">Schemalägg start tid</span><span class="sxs-lookup"><span data-stu-id="e08d4-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="e08d4-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="e08d4-129">-StopTime</span></span>
<span data-ttu-id="e08d4-130">Schemalägg stopptid</span><span class="sxs-lookup"><span data-stu-id="e08d4-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="e08d4-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="e08d4-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="e08d4-132">Kan ange bandbredd som obegränsad</span><span class="sxs-lookup"><span data-stu-id="e08d4-132">Will Set Bandwidth as Unlimited</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UnlimitedBandwidthParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e08d4-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e08d4-133">-Confirm</span></span>
<span data-ttu-id="e08d4-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e08d4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e08d4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e08d4-135">-WhatIf</span></span>
<span data-ttu-id="e08d4-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e08d4-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e08d4-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e08d4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e08d4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e08d4-138">CommonParameters</span></span>
<span data-ttu-id="e08d4-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e08d4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e08d4-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e08d4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e08d4-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e08d4-141">INPUTS</span></span>

### <span data-ttu-id="e08d4-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="e08d4-142">None</span></span>

## <span data-ttu-id="e08d4-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e08d4-143">OUTPUTS</span></span>

### <span data-ttu-id="e08d4-144">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="e08d4-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="e08d4-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e08d4-145">NOTES</span></span>

## <span data-ttu-id="e08d4-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e08d4-146">RELATED LINKS</span></span>
