---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: f39554dacdaabfc42fe44d55a7f3034c1c8b54df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927326"
---
# <span data-ttu-id="5caf8-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="5caf8-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="5caf8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5caf8-102">SYNOPSIS</span></span>
<span data-ttu-id="5caf8-103">Uppdaterar ett jobb steg</span><span class="sxs-lookup"><span data-stu-id="5caf8-103">Updates a job step</span></span>

## <span data-ttu-id="5caf8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5caf8-104">SYNTAX</span></span>

### <span data-ttu-id="5caf8-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5caf8-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5caf8-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="5caf8-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5caf8-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="5caf8-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5caf8-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="5caf8-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5caf8-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="5caf8-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5caf8-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="5caf8-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5caf8-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5caf8-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5caf8-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5caf8-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5caf8-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5caf8-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5caf8-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5caf8-114">DESCRIPTION</span></span>
<span data-ttu-id="5caf8-115">Set-AzSqlElasticJobStep cmdlet uppdaterar ett jobb steg</span><span class="sxs-lookup"><span data-stu-id="5caf8-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="5caf8-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5caf8-116">EXAMPLES</span></span>

### <span data-ttu-id="5caf8-117">Exempel 1 – uppdaterar mål gruppen för ett jobb för ett jobb</span><span class="sxs-lookup"><span data-stu-id="5caf8-117">Example 1 - Updates a job step's target group for a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="5caf8-118">Exempel 2 – uppdaterar ett Job-SQL-skript för ett jobb</span><span class="sxs-lookup"><span data-stu-id="5caf8-118">Example 2 - Updates a job step's T-SQL script for a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="5caf8-119">Uppdaterar ett jobb steg från ett jobb</span><span class="sxs-lookup"><span data-stu-id="5caf8-119">Updates a job step from a job</span></span>

## <span data-ttu-id="5caf8-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5caf8-120">PARAMETERS</span></span>

### <span data-ttu-id="5caf8-121">-AgentName</span><span class="sxs-lookup"><span data-stu-id="5caf8-121">-AgentName</span></span>
<span data-ttu-id="5caf8-122">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="5caf8-122">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5caf8-123">-CommandText</span><span class="sxs-lookup"><span data-stu-id="5caf8-123">-CommandText</span></span>
<span data-ttu-id="5caf8-124">Kommando texten</span><span class="sxs-lookup"><span data-stu-id="5caf8-124">The command text</span></span>

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

### <span data-ttu-id="5caf8-125">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="5caf8-125">-CredentialName</span></span>
<span data-ttu-id="5caf8-126">Namnet på autentiseringsuppgiften</span><span class="sxs-lookup"><span data-stu-id="5caf8-126">The credential name</span></span>

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

