---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E3D7A3FE-40D4-4495-BA39-493F85F304AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsapplicationinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
ms.openlocfilehash: 0f238a417ac83cac82305ceb9c9ce20586328976
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527356"
---
# <span data-ttu-id="cf849-101">New-AzOperationalInsightsApplicationInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="cf849-101">New-AzOperationalInsightsApplicationInsightsDataSource</span></span>

## <span data-ttu-id="cf849-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cf849-102">SYNOPSIS</span></span>
<span data-ttu-id="cf849-103">Samla in loggar från ett givet Application-Insights-program.</span><span class="sxs-lookup"><span data-stu-id="cf849-103">Collect logs from given Application-Insights application.</span></span>

## <span data-ttu-id="cf849-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cf849-104">SYNTAX</span></span>

### <span data-ttu-id="cf849-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="cf849-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf849-106">ByWorkspaceObjectByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="cf849-106">ByWorkspaceObjectByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf849-107">ByWorkspaceObjectByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="cf849-107">ByWorkspaceObjectByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf849-108">ByWorkspaceNameByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="cf849-108">ByWorkspaceNameByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf849-109">ByWorkspaceNameByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="cf849-109">ByWorkspaceNameByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf849-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cf849-110">DESCRIPTION</span></span>
<span data-ttu-id="cf849-111">**New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet aktiverar samlingen av loggar från ett givet Application-Insights-program.</span><span class="sxs-lookup"><span data-stu-id="cf849-111">The **New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet enables the collection of logs from a given Application-Insights application.</span></span>

## <span data-ttu-id="cf849-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cf849-112">EXAMPLES</span></span>

### <span data-ttu-id="cf849-113">Exempel 1: skapa en data källa med Application-Insights i arbets ytan</span><span class="sxs-lookup"><span data-stu-id="cf849-113">Example 1: Create application-insights data source in workspace</span></span>
```
PS C:\> New-AzOperationalInsightsApplicationInsightsDataSource -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -ApplicationSubscriptionId "e791a474-ee54-46a2-bb06-5e058302d234" -ApplicationResourceGroupName "ContosoResourceGroup" -ApplicationName "MyAIApplication"

Name              : subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="cf849-114">Det här kommandot skapar en program-Insights-data källa för ett givet program i en given logganalys-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="cf849-114">This command creates an application-insights data source of a given application in a given log analytics workspace.</span></span> <span data-ttu-id="cf849-115">Detta möjliggör insamling av loggar från ett givet program till arbets ytan logganalys.</span><span class="sxs-lookup"><span data-stu-id="cf849-115">This enables the collection of logs from given application to the log analytics workspace.</span></span>

### <span data-ttu-id="cf849-116">Exempel 2: Hämta arbets yta och skapa en data källa för Application Insights med program resurs-ID</span><span class="sxs-lookup"><span data-stu-id="cf849-116">Example 2: Get workspace object and create application-insights data source by the application resource id</span></span>
```
PS C:\> Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup" | New-AzOperationalInsightsApplicationInsightsDataSource -ApplicationResourceId "/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication"

Name              : subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="cf849-117">Det här kommandot visar hur du hämtar ett objekt i logganalys-arbetsytan och sedan skickar utdata för att skapa en associerad program data källa med program resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="cf849-117">This command demonstrates getting a log analytics workspace object and then passing the output to create an associated application-insights data source by the application resource id.</span></span> 

## <span data-ttu-id="cf849-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cf849-118">PARAMETERS</span></span>

### <span data-ttu-id="cf849-119">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="cf849-119">-ApplicationName</span></span>
<span data-ttu-id="cf849-120">Namnet på det länkade programmet.</span><span class="sxs-lookup"><span data-stu-id="cf849-120">The name of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf849-121">-ApplicationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf849-121">-ApplicationResourceGroupName</span></span>
<span data-ttu-id="cf849-122">Namnet på den länkade program resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cf849-122">The resource group name of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf849-123">-ApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="cf849-123">-ApplicationResourceId</span></span>
<span data-ttu-id="cf849-124">Resurs-ID för länkad program.</span><span class="sxs-lookup"><span data-stu-id="cf849-124">The linked application resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationResourceId, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf849-125">-ApplicationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf849-125">-ApplicationSubscriptionId</span></span>
<span data-ttu-id="cf849-126">Abonnemangs-ID för det länkade programmet.</span><span class="sxs-lookup"><span data-stu-id="cf849-126">The subscription id of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf849-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf849-127">-DefaultProfile</span></span>
<span data-ttu-id="cf849-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cf849-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf849-129">-Force</span><span class="sxs-lookup"><span data-stu-id="cf849-129">-Force</span></span>
<span data-ttu-id="cf849-130">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="cf849-130">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="cf849-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf849-131">-ResourceGroupName</span></span>
<span data-ttu-id="cf849-132">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="cf849-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByApplicationParameters, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf849-133">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="cf849-133">-Workspace</span></span>
<span data-ttu-id="cf849-134">Arbets ytan som innehåller data källan.</span><span class="sxs-lookup"><span data-stu-id="cf849-134">The workspace that will contain the data source.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceObjectByApplicationResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf849-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cf849-135">-WorkspaceName</span></span>
<span data-ttu-id="cf849-136">Namnet på den arbets yta som ska innehålla data källan.</span><span class="sxs-lookup"><span data-stu-id="cf849-136">The name of the workspace that will contain the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByApplicationParameters, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf849-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cf849-137">-Confirm</span></span>
<span data-ttu-id="cf849-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cf849-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf849-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf849-139">-WhatIf</span></span>
<span data-ttu-id="cf849-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cf849-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf849-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cf849-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf849-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf849-142">CommonParameters</span></span>
<span data-ttu-id="cf849-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf849-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf849-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf849-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf849-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cf849-145">INPUTS</span></span>

### <span data-ttu-id="cf849-146">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="cf849-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="cf849-147">System. String</span><span class="sxs-lookup"><span data-stu-id="cf849-147">System.String</span></span>

## <span data-ttu-id="cf849-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cf849-148">OUTPUTS</span></span>

### <span data-ttu-id="cf849-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="cf849-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="cf849-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cf849-150">NOTES</span></span>

## <span data-ttu-id="cf849-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cf849-151">RELATED LINKS</span></span>
