---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 53bd1b1cd1c2f7ba87df8cb5c27f1b2380db04af
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272821"
---
# <span data-ttu-id="acd7a-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="acd7a-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="acd7a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="acd7a-102">SYNOPSIS</span></span>
<span data-ttu-id="acd7a-103">Uppdaterar ett jobb</span><span class="sxs-lookup"><span data-stu-id="acd7a-103">Updates a job</span></span>

## <span data-ttu-id="acd7a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="acd7a-104">SYNTAX</span></span>

### <span data-ttu-id="acd7a-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="acd7a-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acd7a-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="acd7a-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acd7a-107">Kommer</span><span class="sxs-lookup"><span data-stu-id="acd7a-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acd7a-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="acd7a-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="acd7a-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="acd7a-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acd7a-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="acd7a-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acd7a-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="acd7a-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acd7a-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="acd7a-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acd7a-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="acd7a-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acd7a-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="acd7a-114">DESCRIPTION</span></span>
<span data-ttu-id="acd7a-115">Set-AzSqlElasticJob cmdlet uppdaterar ett jobb</span><span class="sxs-lookup"><span data-stu-id="acd7a-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="acd7a-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="acd7a-116">EXAMPLES</span></span>

### <span data-ttu-id="acd7a-117">Exempel 1: uppdaterar ett jobb för att starta en timme från och med Upprepa 1 timme</span><span class="sxs-lookup"><span data-stu-id="acd7a-117">Example 1: Updates a job to start an hour from now and repeat every 1 hour</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="acd7a-118">Uppdaterar ett jobb</span><span class="sxs-lookup"><span data-stu-id="acd7a-118">Updates a job</span></span>

### <span data-ttu-id="acd7a-119">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="acd7a-119">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJob -AgentName agent -Enable -IntervalCount 1 -IntervalType Hour -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1 -StartTime '9/16/2016 11:31:12'
```

## <span data-ttu-id="acd7a-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="acd7a-120">PARAMETERS</span></span>

### <span data-ttu-id="acd7a-121">-AgentName</span><span class="sxs-lookup"><span data-stu-id="acd7a-121">-AgentName</span></span>
<span data-ttu-id="acd7a-122">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="acd7a-122">The agent name</span></span>

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

### <span data-ttu-id="acd7a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acd7a-123">-DefaultProfile</span></span>
<span data-ttu-id="acd7a-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="acd7a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acd7a-125">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="acd7a-125">-Description</span></span>
<span data-ttu-id="acd7a-126">Beskrivning av jobbet</span><span class="sxs-lookup"><span data-stu-id="acd7a-126">The job description</span></span>

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

### <span data-ttu-id="acd7a-127">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="acd7a-127">-Enable</span></span>
<span data-ttu-id="acd7a-128">Flaggan som visar vilken kund som ska vara aktive rad.</span><span class="sxs-lookup"><span data-stu-id="acd7a-128">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="acd7a-129">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="acd7a-129">-EndTime</span></span>
<span data-ttu-id="acd7a-130">Slut tid för jobb schema</span><span class="sxs-lookup"><span data-stu-id="acd7a-130">The job schedule end time</span></span>

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

### <span data-ttu-id="acd7a-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acd7a-131">-InputObject</span></span>
<span data-ttu-id="acd7a-132">Jobbobjektet</span><span class="sxs-lookup"><span data-stu-id="acd7a-132">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, RunOnceUsingParentObject, RecurringUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acd7a-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="acd7a-133">-IntervalCount</span></span>
<span data-ttu-id="acd7a-134">Intervallet för återkommande schema</span><span class="sxs-lookup"><span data-stu-id="acd7a-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="acd7a-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="acd7a-135">-IntervalType</span></span>
<span data-ttu-id="acd7a-136">Det återkommande intervallet för schema – kan vara minut, timme, dag, vecka, månad</span><span class="sxs-lookup"><span data-stu-id="acd7a-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="acd7a-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="acd7a-137">-Name</span></span>
<span data-ttu-id="acd7a-138">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="acd7a-138">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd7a-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acd7a-139">-ResourceGroupName</span></span>
<span data-ttu-id="acd7a-140">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="acd7a-140">The resource group name</span></span>

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

### <span data-ttu-id="acd7a-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acd7a-141">-ResourceId</span></span>
<span data-ttu-id="acd7a-142">Jobb resurs-ID</span><span class="sxs-lookup"><span data-stu-id="acd7a-142">The job resource id</span></span>

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

### <span data-ttu-id="acd7a-143">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="acd7a-143">-RunOnce</span></span>
<span data-ttu-id="acd7a-144">Flaggan som visar att jobbet körs en gång</span><span class="sxs-lookup"><span data-stu-id="acd7a-144">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="acd7a-145">-ServerName</span><span class="sxs-lookup"><span data-stu-id="acd7a-145">-ServerName</span></span>
<span data-ttu-id="acd7a-146">Server namnet</span><span class="sxs-lookup"><span data-stu-id="acd7a-146">The server name</span></span>

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

### <span data-ttu-id="acd7a-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="acd7a-147">-StartTime</span></span>
<span data-ttu-id="acd7a-148">Start tiden för jobb schema</span><span class="sxs-lookup"><span data-stu-id="acd7a-148">The job schedule start time</span></span>

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

### <span data-ttu-id="acd7a-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="acd7a-149">-Confirm</span></span>
<span data-ttu-id="acd7a-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="acd7a-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acd7a-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acd7a-151">-WhatIf</span></span>
<span data-ttu-id="acd7a-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="acd7a-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acd7a-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="acd7a-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acd7a-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acd7a-154">CommonParameters</span></span>
<span data-ttu-id="acd7a-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acd7a-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acd7a-156">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="acd7a-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acd7a-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="acd7a-157">INPUTS</span></span>

### <span data-ttu-id="acd7a-158">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="acd7a-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="acd7a-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="acd7a-159">OUTPUTS</span></span>

### <span data-ttu-id="acd7a-160">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="acd7a-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="acd7a-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="acd7a-161">NOTES</span></span>

## <span data-ttu-id="acd7a-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="acd7a-162">RELATED LINKS</span></span>