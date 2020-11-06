---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: 86bc4b8bedbaafb6da1267d94ffa01b3d0ca95c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575163"
---
# <span data-ttu-id="d8b0e-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="d8b0e-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="d8b0e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8b0e-102">SYNOPSIS</span></span>
<span data-ttu-id="d8b0e-103">Lägger till en data källa för Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="d8b0e-103">Adds a data source to Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8b0e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8b0e-104">SYNTAX</span></span>

### <span data-ttu-id="d8b0e-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="d8b0e-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8b0e-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d8b0e-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning]
 [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8b0e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8b0e-107">DESCRIPTION</span></span>
<span data-ttu-id="d8b0e-108">**New-AzureRmOperationalInsightsLinuxSyslogDataSource** cmdlet lägger till en syslog-datakälla på anslutna Linux-datorer på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="d8b0e-108">The **New-AzureRmOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="d8b0e-109">Användnings information för Azure kan samla in syslog-data.</span><span class="sxs-lookup"><span data-stu-id="d8b0e-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="d8b0e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8b0e-110">EXAMPLES</span></span>

## <span data-ttu-id="d8b0e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8b0e-111">PARAMETERS</span></span>

### <span data-ttu-id="d8b0e-112">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="d8b0e-112">-CollectAlert</span></span>
<span data-ttu-id="d8b0e-113">Anger att operativa insikter samlar in aviseringar.</span><span class="sxs-lookup"><span data-stu-id="d8b0e-113">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="d8b0e-114">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="d8b0e-114">-CollectCritical</span></span>
<span data-ttu-id="d8b0e-115">Visar att operativa insikter samlar in kritiska meddelanden.</span><span class="sxs-lookup"><span data-stu-id="d8b0e-115">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="d8b0e-116">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="d8b0e-116">-CollectDebug</span></span>
<span data-ttu-id="d8b0e-117">Anger att operativa insikter samlar in fel söknings meddelanden.</span><span class="sxs-lookup"><span data-stu-id="d8b0e-117">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="d8b0e-118">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="d8b0e-118">-CollectEmergency</span></span>
<span data-ttu-id="d8b0e-119">Anger att funktions insikter samlar in nödsamtal.</span><span class="sxs-lookup"><span data-stu-id="d8b0e-119">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="d8b0e-120">-CollectError</span><span class="sxs-lookup"><span data-stu-id="d8b0e-120">-CollectError</span></span>
<span data-ttu-id="d8b0e-121">Anger att drift insikter samlar in fel meddelanden.</span><span class="sxs-lookup"><span data-stu-id="d8b0e-121">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="d8b0e-122">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="d8b0e-122">-CollectInformational</span></span>
<span data-ttu-id="d8b0e-123">Visar att operativa insikter samlar in informations meddelanden.</span><span class="sxs-lookup"><span data-stu-id="d8b0e-123">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="d8b0e-124">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="d8b0e-124">-CollectNotice</span></span>
<span data-ttu-id="d8b0e-125">Visar att operativa insikter samlar in meddelanden.</span><span class="sxs-lookup"><span data-stu-id="d8b0e-125">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="d8b0e-126">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="d8b0e-126">-CollectWarning</span></span>
<span data-ttu-id="d8b0e-127">Anger att syslog inkluderar varnings meddelanden.</span><span class="sxs-lookup"><span data-stu-id="d8b0e-127">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="d8b0e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8b0e-128">-DefaultProfile</span></span>
<span data-ttu-id="d8b0e-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d8b0e-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b0e-130">-Anläggning</span><span class="sxs-lookup"><span data-stu-id="d8b0e-130">-Facility</span></span>
<span data-ttu-id="d8b0e-131">Anger en funktions kod.</span><span class="sxs-lookup"><span data-stu-id="d8b0e-131">Specifies a facility code.</span></span>

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

### <span data-ttu-id="d8b0e-132">-Force</span><span class="sxs-lookup"><span data-stu-id="d8b0e-132">-Force</span></span>
<span data-ttu-id="d8b0e-133">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d8b0e-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d8b0e-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="d8b0e-134">-Name</span></span>
<span data-ttu-id="d8b0e-135">Anger ett namn för data källan.</span><span class="sxs-lookup"><span data-stu-id="d8b0e-135">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="d8b0e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8b0e-136">-ResourceGroupName</span></span>
<span data-ttu-id="d8b0e-137">Anger namnet på en resurs grupp som innehåller Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="d8b0e-137">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="d8b0e-138">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="d8b0e-138">-Workspace</span></span>
<span data-ttu-id="d8b0e-139">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="d8b0e-139">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d8b0e-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d8b0e-140">-WorkspaceName</span></span>
<span data-ttu-id="d8b0e-141">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="d8b0e-141">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d8b0e-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d8b0e-142">-Confirm</span></span>
<span data-ttu-id="d8b0e-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d8b0e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8b0e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8b0e-144">-WhatIf</span></span>
<span data-ttu-id="d8b0e-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d8b0e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8b0e-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d8b0e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8b0e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8b0e-147">CommonParameters</span></span>
<span data-ttu-id="d8b0e-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8b0e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8b0e-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8b0e-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8b0e-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8b0e-150">INPUTS</span></span>

### <span data-ttu-id="d8b0e-151">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d8b0e-151">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="d8b0e-152">Parametrar: arbets yta (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d8b0e-152">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="d8b0e-153">System. String</span><span class="sxs-lookup"><span data-stu-id="d8b0e-153">System.String</span></span>

## <span data-ttu-id="d8b0e-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8b0e-154">OUTPUTS</span></span>

### <span data-ttu-id="d8b0e-155">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="d8b0e-155">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d8b0e-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8b0e-156">NOTES</span></span>

## <span data-ttu-id="d8b0e-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8b0e-157">RELATED LINKS</span></span>

[<span data-ttu-id="d8b0e-158">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="d8b0e-158">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="d8b0e-159">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="d8b0e-159">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md)


