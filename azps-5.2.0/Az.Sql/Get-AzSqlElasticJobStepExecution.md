---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstepexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
ms.openlocfilehash: 03c4a6dede1f60e782bbfecdec1fb18894b2ca15
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395027"
---
# <span data-ttu-id="4d17d-101">Get-AzSqlElasticJobStepExecution</span><span class="sxs-lookup"><span data-stu-id="4d17d-101">Get-AzSqlElasticJobStepExecution</span></span>

## <span data-ttu-id="4d17d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d17d-102">SYNOPSIS</span></span>
<span data-ttu-id="4d17d-103">Får ett eller flera jobb körningar</span><span class="sxs-lookup"><span data-stu-id="4d17d-103">Gets one or more job step executions</span></span>

## <span data-ttu-id="4d17d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d17d-104">SYNTAX</span></span>

### <span data-ttu-id="4d17d-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4d17d-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4d17d-106">WithJobStepName</span><span class="sxs-lookup"><span data-stu-id="4d17d-106">WithJobStepName</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -StepName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4d17d-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="4d17d-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d17d-108">WithJobStepNameUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4d17d-108">WithJobStepNameUsingParentObject</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d17d-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4d17d-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d17d-110">WithJobStepNameUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4d17d-110">WithJobStepNameUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d17d-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d17d-111">DESCRIPTION</span></span>
<span data-ttu-id="4d17d-112">Med Get-AzSqlElasticJobStepExecution cmdlet får du ett eller flera jobb körningar från en jobb körning</span><span class="sxs-lookup"><span data-stu-id="4d17d-112">The Get-AzSqlElasticJobStepExecution cmdlet gets one or more job step executions from a job execution</span></span>

## <span data-ttu-id="4d17d-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d17d-113">EXAMPLES</span></span>

### <span data-ttu-id="4d17d-114">Exempel 1-hämtar ett eller flera jobb-körningar från ett jobb försök</span><span class="sxs-lookup"><span data-stu-id="4d17d-114">Example 1 - Gets one or more job step executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="4d17d-115">Exempel 2 – får ett eller flera jobb körningar från en jobb körning, filtrerar enligt steg namn</span><span class="sxs-lookup"><span data-stu-id="4d17d-115">Example 2 - Gets one or more job step executions from a job execution, filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution -StepName step1

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

<span data-ttu-id="4d17d-116">Får ett eller flera jobb körningar</span><span class="sxs-lookup"><span data-stu-id="4d17d-116">Gets one or more job step executions</span></span>

## <span data-ttu-id="4d17d-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d17d-117">PARAMETERS</span></span>

### <span data-ttu-id="4d17d-118">-Aktiv</span><span class="sxs-lookup"><span data-stu-id="4d17d-118">-Active</span></span>
<span data-ttu-id="4d17d-119">Flagga för att filtrera efter aktiva körningar.</span><span class="sxs-lookup"><span data-stu-id="4d17d-119">Flag to filter by active executions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d17d-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="4d17d-120">-AgentName</span></span>
<span data-ttu-id="4d17d-121">Namnet på agenten.</span><span class="sxs-lookup"><span data-stu-id="4d17d-121">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d17d-122">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="4d17d-122">-CreateTimeMax</span></span>
<span data-ttu-id="4d17d-123">Filtrera efter skapande tid Max</span><span class="sxs-lookup"><span data-stu-id="4d17d-123">Filter by create time max</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d17d-124">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="4d17d-124">-CreateTimeMin</span></span>
<span data-ttu-id="4d17d-125">Filtrera efter skapa tid</span><span class="sxs-lookup"><span data-stu-id="4d17d-125">Filter by create time min</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d17d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d17d-126">-DefaultProfile</span></span>
<span data-ttu-id="4d17d-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4d17d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d17d-128">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="4d17d-128">-EndTimeMax</span></span>
<span data-ttu-id="4d17d-129">Filtrera efter slut tid max.</span><span class="sxs-lookup"><span data-stu-id="4d17d-129">Filter by end time max.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d17d-130">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="4d17d-130">-EndTimeMin</span></span>
<span data-ttu-id="4d17d-131">Filtrerar efter slut tid min.</span><span class="sxs-lookup"><span data-stu-id="4d17d-131">Filter by end time min.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d17d-132">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="4d17d-132">-JobExecutionId</span></span>
<span data-ttu-id="4d17d-133">Kör-ID för jobb.</span><span class="sxs-lookup"><span data-stu-id="4d17d-133">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d17d-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="4d17d-134">-JobName</span></span>
<span data-ttu-id="4d17d-135">Jobbnamn.</span><span class="sxs-lookup"><span data-stu-id="4d17d-135">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d17d-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4d17d-136">-ParentObject</span></span>
<span data-ttu-id="4d17d-137">Agent-objektet.</span><span class="sxs-lookup"><span data-stu-id="4d17d-137">The agent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet, WithJobStepNameUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d17d-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4d17d-138">-ParentResourceId</span></span>
<span data-ttu-id="4d17d-139">Resurs-ID för jobb körning.</span><span class="sxs-lookup"><span data-stu-id="4d17d-139">The job execution resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d17d-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d17d-140">-ResourceGroupName</span></span>
<span data-ttu-id="4d17d-141">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4d17d-141">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d17d-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4d17d-142">-ServerName</span></span>
<span data-ttu-id="4d17d-143">Server namnet.</span><span class="sxs-lookup"><span data-stu-id="4d17d-143">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d17d-144">-StepName</span><span class="sxs-lookup"><span data-stu-id="4d17d-144">-StepName</span></span>
<span data-ttu-id="4d17d-145">Namnet på jobb steget.</span><span class="sxs-lookup"><span data-stu-id="4d17d-145">The job step name.</span></span>

```yaml
Type: System.String
Parameter Sets: WithJobStepName, WithJobStepNameUsingParentObject, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d17d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d17d-146">CommonParameters</span></span>
<span data-ttu-id="4d17d-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d17d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d17d-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d17d-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d17d-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d17d-149">INPUTS</span></span>

### <span data-ttu-id="4d17d-150">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="4d17d-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="4d17d-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d17d-151">OUTPUTS</span></span>

### <span data-ttu-id="4d17d-152">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="4d17d-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="4d17d-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d17d-153">NOTES</span></span>

## <span data-ttu-id="4d17d-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d17d-154">RELATED LINKS</span></span>
