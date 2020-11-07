---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: 29ae424807b8648238e2cc855fb90734773e870d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920307"
---
# <span data-ttu-id="6fb24-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="6fb24-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="6fb24-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6fb24-102">SYNOPSIS</span></span>
<span data-ttu-id="6fb24-103">Skapar ett nytt jobb</span><span class="sxs-lookup"><span data-stu-id="6fb24-103">Creates a new job</span></span>

## <span data-ttu-id="6fb24-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6fb24-104">SYNTAX</span></span>

### <span data-ttu-id="6fb24-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6fb24-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6fb24-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="6fb24-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fb24-107">Kommer</span><span class="sxs-lookup"><span data-stu-id="6fb24-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6fb24-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="6fb24-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fb24-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="6fb24-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fb24-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="6fb24-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fb24-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6fb24-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fb24-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6fb24-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6fb24-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6fb24-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fb24-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6fb24-114">DESCRIPTION</span></span>
<span data-ttu-id="6fb24-115">New-AzSqlElasticJob cmdlet skapar ett nytt jobb</span><span class="sxs-lookup"><span data-stu-id="6fb24-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="6fb24-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6fb24-116">EXAMPLES</span></span>

### <span data-ttu-id="6fb24-117">Exempel 1-skapar ett nytt jobb</span><span class="sxs-lookup"><span data-stu-id="6fb24-117">Example 1 - Creates a new job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="6fb24-118">Skapar ett nytt jobb</span><span class="sxs-lookup"><span data-stu-id="6fb24-118">Creates a new job</span></span>

## <span data-ttu-id="6fb24-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6fb24-119">PARAMETERS</span></span>

### <span data-ttu-id="6fb24-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="6fb24-120">-AgentName</span></span>
<span data-ttu-id="6fb24-121">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="6fb24-121">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fb24-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fb24-122">-DefaultProfile</span></span>
<span data-ttu-id="6fb24-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6fb24-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fb24-124">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="6fb24-124">-Description</span></span>
<span data-ttu-id="6fb24-125">Beskrivning av jobbet</span><span class="sxs-lookup"><span data-stu-id="6fb24-125">The job description</span></span>

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

### <span data-ttu-id="6fb24-126">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="6fb24-126">-Enable</span></span>
<span data-ttu-id="6fb24-127">Flaggan som visar vilken kund som ska vara aktive rad.</span><span class="sxs-lookup"><span data-stu-id="6fb24-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="6fb24-128">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="6fb24-128">-EndTime</span></span>
<span data-ttu-id="6fb24-129">Slut tid för jobb schema</span><span class="sxs-lookup"><span data-stu-id="6fb24-129">The job schedule end time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fb24-130">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="6fb24-130">-IntervalCount</span></span>
<span data-ttu-id="6fb24-131">Intervallet för återkommande schema</span><span class="sxs-lookup"><span data-stu-id="6fb24-131">The recurring schedule interval count</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fb24-132">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="6fb24-132">-IntervalType</span></span>
<span data-ttu-id="6fb24-133">Det återkommande intervallet för schema – kan vara minut, timme, dag, vecka, månad</span><span class="sxs-lookup"><span data-stu-id="6fb24-133">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

```yaml
Type: System.String
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fb24-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="6fb24-134">-Name</span></span>
<span data-ttu-id="6fb24-135">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="6fb24-135">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fb24-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6fb24-136">-ParentObject</span></span>
<span data-ttu-id="6fb24-137">Agent-indatavärdet</span><span class="sxs-lookup"><span data-stu-id="6fb24-137">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet, RunOnceUsingParentObject, RecurringUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fb24-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6fb24-138">-ParentResourceId</span></span>
<span data-ttu-id="6fb24-139">Agent resurs-ID</span><span class="sxs-lookup"><span data-stu-id="6fb24-139">The agent resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, RunOnceUsingParentResourceId, RecurringUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fb24-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fb24-140">-ResourceGroupName</span></span>
<span data-ttu-id="6fb24-141">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="6fb24-141">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fb24-142">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="6fb24-142">-RunOnce</span></span>
<span data-ttu-id="6fb24-143">Flaggan som visar att jobbet körs en gång</span><span class="sxs-lookup"><span data-stu-id="6fb24-143">The flag to indicate job will be run once</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RunOnce, RunOnceUsingParentObject, RunOnceUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fb24-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6fb24-144">-ServerName</span></span>
<span data-ttu-id="6fb24-145">Server namnet</span><span class="sxs-lookup"><span data-stu-id="6fb24-145">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fb24-146">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6fb24-146">-StartTime</span></span>
<span data-ttu-id="6fb24-147">Start tiden för jobb schema</span><span class="sxs-lookup"><span data-stu-id="6fb24-147">The job schedule start time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: RunOnce, Recurring, RunOnceUsingParentObject, RecurringUsingParentObject, RunOnceUsingParentResourceId, RecurringUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fb24-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6fb24-148">-Confirm</span></span>
<span data-ttu-id="6fb24-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6fb24-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fb24-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fb24-150">-WhatIf</span></span>
<span data-ttu-id="6fb24-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6fb24-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fb24-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6fb24-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fb24-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fb24-153">CommonParameters</span></span>
<span data-ttu-id="6fb24-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fb24-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fb24-155">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6fb24-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fb24-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6fb24-156">INPUTS</span></span>

### <span data-ttu-id="6fb24-157">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="6fb24-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="6fb24-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6fb24-158">OUTPUTS</span></span>

### <span data-ttu-id="6fb24-159">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="6fb24-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="6fb24-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6fb24-160">NOTES</span></span>

## <span data-ttu-id="6fb24-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6fb24-161">RELATED LINKS</span></span>
