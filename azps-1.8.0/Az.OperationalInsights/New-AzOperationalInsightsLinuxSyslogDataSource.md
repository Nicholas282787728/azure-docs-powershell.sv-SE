---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: a0268931d276c74560acd5cb04cac1d1e5778b81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747570"
---
# <span data-ttu-id="9b584-101">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="9b584-101">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="9b584-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b584-102">SYNOPSIS</span></span>
<span data-ttu-id="9b584-103">Lägger till en data källa för Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="9b584-103">Adds a data source to Linux computers.</span></span>

## <span data-ttu-id="9b584-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b584-104">SYNTAX</span></span>

### <span data-ttu-id="9b584-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="9b584-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b584-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9b584-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Facility] <String>
 [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning] [-CollectNotice]
 [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b584-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b584-107">DESCRIPTION</span></span>
<span data-ttu-id="9b584-108">**New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet lägger till en syslog-datakälla på anslutna Linux-datorer på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="9b584-108">The **New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="9b584-109">Användnings information för Azure kan samla in syslog-data.</span><span class="sxs-lookup"><span data-stu-id="9b584-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="9b584-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b584-110">EXAMPLES</span></span>

## <span data-ttu-id="9b584-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b584-111">PARAMETERS</span></span>

### <span data-ttu-id="9b584-112">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="9b584-112">-CollectAlert</span></span>
<span data-ttu-id="9b584-113">Anger att operativa insikter samlar in aviseringar.</span><span class="sxs-lookup"><span data-stu-id="9b584-113">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="9b584-114">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="9b584-114">-CollectCritical</span></span>
<span data-ttu-id="9b584-115">Visar att operativa insikter samlar in kritiska meddelanden.</span><span class="sxs-lookup"><span data-stu-id="9b584-115">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="9b584-116">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="9b584-116">-CollectDebug</span></span>
<span data-ttu-id="9b584-117">Anger att operativa insikter samlar in fel söknings meddelanden.</span><span class="sxs-lookup"><span data-stu-id="9b584-117">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="9b584-118">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="9b584-118">-CollectEmergency</span></span>
<span data-ttu-id="9b584-119">Anger att funktions insikter samlar in nödsamtal.</span><span class="sxs-lookup"><span data-stu-id="9b584-119">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="9b584-120">-CollectError</span><span class="sxs-lookup"><span data-stu-id="9b584-120">-CollectError</span></span>
<span data-ttu-id="9b584-121">Anger att drift insikter samlar in fel meddelanden.</span><span class="sxs-lookup"><span data-stu-id="9b584-121">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="9b584-122">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="9b584-122">-CollectInformational</span></span>
<span data-ttu-id="9b584-123">Visar att operativa insikter samlar in informations meddelanden.</span><span class="sxs-lookup"><span data-stu-id="9b584-123">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="9b584-124">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="9b584-124">-CollectNotice</span></span>
<span data-ttu-id="9b584-125">Visar att operativa insikter samlar in meddelanden.</span><span class="sxs-lookup"><span data-stu-id="9b584-125">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="9b584-126">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="9b584-126">-CollectWarning</span></span>
<span data-ttu-id="9b584-127">Anger att syslog inkluderar varnings meddelanden.</span><span class="sxs-lookup"><span data-stu-id="9b584-127">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="9b584-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b584-128">-DefaultProfile</span></span>
<span data-ttu-id="9b584-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9b584-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b584-130">-Anläggning</span><span class="sxs-lookup"><span data-stu-id="9b584-130">-Facility</span></span>
<span data-ttu-id="9b584-131">Anger en funktions kod.</span><span class="sxs-lookup"><span data-stu-id="9b584-131">Specifies a facility code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b584-132">-Force</span><span class="sxs-lookup"><span data-stu-id="9b584-132">-Force</span></span>
<span data-ttu-id="9b584-133">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="9b584-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9b584-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="9b584-134">-Name</span></span>
<span data-ttu-id="9b584-135">Anger ett namn för data källan.</span><span class="sxs-lookup"><span data-stu-id="9b584-135">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b584-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b584-136">-ResourceGroupName</span></span>
<span data-ttu-id="9b584-137">Anger namnet på en resurs grupp som innehåller Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="9b584-137">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b584-138">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="9b584-138">-Workspace</span></span>
<span data-ttu-id="9b584-139">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="9b584-139">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b584-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9b584-140">-WorkspaceName</span></span>
<span data-ttu-id="9b584-141">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="9b584-141">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b584-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9b584-142">-Confirm</span></span>
<span data-ttu-id="9b584-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9b584-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b584-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b584-144">-WhatIf</span></span>
<span data-ttu-id="9b584-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9b584-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b584-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9b584-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b584-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b584-147">CommonParameters</span></span>
<span data-ttu-id="9b584-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b584-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b584-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b584-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b584-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b584-150">INPUTS</span></span>

### <span data-ttu-id="9b584-151">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="9b584-151">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="9b584-152">System. String</span><span class="sxs-lookup"><span data-stu-id="9b584-152">System.String</span></span>

## <span data-ttu-id="9b584-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b584-153">OUTPUTS</span></span>

### <span data-ttu-id="9b584-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="9b584-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="9b584-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b584-155">NOTES</span></span>

## <span data-ttu-id="9b584-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b584-156">RELATED LINKS</span></span>

[<span data-ttu-id="9b584-157">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="9b584-157">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="9b584-158">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="9b584-158">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)


