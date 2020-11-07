---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 04f182cb410e77a9ca61aa6f80da14c08e517406
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920446"
---
# <span data-ttu-id="c62fa-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="c62fa-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="c62fa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c62fa-102">SYNOPSIS</span></span>
<span data-ttu-id="c62fa-103">Uppdaterar ett jobb</span><span class="sxs-lookup"><span data-stu-id="c62fa-103">Updates a job</span></span>

## <span data-ttu-id="c62fa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c62fa-104">SYNTAX</span></span>

### <span data-ttu-id="c62fa-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c62fa-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c62fa-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="c62fa-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c62fa-107">Kommer</span><span class="sxs-lookup"><span data-stu-id="c62fa-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c62fa-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="c62fa-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c62fa-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="c62fa-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c62fa-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="c62fa-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c62fa-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c62fa-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c62fa-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c62fa-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c62fa-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c62fa-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c62fa-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c62fa-114">DESCRIPTION</span></span>
<span data-ttu-id="c62fa-115">Set-AzSqlElasticJob cmdlet uppdaterar ett jobb</span><span class="sxs-lookup"><span data-stu-id="c62fa-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="c62fa-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c62fa-116">EXAMPLES</span></span>

### <span data-ttu-id="c62fa-117">Exempel 1-uppdaterar ett jobb för att starta en timme från och med Upprepa 1 timme</span><span class="sxs-lookup"><span data-stu-id="c62fa-117">Example 1 - Updates a job to start an hour from now and repeat every 1 hour</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="c62fa-118">Uppdaterar ett jobb</span><span class="sxs-lookup"><span data-stu-id="c62fa-118">Updates a job</span></span>

## <span data-ttu-id="c62fa-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c62fa-119">PARAMETERS</span></span>

### <span data-ttu-id="c62fa-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="c62fa-120">-AgentName</span></span>
<span data-ttu-id="c62fa-121">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="c62fa-121">The agent name</span></span>

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

### <span data-ttu-id="c62fa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c62fa-122">-DefaultProfile</span></span>
<span data-ttu-id="c62fa-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c62fa-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c62fa-124">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="c62fa-124">-Description</span></span>
<span data-ttu-id="c62fa-125">Beskrivning av jobbet</span><span class="sxs-lookup"><span data-stu-id="c62fa-125">The job description</span></span>

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

### <span data-ttu-id="c62fa-126">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="c62fa-126">-Enable</span></span>
<span data-ttu-id="c62fa-127">Flaggan som visar vilken kund som ska vara aktive rad.</span><span class="sxs-lookup"><span data-stu-id="c62fa-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="c62fa-128">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="c62fa-128">-EndTime</span></span>
<span data-ttu-id="c62fa-129">Slut tid för jobb schema</span><span class="sxs-lookup"><span data-stu-id="c62fa-129">The job schedule end time</span></span>

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

### <span data-ttu-id="c62fa-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c62fa-130">-InputObject</span></span>
<span data-ttu-id="c62fa-131">Jobbobjektet</span><span class="sxs-lookup"><span data-stu-id="c62fa-131">The job input object</span></span>

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

### <span data-ttu-id="c62fa-132">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="c62fa-132">-IntervalCount</span></span>
<span data-ttu-id="c62fa-133">Intervallet för återkommande schema</span><span class="sxs-lookup"><span data-stu-id="c62fa-133">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="c62fa-134">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="c62fa-134">-IntervalType</span></span>
<span data-ttu-id="c62fa-135">Det återkommande intervallet för schema – kan vara minut, timme, dag, vecka, månad</span><span class="sxs-lookup"><span data-stu-id="c62fa-135">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="c62fa-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="c62fa-136">-Name</span></span>
<span data-ttu-id="c62fa-137">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="c62fa-137">The job name</span></span>

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

### <span data-ttu-id="c62fa-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c62fa-138">-ResourceGroupName</span></span>
<span data-ttu-id="c62fa-139">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="c62fa-139">The resource group name</span></span>

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

### <span data-ttu-id="c62fa-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c62fa-140">-ResourceId</span></span>
<span data-ttu-id="c62fa-141">Jobb resurs-ID</span><span class="sxs-lookup"><span data-stu-id="c62fa-141">The job resource id</span></span>

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

### <span data-ttu-id="c62fa-142">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="c62fa-142">-RunOnce</span></span>
<span data-ttu-id="c62fa-143">Flaggan som visar att jobbet körs en gång</span><span class="sxs-lookup"><span data-stu-id="c62fa-143">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="c62fa-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c62fa-144">-ServerName</span></span>
<span data-ttu-id="c62fa-145">Server namnet</span><span class="sxs-lookup"><span data-stu-id="c62fa-145">The server name</span></span>

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

### <span data-ttu-id="c62fa-146">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c62fa-146">-StartTime</span></span>
<span data-ttu-id="c62fa-147">Start tiden för jobb schema</span><span class="sxs-lookup"><span data-stu-id="c62fa-147">The job schedule start time</span></span>

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

### <span data-ttu-id="c62fa-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c62fa-148">-Confirm</span></span>
<span data-ttu-id="c62fa-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c62fa-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c62fa-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c62fa-150">-WhatIf</span></span>
<span data-ttu-id="c62fa-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c62fa-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c62fa-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c62fa-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c62fa-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c62fa-153">CommonParameters</span></span>
<span data-ttu-id="c62fa-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c62fa-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c62fa-155">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c62fa-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c62fa-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c62fa-156">INPUTS</span></span>

### <span data-ttu-id="c62fa-157">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="c62fa-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="c62fa-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c62fa-158">OUTPUTS</span></span>

### <span data-ttu-id="c62fa-159">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="c62fa-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="c62fa-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c62fa-160">NOTES</span></span>

## <span data-ttu-id="c62fa-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c62fa-161">RELATED LINKS</span></span>
