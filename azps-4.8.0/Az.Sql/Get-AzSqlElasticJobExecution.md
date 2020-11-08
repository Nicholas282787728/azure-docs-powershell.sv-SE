---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: d5583e5d7c0984b36679517859cc5a109b808a1a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259860"
---
# <span data-ttu-id="9d874-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="9d874-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="9d874-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9d874-102">SYNOPSIS</span></span>
<span data-ttu-id="9d874-103">Får ett eller flera jobb körningar</span><span class="sxs-lookup"><span data-stu-id="9d874-103">Gets one or more job executions</span></span>

## <span data-ttu-id="9d874-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9d874-104">SYNTAX</span></span>

### <span data-ttu-id="9d874-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9d874-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d874-106">WithJobExecutionId</span><span class="sxs-lookup"><span data-stu-id="9d874-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d874-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="9d874-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d874-108">WithJobExecutionIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="9d874-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d874-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9d874-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d874-110">WithJobExecutionIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9d874-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d874-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9d874-111">DESCRIPTION</span></span>
<span data-ttu-id="9d874-112">Get-AzSqlElasticJobExecution cmdlet får ett eller flera jobb körningar</span><span class="sxs-lookup"><span data-stu-id="9d874-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="9d874-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9d874-113">EXAMPLES</span></span>

### <span data-ttu-id="9d874-114">Exempel 1: hämtar ett eller flera jobb för alla jobb</span><span class="sxs-lookup"><span data-stu-id="9d874-114">Example 1: Gets one or more job executions across all jobs</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="9d874-115">Exempel 2: hämtar ett eller flera jobb för jobbet</span><span class="sxs-lookup"><span data-stu-id="9d874-115">Example 2: Gets one or more job executions for a job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="9d874-116">Får ett eller flera jobb körningar</span><span class="sxs-lookup"><span data-stu-id="9d874-116">Gets one or more job executions</span></span>

### <span data-ttu-id="9d874-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="9d874-117">Example 3</span></span>

<span data-ttu-id="9d874-118">Får ett eller flera jobb.</span><span class="sxs-lookup"><span data-stu-id="9d874-118">Gets one or more job executions.</span></span> <span data-ttu-id="9d874-119">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="9d874-119">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlElasticJobExecution -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1
```

## <span data-ttu-id="9d874-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9d874-120">PARAMETERS</span></span>

### <span data-ttu-id="9d874-121">-Aktiv</span><span class="sxs-lookup"><span data-stu-id="9d874-121">-Active</span></span>
<span data-ttu-id="9d874-122">Filtrera efter skapa tid</span><span class="sxs-lookup"><span data-stu-id="9d874-122">Filter by create time min</span></span>

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

### <span data-ttu-id="9d874-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="9d874-123">-AgentName</span></span>
<span data-ttu-id="9d874-124">Namnet på agenten.</span><span class="sxs-lookup"><span data-stu-id="9d874-124">The agent name.</span></span>

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

### <span data-ttu-id="9d874-125">-Antal</span><span class="sxs-lookup"><span data-stu-id="9d874-125">-Count</span></span>
<span data-ttu-id="9d874-126">COUNT returnerar det högsta antalet körningar.</span><span class="sxs-lookup"><span data-stu-id="9d874-126">Count returns the top number of executions.</span></span>

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

### <span data-ttu-id="9d874-127">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="9d874-127">-CreateTimeMax</span></span>
<span data-ttu-id="9d874-128">Filtrera efter skapa tid</span><span class="sxs-lookup"><span data-stu-id="9d874-128">Filter by create time min</span></span>

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

### <span data-ttu-id="9d874-129">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="9d874-129">-CreateTimeMin</span></span>
<span data-ttu-id="9d874-130">Filtrera efter skapa tid</span><span class="sxs-lookup"><span data-stu-id="9d874-130">Filter by create time min</span></span>

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

### <span data-ttu-id="9d874-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d874-131">-DefaultProfile</span></span>
<span data-ttu-id="9d874-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9d874-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d874-133">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="9d874-133">-EndTimeMax</span></span>
<span data-ttu-id="9d874-134">Filtrera efter skapa tid</span><span class="sxs-lookup"><span data-stu-id="9d874-134">Filter by create time min</span></span>

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

### <span data-ttu-id="9d874-135">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="9d874-135">-EndTimeMin</span></span>
<span data-ttu-id="9d874-136">Filtrera efter skapa tid</span><span class="sxs-lookup"><span data-stu-id="9d874-136">Filter by create time min</span></span>

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

### <span data-ttu-id="9d874-137">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="9d874-137">-JobExecutionId</span></span>
<span data-ttu-id="9d874-138">Kör-ID för jobb.</span><span class="sxs-lookup"><span data-stu-id="9d874-138">The job execution id.</span></span>

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

### <span data-ttu-id="9d874-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="9d874-139">-JobName</span></span>
<span data-ttu-id="9d874-140">Jobbnamn.</span><span class="sxs-lookup"><span data-stu-id="9d874-140">The job name.</span></span>

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

### <span data-ttu-id="9d874-141">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9d874-141">-ParentObject</span></span>
<span data-ttu-id="9d874-142">Kör-ID för jobb.</span><span class="sxs-lookup"><span data-stu-id="9d874-142">The job execution id.</span></span>

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

### <span data-ttu-id="9d874-143">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9d874-143">-ParentResourceId</span></span>
<span data-ttu-id="9d874-144">Agentens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="9d874-144">The agent resource id.</span></span>

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

### <span data-ttu-id="9d874-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d874-145">-ResourceGroupName</span></span>
<span data-ttu-id="9d874-146">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="9d874-146">The resource group name.</span></span>

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

### <span data-ttu-id="9d874-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9d874-147">-ServerName</span></span>
<span data-ttu-id="9d874-148">Server namnet.</span><span class="sxs-lookup"><span data-stu-id="9d874-148">The server name.</span></span>

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

### <span data-ttu-id="9d874-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d874-149">CommonParameters</span></span>
<span data-ttu-id="9d874-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d874-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d874-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d874-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d874-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9d874-152">INPUTS</span></span>

### <span data-ttu-id="9d874-153">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="9d874-153">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="9d874-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9d874-154">OUTPUTS</span></span>

### <span data-ttu-id="9d874-155">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="9d874-155">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="9d874-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9d874-156">NOTES</span></span>

## <span data-ttu-id="9d874-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9d874-157">RELATED LINKS</span></span>
