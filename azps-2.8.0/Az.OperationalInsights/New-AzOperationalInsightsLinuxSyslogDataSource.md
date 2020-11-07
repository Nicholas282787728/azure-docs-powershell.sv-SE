---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: de0864f91ccda3bbf30ec60d06aba60f992baf26
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919618"
---
# <span data-ttu-id="1ceee-101">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="1ceee-101">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="1ceee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1ceee-102">SYNOPSIS</span></span>
<span data-ttu-id="1ceee-103">Lägger till en data källa för Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="1ceee-103">Adds a data source to Linux computers.</span></span>

## <span data-ttu-id="1ceee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1ceee-104">SYNTAX</span></span>

### <span data-ttu-id="1ceee-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="1ceee-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ceee-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1ceee-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Facility] <String>
 [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning] [-CollectNotice]
 [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ceee-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1ceee-107">DESCRIPTION</span></span>
<span data-ttu-id="1ceee-108">**New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet lägger till en syslog-datakälla på anslutna Linux-datorer på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="1ceee-108">The **New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="1ceee-109">Användnings information för Azure kan samla in syslog-data.</span><span class="sxs-lookup"><span data-stu-id="1ceee-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="1ceee-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1ceee-110">EXAMPLES</span></span>

### <span data-ttu-id="1ceee-111">Exempel 1: skapa syslog-datakällor</span><span class="sxs-lookup"><span data-stu-id="1ceee-111">Example 1: Create syslog data sources</span></span>
```
$FacilityNames       = @()
$FacilityNames      += 'auth'
$FacilityNames      += 'authpriv'
$FacilityNames      += 'cron'
$FacilityNames      += 'daemon'
$FacilityNames      += 'ftp'
$FacilityNames      += 'kern'
$FacilityNames      += 'mail'
$FacilityNames      += 'syslog'
$FacilityNames      += 'user'
$FacilityNames      += 'uucp'
$ResourceGroupName   = 'MyResourceGroup'
$WorkspaceName       = 'MyWorkspaceName'

$Count = 0
foreach ($FacilityName in $FacilityNames) {
    $Count++
    $null = New-AzOperationalInsightsLinuxSyslogDataSource `
    -ResourceGroupName $ResourceGroupName `
    -WorkspaceName $WorkspaceName `
    -Name "Linux-syslog-$($Count)" `
    -Facility $FacilityName `
    -CollectEmergency `
    -CollectAlert `
    -CollectCritical `
    -CollectError `
    -CollectWarning `
    -CollectNotice `
    -CollectDebug `
    -CollectInformational
}

Get-AzOperationalInsightsDataSource `
   -ResourceGroupName $ResourceGroupName `
   -WorkspaceName $WorkspaceName `
   -Kind 'LinuxSyslog'
```

## <span data-ttu-id="1ceee-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1ceee-112">PARAMETERS</span></span>

### <span data-ttu-id="1ceee-113">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="1ceee-113">-CollectAlert</span></span>
<span data-ttu-id="1ceee-114">Anger att operativa insikter samlar in aviseringar.</span><span class="sxs-lookup"><span data-stu-id="1ceee-114">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="1ceee-115">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="1ceee-115">-CollectCritical</span></span>
<span data-ttu-id="1ceee-116">Visar att operativa insikter samlar in kritiska meddelanden.</span><span class="sxs-lookup"><span data-stu-id="1ceee-116">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="1ceee-117">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="1ceee-117">-CollectDebug</span></span>
<span data-ttu-id="1ceee-118">Anger att operativa insikter samlar in fel söknings meddelanden.</span><span class="sxs-lookup"><span data-stu-id="1ceee-118">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="1ceee-119">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="1ceee-119">-CollectEmergency</span></span>
<span data-ttu-id="1ceee-120">Anger att funktions insikter samlar in nödsamtal.</span><span class="sxs-lookup"><span data-stu-id="1ceee-120">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="1ceee-121">-CollectError</span><span class="sxs-lookup"><span data-stu-id="1ceee-121">-CollectError</span></span>
<span data-ttu-id="1ceee-122">Anger att drift insikter samlar in fel meddelanden.</span><span class="sxs-lookup"><span data-stu-id="1ceee-122">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="1ceee-123">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="1ceee-123">-CollectInformational</span></span>
<span data-ttu-id="1ceee-124">Visar att operativa insikter samlar in informations meddelanden.</span><span class="sxs-lookup"><span data-stu-id="1ceee-124">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="1ceee-125">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="1ceee-125">-CollectNotice</span></span>
<span data-ttu-id="1ceee-126">Visar att operativa insikter samlar in meddelanden.</span><span class="sxs-lookup"><span data-stu-id="1ceee-126">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="1ceee-127">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="1ceee-127">-CollectWarning</span></span>
<span data-ttu-id="1ceee-128">Anger att syslog inkluderar varnings meddelanden.</span><span class="sxs-lookup"><span data-stu-id="1ceee-128">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="1ceee-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ceee-129">-DefaultProfile</span></span>
<span data-ttu-id="1ceee-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1ceee-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ceee-131">-Anläggning</span><span class="sxs-lookup"><span data-stu-id="1ceee-131">-Facility</span></span>
<span data-ttu-id="1ceee-132">Anger en funktions kod.</span><span class="sxs-lookup"><span data-stu-id="1ceee-132">Specifies a facility code.</span></span>

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

### <span data-ttu-id="1ceee-133">-Force</span><span class="sxs-lookup"><span data-stu-id="1ceee-133">-Force</span></span>
<span data-ttu-id="1ceee-134">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="1ceee-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1ceee-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="1ceee-135">-Name</span></span>
<span data-ttu-id="1ceee-136">Anger ett namn för data källan.</span><span class="sxs-lookup"><span data-stu-id="1ceee-136">Specifies a name for the data source.</span></span> <span data-ttu-id="1ceee-137">Namnet visas inte i Azure-portalen och en sträng kan användas så länge det är unikt.</span><span class="sxs-lookup"><span data-stu-id="1ceee-137">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="1ceee-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ceee-138">-ResourceGroupName</span></span>
<span data-ttu-id="1ceee-139">Anger namnet på en resurs grupp som innehåller Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="1ceee-139">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="1ceee-140">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="1ceee-140">-Workspace</span></span>
<span data-ttu-id="1ceee-141">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="1ceee-141">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="1ceee-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1ceee-142">-WorkspaceName</span></span>
<span data-ttu-id="1ceee-143">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="1ceee-143">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="1ceee-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1ceee-144">-Confirm</span></span>
<span data-ttu-id="1ceee-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1ceee-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ceee-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ceee-146">-WhatIf</span></span>
<span data-ttu-id="1ceee-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1ceee-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ceee-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1ceee-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ceee-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ceee-149">CommonParameters</span></span>
<span data-ttu-id="1ceee-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ceee-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ceee-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ceee-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ceee-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1ceee-152">INPUTS</span></span>

### <span data-ttu-id="1ceee-153">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1ceee-153">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="1ceee-154">System. String</span><span class="sxs-lookup"><span data-stu-id="1ceee-154">System.String</span></span>

## <span data-ttu-id="1ceee-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1ceee-155">OUTPUTS</span></span>

### <span data-ttu-id="1ceee-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="1ceee-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="1ceee-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1ceee-157">NOTES</span></span>

## <span data-ttu-id="1ceee-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1ceee-158">RELATED LINKS</span></span>

[<span data-ttu-id="1ceee-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="1ceee-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="1ceee-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="1ceee-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)


