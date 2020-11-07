---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: 5b5837fb0c5fa56e8e8f9887b6d85bfc3a3a559c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920366"
---
# <span data-ttu-id="05091-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="05091-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="05091-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05091-102">SYNOPSIS</span></span>
<span data-ttu-id="05091-103">Får ett eller flera jobb körningar</span><span class="sxs-lookup"><span data-stu-id="05091-103">Gets one or more job executions</span></span>

## <span data-ttu-id="05091-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05091-104">SYNTAX</span></span>

### <span data-ttu-id="05091-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="05091-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05091-106">WithJobExecutionId</span><span class="sxs-lookup"><span data-stu-id="05091-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05091-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="05091-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05091-108">WithJobExecutionIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="05091-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05091-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="05091-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05091-110">WithJobExecutionIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="05091-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05091-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05091-111">DESCRIPTION</span></span>
<span data-ttu-id="05091-112">Get-AzSqlElasticJobExecution cmdlet får ett eller flera jobb körningar</span><span class="sxs-lookup"><span data-stu-id="05091-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="05091-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05091-113">EXAMPLES</span></span>

### <span data-ttu-id="05091-114">Exempel 1-får ett eller flera jobb för alla jobb</span><span class="sxs-lookup"><span data-stu-id="05091-114">Example 1 - Gets one or more job executions across all jobs</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="05091-115">Exempel 2 – får ett eller flera jobb för jobbet</span><span class="sxs-lookup"><span data-stu-id="05091-115">Example 2 - Gets one or more job executions for a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="05091-116">Får ett eller flera jobb körningar</span><span class="sxs-lookup"><span data-stu-id="05091-116">Gets one or more job executions</span></span>

## <span data-ttu-id="05091-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05091-117">PARAMETERS</span></span>

### <span data-ttu-id="05091-118">-Aktiv</span><span class="sxs-lookup"><span data-stu-id="05091-118">-Active</span></span>
<span data-ttu-id="05091-119">Filtrera efter skapa tid</span><span class="sxs-lookup"><span data-stu-id="05091-119">Filter by create time min</span></span>

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

### <span data-ttu-id="05091-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="05091-120">-AgentName</span></span>
<span data-ttu-id="05091-121">Namnet på agenten.</span><span class="sxs-lookup"><span data-stu-id="05091-121">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05091-122">-Antal</span><span class="sxs-lookup"><span data-stu-id="05091-122">-Count</span></span>
<span data-ttu-id="05091-123">COUNT returnerar det högsta antalet körningar.</span><span class="sxs-lookup"><span data-stu-id="05091-123">Count returns the top number of executions.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05091-124">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="05091-124">-CreateTimeMax</span></span>
<span data-ttu-id="05091-125">Filtrera efter skapa tid</span><span class="sxs-lookup"><span data-stu-id="05091-125">Filter by create time min</span></span>

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

### <span data-ttu-id="05091-126">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="05091-126">-CreateTimeMin</span></span>
<span data-ttu-id="05091-127">Filtrera efter skapa tid</span><span class="sxs-lookup"><span data-stu-id="05091-127">Filter by create time min</span></span>

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

### <span data-ttu-id="05091-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05091-128">-DefaultProfile</span></span>
<span data-ttu-id="05091-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="05091-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05091-130">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="05091-130">-EndTimeMax</span></span>
<span data-ttu-id="05091-131">Filtrera efter skapa tid</span><span class="sxs-lookup"><span data-stu-id="05091-131">Filter by create time min</span></span>

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

### <span data-ttu-id="05091-132">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="05091-132">-EndTimeMin</span></span>
<span data-ttu-id="05091-133">Filtrera efter skapa tid</span><span class="sxs-lookup"><span data-stu-id="05091-133">Filter by create time min</span></span>

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

### <span data-ttu-id="05091-134">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="05091-134">-JobExecutionId</span></span>
<span data-ttu-id="05091-135">Kör-ID för jobb.</span><span class="sxs-lookup"><span data-stu-id="05091-135">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: WithJobExecutionId, WithJobExecutionIdUsingParentObject, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05091-136">-JobName</span><span class="sxs-lookup"><span data-stu-id="05091-136">-JobName</span></span>
<span data-ttu-id="05091-137">Jobbnamn.</span><span class="sxs-lookup"><span data-stu-id="05091-137">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WithJobExecutionId, WithJobExecutionIdUsingParentObject, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05091-138">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="05091-138">-ParentObject</span></span>
<span data-ttu-id="05091-139">Kör-ID för jobb.</span><span class="sxs-lookup"><span data-stu-id="05091-139">The job execution id.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet, WithJobExecutionIdUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05091-140">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="05091-140">-ParentResourceId</span></span>
<span data-ttu-id="05091-141">Agentens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="05091-141">The agent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05091-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05091-142">-ResourceGroupName</span></span>
<span data-ttu-id="05091-143">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="05091-143">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05091-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="05091-144">-ServerName</span></span>
<span data-ttu-id="05091-145">Server namnet.</span><span class="sxs-lookup"><span data-stu-id="05091-145">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05091-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05091-146">CommonParameters</span></span>
<span data-ttu-id="05091-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05091-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05091-148">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05091-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05091-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05091-149">INPUTS</span></span>

### <span data-ttu-id="05091-150">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="05091-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="05091-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05091-151">OUTPUTS</span></span>

### <span data-ttu-id="05091-152">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="05091-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="05091-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05091-153">NOTES</span></span>

## <span data-ttu-id="05091-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05091-154">RELATED LINKS</span></span>
