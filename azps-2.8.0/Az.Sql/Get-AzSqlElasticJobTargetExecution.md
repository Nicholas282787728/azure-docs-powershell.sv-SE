---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
ms.openlocfilehash: 95cd4cdfb9cc21207e336a514e91d56193119e8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920363"
---
# <span data-ttu-id="6704f-101">Get-AzSqlElasticJobTargetExecution</span><span class="sxs-lookup"><span data-stu-id="6704f-101">Get-AzSqlElasticJobTargetExecution</span></span>

## <span data-ttu-id="6704f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6704f-102">SYNOPSIS</span></span>
<span data-ttu-id="6704f-103">Hämtar ett eller flera jobb mål</span><span class="sxs-lookup"><span data-stu-id="6704f-103">Gets one or more job target executions</span></span>

## <span data-ttu-id="6704f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6704f-104">SYNTAX</span></span>

### <span data-ttu-id="6704f-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6704f-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -Count <Int32> [-StepName <String>] [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6704f-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="6704f-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -Count <Int32>
 [-StepName <String>] [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6704f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6704f-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentResourceId] <String> -Count <Int32> [-StepName <String>]
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6704f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6704f-108">DESCRIPTION</span></span>
<span data-ttu-id="6704f-109">Get-AzSqlElasticJobTargetExecution cmdlet får ett eller flera jobb mål körningar från en jobb körning</span><span class="sxs-lookup"><span data-stu-id="6704f-109">The Get-AzSqlElasticJobTargetExecution cmdlet gets one or more job target executions from a job execution</span></span>

## <span data-ttu-id="6704f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6704f-110">EXAMPLES</span></span>

### <span data-ttu-id="6704f-111">Exempel 1-får ett eller flera jobb mål körningar från ett jobb uppdrag</span><span class="sxs-lookup"><span data-stu-id="6704f-111">Example 1 - Gets one or more job target executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
job1    1          step1    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db1                6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="6704f-112">Exempel 2 – får ett eller flera jobb mål körningar från ett jobb körning-filtrering enligt steget namn</span><span class="sxs-lookup"><span data-stu-id="6704f-112">Example 2 - Gets one or more job target executions from a job executions - filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2 -StepName step2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
```

<span data-ttu-id="6704f-113">Hämtar ett eller flera jobb mål</span><span class="sxs-lookup"><span data-stu-id="6704f-113">Gets one or more job target executions</span></span>

## <span data-ttu-id="6704f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6704f-114">PARAMETERS</span></span>

### <span data-ttu-id="6704f-115">-Aktiv</span><span class="sxs-lookup"><span data-stu-id="6704f-115">-Active</span></span>
<span data-ttu-id="6704f-116">Flagga för att filtrera efter aktiva körningar.</span><span class="sxs-lookup"><span data-stu-id="6704f-116">Flag to filter by active executions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6704f-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="6704f-117">-AgentName</span></span>
<span data-ttu-id="6704f-118">Namnet på agenten.</span><span class="sxs-lookup"><span data-stu-id="6704f-118">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6704f-119">-Antal</span><span class="sxs-lookup"><span data-stu-id="6704f-119">-Count</span></span>
<span data-ttu-id="6704f-120">COUNT returnerar det högsta antalet körningar.</span><span class="sxs-lookup"><span data-stu-id="6704f-120">Count returns the top number of executions.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6704f-121">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="6704f-121">-CreateTimeMax</span></span>
<span data-ttu-id="6704f-122">Filtrera efter skapande tid Max</span><span class="sxs-lookup"><span data-stu-id="6704f-122">Filter by create time max</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6704f-123">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="6704f-123">-CreateTimeMin</span></span>
<span data-ttu-id="6704f-124">Filtrera efter skapa tid</span><span class="sxs-lookup"><span data-stu-id="6704f-124">Filter by create time min</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6704f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6704f-125">-DefaultProfile</span></span>
<span data-ttu-id="6704f-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6704f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6704f-127">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="6704f-127">-EndTimeMax</span></span>
<span data-ttu-id="6704f-128">Filtrera efter slut tid max.</span><span class="sxs-lookup"><span data-stu-id="6704f-128">Filter by end time max.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6704f-129">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="6704f-129">-EndTimeMin</span></span>
<span data-ttu-id="6704f-130">Filtrerar efter slut tid min.</span><span class="sxs-lookup"><span data-stu-id="6704f-130">Filter by end time min.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6704f-131">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="6704f-131">-JobExecutionId</span></span>
<span data-ttu-id="6704f-132">Kör-ID för jobb.</span><span class="sxs-lookup"><span data-stu-id="6704f-132">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6704f-133">-JobName</span><span class="sxs-lookup"><span data-stu-id="6704f-133">-JobName</span></span>
<span data-ttu-id="6704f-134">Jobbnamn.</span><span class="sxs-lookup"><span data-stu-id="6704f-134">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6704f-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6704f-135">-ParentObject</span></span>
<span data-ttu-id="6704f-136">Jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="6704f-136">The job execution object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6704f-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6704f-137">-ParentResourceId</span></span>
<span data-ttu-id="6704f-138">Resurs-ID för jobb körning.</span><span class="sxs-lookup"><span data-stu-id="6704f-138">The job execution resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6704f-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6704f-139">-ResourceGroupName</span></span>
<span data-ttu-id="6704f-140">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="6704f-140">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6704f-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6704f-141">-ServerName</span></span>
<span data-ttu-id="6704f-142">Server namnet.</span><span class="sxs-lookup"><span data-stu-id="6704f-142">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6704f-143">-StepName</span><span class="sxs-lookup"><span data-stu-id="6704f-143">-StepName</span></span>
<span data-ttu-id="6704f-144">Namnet på jobb steget.</span><span class="sxs-lookup"><span data-stu-id="6704f-144">The job step name.</span></span>

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

### <span data-ttu-id="6704f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6704f-145">CommonParameters</span></span>
<span data-ttu-id="6704f-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6704f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6704f-147">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6704f-147">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6704f-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6704f-148">INPUTS</span></span>

### <span data-ttu-id="6704f-149">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="6704f-149">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="6704f-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6704f-150">OUTPUTS</span></span>

### <span data-ttu-id="6704f-151">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="6704f-151">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="6704f-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6704f-152">NOTES</span></span>

## <span data-ttu-id="6704f-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6704f-153">RELATED LINKS</span></span>
