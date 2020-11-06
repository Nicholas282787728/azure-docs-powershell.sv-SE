---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: 49d465b1d993542790c20833ff5b1f75e03d5f26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585992"
---
# <span data-ttu-id="69ee5-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="69ee5-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="69ee5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="69ee5-103">Lägger till en data källa för Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="69ee5-103">Adds a data source to Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69ee5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69ee5-104">SYNTAX</span></span>

### <span data-ttu-id="69ee5-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="69ee5-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69ee5-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="69ee5-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning]
 [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69ee5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69ee5-107">DESCRIPTION</span></span>
<span data-ttu-id="69ee5-108">**New-AzureRmOperationalInsightsLinuxSyslogDataSource** cmdlet lägger till en syslog-datakälla på anslutna Linux-datorer på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="69ee5-108">The **New-AzureRmOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="69ee5-109">Användnings information för Azure kan samla in syslog-data.</span><span class="sxs-lookup"><span data-stu-id="69ee5-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="69ee5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69ee5-110">EXAMPLES</span></span>

## <span data-ttu-id="69ee5-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69ee5-111">PARAMETERS</span></span>

### <span data-ttu-id="69ee5-112">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="69ee5-112">-CollectAlert</span></span>
<span data-ttu-id="69ee5-113">Anger att operativa insikter samlar in aviseringar.</span><span class="sxs-lookup"><span data-stu-id="69ee5-113">Indicates that Operational Insights collects alert messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-114">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="69ee5-114">-CollectCritical</span></span>
<span data-ttu-id="69ee5-115">Visar att operativa insikter samlar in kritiska meddelanden.</span><span class="sxs-lookup"><span data-stu-id="69ee5-115">Indicates that Operational Insights collects critical messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-116">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="69ee5-116">-CollectDebug</span></span>
<span data-ttu-id="69ee5-117">Anger att operativa insikter samlar in fel söknings meddelanden.</span><span class="sxs-lookup"><span data-stu-id="69ee5-117">Indicates that Operational Insights collects debug messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-118">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="69ee5-118">-CollectEmergency</span></span>
<span data-ttu-id="69ee5-119">Anger att funktions insikter samlar in nödsamtal.</span><span class="sxs-lookup"><span data-stu-id="69ee5-119">Indicates that Operational Insights collects emergency messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-120">-CollectError</span><span class="sxs-lookup"><span data-stu-id="69ee5-120">-CollectError</span></span>
<span data-ttu-id="69ee5-121">Anger att drift insikter samlar in fel meddelanden.</span><span class="sxs-lookup"><span data-stu-id="69ee5-121">Indicates that Operational Insights collects error messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-122">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="69ee5-122">-CollectInformational</span></span>
<span data-ttu-id="69ee5-123">Visar att operativa insikter samlar in informations meddelanden.</span><span class="sxs-lookup"><span data-stu-id="69ee5-123">Indicates that Operational Insights collects informational messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-124">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="69ee5-124">-CollectNotice</span></span>
<span data-ttu-id="69ee5-125">Visar att operativa insikter samlar in meddelanden.</span><span class="sxs-lookup"><span data-stu-id="69ee5-125">Indicates that Operational Insights collects notice messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-126">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="69ee5-126">-CollectWarning</span></span>
<span data-ttu-id="69ee5-127">Anger att syslog inkluderar varnings meddelanden.</span><span class="sxs-lookup"><span data-stu-id="69ee5-127">Indicates that the syslog includes warning messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69ee5-128">-DefaultProfile</span></span>
<span data-ttu-id="69ee5-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="69ee5-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-130">-Anläggning</span><span class="sxs-lookup"><span data-stu-id="69ee5-130">-Facility</span></span>
<span data-ttu-id="69ee5-131">Anger en funktions kod.</span><span class="sxs-lookup"><span data-stu-id="69ee5-131">Specifies a facility code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-132">-Force</span><span class="sxs-lookup"><span data-stu-id="69ee5-132">-Force</span></span>
<span data-ttu-id="69ee5-133">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="69ee5-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="69ee5-134">-Name</span></span>
<span data-ttu-id="69ee5-135">Anger ett namn för data källan.</span><span class="sxs-lookup"><span data-stu-id="69ee5-135">Specifies a name for the data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69ee5-136">-ResourceGroupName</span></span>
<span data-ttu-id="69ee5-137">Anger namnet på en resurs grupp som innehåller Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="69ee5-137">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-138">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="69ee5-138">-Workspace</span></span>
<span data-ttu-id="69ee5-139">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="69ee5-139">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="69ee5-140">-WorkspaceName</span></span>
<span data-ttu-id="69ee5-141">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="69ee5-141">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="69ee5-142">-Confirm</span></span>
<span data-ttu-id="69ee5-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="69ee5-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69ee5-144">-WhatIf</span></span>
<span data-ttu-id="69ee5-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="69ee5-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69ee5-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="69ee5-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ee5-147">CommonParameters</span></span>
<span data-ttu-id="69ee5-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69ee5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ee5-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69ee5-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ee5-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69ee5-150">INPUTS</span></span>

### <span data-ttu-id="69ee5-151">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="69ee5-151">PSWorkspace</span></span>
<span data-ttu-id="69ee5-152">Parametern ' Workspace ' godkänner värdet av typen ' PSWorkspace ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="69ee5-152">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="69ee5-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69ee5-153">OUTPUTS</span></span>

### <span data-ttu-id="69ee5-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="69ee5-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="69ee5-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69ee5-155">NOTES</span></span>

## <span data-ttu-id="69ee5-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69ee5-156">RELATED LINKS</span></span>

[<span data-ttu-id="69ee5-157">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="69ee5-157">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="69ee5-158">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="69ee5-158">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md)


