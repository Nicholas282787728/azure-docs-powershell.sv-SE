---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: a53a982e13b84bb401389e5edb5294ef1d094a49
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927181"
---
# <span data-ttu-id="cb808-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="cb808-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="cb808-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb808-102">SYNOPSIS</span></span>
<span data-ttu-id="cb808-103">Uppdaterar ett jobb</span><span class="sxs-lookup"><span data-stu-id="cb808-103">Updates a job</span></span>

## <span data-ttu-id="cb808-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb808-104">SYNTAX</span></span>

### <span data-ttu-id="cb808-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="cb808-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb808-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="cb808-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb808-107">Kommer</span><span class="sxs-lookup"><span data-stu-id="cb808-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb808-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="cb808-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb808-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="cb808-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb808-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="cb808-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb808-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cb808-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb808-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="cb808-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb808-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="cb808-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb808-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb808-114">DESCRIPTION</span></span>
<span data-ttu-id="cb808-115">Set-AzSqlElasticJob cmdlet uppdaterar ett jobb</span><span class="sxs-lookup"><span data-stu-id="cb808-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="cb808-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb808-116">EXAMPLES</span></span>

### <span data-ttu-id="cb808-117">Exempel 1-uppdaterar ett jobb för att starta en timme från och med Upprepa 1 timme</span><span class="sxs-lookup"><span data-stu-id="cb808-117">Example 1 - Updates a job to start an hour from now and repeat every 1 hour</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="cb808-118">Uppdaterar ett jobb</span><span class="sxs-lookup"><span data-stu-id="cb808-118">Updates a job</span></span>

## <span data-ttu-id="cb808-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb808-119">PARAMETERS</span></span>

### <span data-ttu-id="cb808-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="cb808-120">-AgentName</span></span>
<span data-ttu-id="cb808-121">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="cb808-121">The agent name</span></span>

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

### <span data-ttu-id="cb808-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb808-122">-DefaultProfile</span></span>
<span data-ttu-id="cb808-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cb808-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb808-124">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="cb808-124">-Description</span></span>
<span data-ttu-id="cb808-125">Beskrivning av jobbet</span><span class="sxs-lookup"><span data-stu-id="cb808-125">The job description</span></span>

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

### <span data-ttu-id="cb808-126">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="cb808-126">-Enable</span></span>
<span data-ttu-id="cb808-127">Flaggan som visar vilken kund som ska vara aktive rad.</span><span class="sxs-lookup"><span data-stu-id="cb808-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="cb808-128">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="cb808-128">-EndTime</span></span>
<span data-ttu-id="cb808-129">Slut tid för jobb schema</span><span class="sxs-lookup"><span data-stu-id="cb808-129">The job schedule end time</span></span>

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

### <span data-ttu-id="cb808-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb808-130">-InputObject</span></span>
<span data-ttu-id="cb808-131">Jobbobjektet</span><span class="sxs-lookup"><span data-stu-id="cb808-131">The job input object</span></span>

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

### <span data-ttu-id="cb808-132">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="cb808-132">-IntervalCount</span></span>
<span data-ttu-id="cb808-133">Intervallet för återkommande schema</span><span class="sxs-lookup"><span data-stu-id="cb808-133">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="cb808-134">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="cb808-134">-IntervalType</span></span>
<span data-ttu-id="cb808-135">Det återkommande intervallet för schema – kan vara minut, timme, dag, vecka, månad</span><span class="sxs-lookup"><span data-stu-id="cb808-135">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="cb808-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="cb808-136">-Name</span></span>
<span data-ttu-id="cb808-137">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="cb808-137">The job name</span></span>

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

### <span data-ttu-id="cb808-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb808-138">-ResourceGroupName</span></span>
<span data-ttu-id="cb808-139">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="cb808-139">The resource group name</span></span>

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

### <span data-ttu-id="cb808-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb808-140">-ResourceId</span></span>
<span data-ttu-id="cb808-141">Jobb resurs-ID</span><span class="sxs-lookup"><span data-stu-id="cb808-141">The job resource id</span></span>

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

### <span data-ttu-id="cb808-142">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="cb808-142">-RunOnce</span></span>
<span data-ttu-id="cb808-143">Flaggan som visar att jobbet körs en gång</span><span class="sxs-lookup"><span data-stu-id="cb808-143">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="cb808-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cb808-144">-ServerName</span></span>
<span data-ttu-id="cb808-145">Server namnet</span><span class="sxs-lookup"><span data-stu-id="cb808-145">The server name</span></span>

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

### <span data-ttu-id="cb808-146">-StartTime</span><span class="sxs-lookup"><span data-stu-id="cb808-146">-StartTime</span></span>
<span data-ttu-id="cb808-147">Start tiden för jobb schema</span><span class="sxs-lookup"><span data-stu-id="cb808-147">The job schedule start time</span></span>

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

### <span data-ttu-id="cb808-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cb808-148">-Confirm</span></span>
<span data-ttu-id="cb808-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cb808-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb808-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb808-150">-WhatIf</span></span>
<span data-ttu-id="cb808-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cb808-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb808-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cb808-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb808-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb808-153">CommonParameters</span></span>
<span data-ttu-id="cb808-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb808-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb808-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb808-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb808-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb808-156">INPUTS</span></span>

### <span data-ttu-id="cb808-157">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="cb808-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="cb808-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb808-158">OUTPUTS</span></span>

### <span data-ttu-id="cb808-159">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="cb808-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="cb808-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb808-160">NOTES</span></span>

## <span data-ttu-id="cb808-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb808-161">RELATED LINKS</span></span>