### <span data-ttu-id="5caf8-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5caf8-127">-DefaultProfile</span></span>
<span data-ttu-id="5caf8-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5caf8-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5caf8-129">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="5caf8-129">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="5caf8-130">Det första återförsöksintervall för försök</span><span class="sxs-lookup"><span data-stu-id="5caf8-130">The initial retry interval seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5caf8-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5caf8-131">-InputObject</span></span>
<span data-ttu-id="5caf8-132">Jobbobjektet-objekt</span><span class="sxs-lookup"><span data-stu-id="5caf8-132">The job step object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel
Parameter Sets: ObjectSet, WithRemoveOutputUsingParentObject, WithAddOutputUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5caf8-133">-JobName</span><span class="sxs-lookup"><span data-stu-id="5caf8-133">-JobName</span></span>
<span data-ttu-id="5caf8-134">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="5caf8-134">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5caf8-135">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="5caf8-135">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="5caf8-136">Maximalt antal sekunder för försök</span><span class="sxs-lookup"><span data-stu-id="5caf8-136">The maximum retry interval seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5caf8-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="5caf8-137">-Name</span></span>
<span data-ttu-id="5caf8-138">Stegets namn</span><span class="sxs-lookup"><span data-stu-id="5caf8-138">The step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5caf8-139">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="5caf8-139">-OutputCredentialName</span></span>
<span data-ttu-id="5caf8-140">Namnet på Uppgiftsutdata</span><span class="sxs-lookup"><span data-stu-id="5caf8-140">The output credential name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5caf8-141">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="5caf8-141">-OutputDatabaseObject</span></span>
<span data-ttu-id="5caf8-142">Objektet utgående databas</span><span class="sxs-lookup"><span data-stu-id="5caf8-142">The output database object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5caf8-143">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="5caf8-143">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="5caf8-144">Resurs-ID för utdatafil</span><span class="sxs-lookup"><span data-stu-id="5caf8-144">The output database resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithAddOutput, WithAddOutputUsingParentObject, WithAddOutputUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5caf8-145">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="5caf8-145">-OutputSchemaName</span></span>
<span data-ttu-id="5caf8-146">Namn på utdatafil</span><span class="sxs-lookup"><span data-stu-id="5caf8-146">The output schema name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5caf8-147">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="5caf8-147">-OutputTableName</span></span>
<span data-ttu-id="5caf8-148">Namn på resultat tabell</span><span class="sxs-lookup"><span data-stu-id="5caf8-148">The output table name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5caf8-149">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="5caf8-149">-RemoveOutput</span></span>
<span data-ttu-id="5caf8-150">Flagga som anger om utdata ska tas bort</span><span class="sxs-lookup"><span data-stu-id="5caf8-150">The flag to indicate whether to remove output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WithRemoveOutput, WithRemoveOutputUsingParentObject, WithRemoveOutputUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5caf8-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5caf8-151">-ResourceGroupName</span></span>
<span data-ttu-id="5caf8-152">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="5caf8-152">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5caf8-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5caf8-153">-ResourceId</span></span>
<span data-ttu-id="5caf8-154">Resurs-ID för jobb steg</span><span class="sxs-lookup"><span data-stu-id="5caf8-154">The job step resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithRemoveOutputUsingParentResourceId, WithAddOutputUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5caf8-155">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="5caf8-155">-RetryAttempts</span></span>
<span data-ttu-id="5caf8-156">Omförsöket attemps</span><span class="sxs-lookup"><span data-stu-id="5caf8-156">The retry attemps</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5caf8-157">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="5caf8-157">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="5caf8-158">Återförsöksintervall backoff multiplikator</span><span class="sxs-lookup"><span data-stu-id="5caf8-158">The retry interval backoff multiplier</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5caf8-159">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5caf8-159">-ServerName</span></span>
<span data-ttu-id="5caf8-160">Server namnet</span><span class="sxs-lookup"><span data-stu-id="5caf8-160">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5caf8-161">-StepId</span><span class="sxs-lookup"><span data-stu-id="5caf8-161">-StepId</span></span>
<span data-ttu-id="5caf8-162">Texten i steg-ID</span><span class="sxs-lookup"><span data-stu-id="5caf8-162">The step id text</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5caf8-163">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="5caf8-163">-TargetGroupName</span></span>
<span data-ttu-id="5caf8-164">Namnet på mål gruppen</span><span class="sxs-lookup"><span data-stu-id="5caf8-164">The target group name</span></span>

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

### <span data-ttu-id="5caf8-165">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="5caf8-165">-TimeoutSeconds</span></span>
<span data-ttu-id="5caf8-166">Timeout</span><span class="sxs-lookup"><span data-stu-id="5caf8-166">The timeout seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5caf8-167">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5caf8-167">-Confirm</span></span>
<span data-ttu-id="5caf8-168">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5caf8-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5caf8-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5caf8-169">-WhatIf</span></span>
<span data-ttu-id="5caf8-170">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5caf8-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5caf8-171">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5caf8-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5caf8-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5caf8-172">CommonParameters</span></span>
<span data-ttu-id="5caf8-173">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5caf8-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5caf8-174">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5caf8-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5caf8-175">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5caf8-175">INPUTS</span></span>

### <span data-ttu-id="5caf8-176">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="5caf8-176">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="5caf8-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5caf8-177">OUTPUTS</span></span>

### <span data-ttu-id="5caf8-178">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="5caf8-178">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="5caf8-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5caf8-179">NOTES</span></span>

## <span data-ttu-id="5caf8-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5caf8-180">RELATED LINKS</span></span>
