---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: e6853c3b4fa32a10e93ee281aab0b97755403671
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101877"
---
# <span data-ttu-id="29f6e-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="29f6e-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="29f6e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29f6e-102">SYNOPSIS</span></span>
<span data-ttu-id="29f6e-103">Skapar ett nytt jobb</span><span class="sxs-lookup"><span data-stu-id="29f6e-103">Creates a new job</span></span>

## <span data-ttu-id="29f6e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29f6e-104">SYNTAX</span></span>

### <span data-ttu-id="29f6e-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="29f6e-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29f6e-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="29f6e-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29f6e-107">Kommer</span><span class="sxs-lookup"><span data-stu-id="29f6e-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29f6e-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="29f6e-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29f6e-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="29f6e-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29f6e-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="29f6e-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29f6e-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="29f6e-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29f6e-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="29f6e-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29f6e-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="29f6e-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29f6e-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29f6e-114">DESCRIPTION</span></span>
<span data-ttu-id="29f6e-115">New-AzSqlElasticJob cmdlet skapar ett nytt jobb</span><span class="sxs-lookup"><span data-stu-id="29f6e-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="29f6e-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29f6e-116">EXAMPLES</span></span>

### <span data-ttu-id="29f6e-117">Exempel 1: skapar ett nytt jobb</span><span class="sxs-lookup"><span data-stu-id="29f6e-117">Example 1: Creates a new job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="29f6e-118">Skapar ett nytt jobb</span><span class="sxs-lookup"><span data-stu-id="29f6e-118">Creates a new job</span></span>

### <span data-ttu-id="29f6e-119">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="29f6e-119">Example 2</span></span>

<span data-ttu-id="29f6e-120">Skapar ett nytt jobb.</span><span class="sxs-lookup"><span data-stu-id="29f6e-120">Creates a new job.</span></span> <span data-ttu-id="29f6e-121">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="29f6e-121">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticJob -Name job1 -RunOnce
```

## <span data-ttu-id="29f6e-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29f6e-122">PARAMETERS</span></span>

### <span data-ttu-id="29f6e-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="29f6e-123">-AgentName</span></span>
<span data-ttu-id="29f6e-124">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="29f6e-124">The agent name</span></span>

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

### <span data-ttu-id="29f6e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29f6e-125">-DefaultProfile</span></span>
<span data-ttu-id="29f6e-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="29f6e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29f6e-127">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="29f6e-127">-Description</span></span>
<span data-ttu-id="29f6e-128">Beskrivning av jobbet</span><span class="sxs-lookup"><span data-stu-id="29f6e-128">The job description</span></span>

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

### <span data-ttu-id="29f6e-129">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="29f6e-129">-Enable</span></span>
<span data-ttu-id="29f6e-130">Flaggan som visar vilken kund som ska vara aktive rad.</span><span class="sxs-lookup"><span data-stu-id="29f6e-130">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="29f6e-131">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="29f6e-131">-EndTime</span></span>
<span data-ttu-id="29f6e-132">Slut tid för jobb schema</span><span class="sxs-lookup"><span data-stu-id="29f6e-132">The job schedule end time</span></span>

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

### <span data-ttu-id="29f6e-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="29f6e-133">-IntervalCount</span></span>
<span data-ttu-id="29f6e-134">Intervallet för återkommande schema</span><span class="sxs-lookup"><span data-stu-id="29f6e-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="29f6e-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="29f6e-135">-IntervalType</span></span>
<span data-ttu-id="29f6e-136">Det återkommande intervallet för schema – kan vara minut, timme, dag, vecka, månad</span><span class="sxs-lookup"><span data-stu-id="29f6e-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="29f6e-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="29f6e-137">-Name</span></span>
<span data-ttu-id="29f6e-138">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="29f6e-138">The job name</span></span>

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

### <span data-ttu-id="29f6e-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="29f6e-139">-ParentObject</span></span>
<span data-ttu-id="29f6e-140">Agent-indatavärdet</span><span class="sxs-lookup"><span data-stu-id="29f6e-140">The agent input object</span></span>

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

### <span data-ttu-id="29f6e-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="29f6e-141">-ParentResourceId</span></span>
<span data-ttu-id="29f6e-142">Agent resurs-ID</span><span class="sxs-lookup"><span data-stu-id="29f6e-142">The agent resource id</span></span>

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

### <span data-ttu-id="29f6e-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29f6e-143">-ResourceGroupName</span></span>
<span data-ttu-id="29f6e-144">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="29f6e-144">The resource group name</span></span>

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

### <span data-ttu-id="29f6e-145">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="29f6e-145">-RunOnce</span></span>
<span data-ttu-id="29f6e-146">Flaggan som visar att jobbet körs en gång</span><span class="sxs-lookup"><span data-stu-id="29f6e-146">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="29f6e-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="29f6e-147">-ServerName</span></span>
<span data-ttu-id="29f6e-148">Server namnet</span><span class="sxs-lookup"><span data-stu-id="29f6e-148">The server name</span></span>

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

### <span data-ttu-id="29f6e-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="29f6e-149">-StartTime</span></span>
<span data-ttu-id="29f6e-150">Start tiden för jobb schema</span><span class="sxs-lookup"><span data-stu-id="29f6e-150">The job schedule start time</span></span>

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

### <span data-ttu-id="29f6e-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="29f6e-151">-Confirm</span></span>
<span data-ttu-id="29f6e-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="29f6e-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29f6e-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29f6e-153">-WhatIf</span></span>
<span data-ttu-id="29f6e-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="29f6e-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29f6e-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="29f6e-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29f6e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29f6e-156">CommonParameters</span></span>
<span data-ttu-id="29f6e-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29f6e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29f6e-158">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29f6e-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29f6e-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29f6e-159">INPUTS</span></span>

### <span data-ttu-id="29f6e-160">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="29f6e-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="29f6e-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29f6e-161">OUTPUTS</span></span>

### <span data-ttu-id="29f6e-162">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="29f6e-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="29f6e-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29f6e-163">NOTES</span></span>

## <span data-ttu-id="29f6e-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29f6e-164">RELATED LINKS</span></span>
