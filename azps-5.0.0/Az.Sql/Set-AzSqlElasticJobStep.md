---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: 4f6f0471224799e818f9db29e5be5a4c49f9c45e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325026"
---
# <span data-ttu-id="5ffe4-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="5ffe4-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="5ffe4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ffe4-102">SYNOPSIS</span></span>
<span data-ttu-id="5ffe4-103">Uppdaterar ett jobb steg</span><span class="sxs-lookup"><span data-stu-id="5ffe4-103">Updates a job step</span></span>

## <span data-ttu-id="5ffe4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ffe4-104">SYNTAX</span></span>

### <span data-ttu-id="5ffe4-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5ffe4-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ffe4-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="5ffe4-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ffe4-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="5ffe4-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ffe4-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="5ffe4-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ffe4-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="5ffe4-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ffe4-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="5ffe4-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ffe4-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5ffe4-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ffe4-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5ffe4-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ffe4-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5ffe4-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ffe4-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ffe4-114">DESCRIPTION</span></span>
<span data-ttu-id="5ffe4-115">Set-AzSqlElasticJobStep cmdlet uppdaterar ett jobb steg</span><span class="sxs-lookup"><span data-stu-id="5ffe4-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="5ffe4-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ffe4-116">EXAMPLES</span></span>

### <span data-ttu-id="5ffe4-117">Exempel 1: uppdaterar mål gruppen för ett jobb för ett jobb</span><span class="sxs-lookup"><span data-stu-id="5ffe4-117">Example 1: Updates a job step's target group for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="5ffe4-118">Exempel 2: uppdaterar ett jobb-SQL-skript för ett jobb</span><span class="sxs-lookup"><span data-stu-id="5ffe4-118">Example 2: Updates a job step's T-SQL script for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="5ffe4-119">Uppdaterar ett jobb steg från ett jobb</span><span class="sxs-lookup"><span data-stu-id="5ffe4-119">Updates a job step from a job</span></span>

### <span data-ttu-id="5ffe4-120">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="5ffe4-120">Example 3</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJobStep -AgentName agent -CommandText 'SELECT 2' -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="5ffe4-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ffe4-121">PARAMETERS</span></span>

### <span data-ttu-id="5ffe4-122">-AgentName</span><span class="sxs-lookup"><span data-stu-id="5ffe4-122">-AgentName</span></span>
<span data-ttu-id="5ffe4-123">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="5ffe4-123">The agent name</span></span>

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

### <span data-ttu-id="5ffe4-124">-CommandText</span><span class="sxs-lookup"><span data-stu-id="5ffe4-124">-CommandText</span></span>
<span data-ttu-id="5ffe4-125">Kommando texten</span><span class="sxs-lookup"><span data-stu-id="5ffe4-125">The command text</span></span>

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

### <span data-ttu-id="5ffe4-126">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="5ffe4-126">-CredentialName</span></span>
<span data-ttu-id="5ffe4-127">Namnet på autentiseringsuppgiften</span><span class="sxs-lookup"><span data-stu-id="5ffe4-127">The credential name</span></span>

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

### <span data-ttu-id="5ffe4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ffe4-128">-DefaultProfile</span></span>
<span data-ttu-id="5ffe4-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ffe4-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ffe4-130">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="5ffe4-130">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="5ffe4-131">Det första återförsöksintervall för försök</span><span class="sxs-lookup"><span data-stu-id="5ffe4-131">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="5ffe4-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ffe4-132">-InputObject</span></span>
<span data-ttu-id="5ffe4-133">Jobbobjektet-objekt</span><span class="sxs-lookup"><span data-stu-id="5ffe4-133">The job step object</span></span>

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

### <span data-ttu-id="5ffe4-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="5ffe4-134">-JobName</span></span>
<span data-ttu-id="5ffe4-135">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="5ffe4-135">The job name</span></span>

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

### <span data-ttu-id="5ffe4-136">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="5ffe4-136">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="5ffe4-137">Maximalt antal sekunder för försök</span><span class="sxs-lookup"><span data-stu-id="5ffe4-137">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="5ffe4-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="5ffe4-138">-Name</span></span>
<span data-ttu-id="5ffe4-139">Stegets namn</span><span class="sxs-lookup"><span data-stu-id="5ffe4-139">The step name</span></span>

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

### <span data-ttu-id="5ffe4-140">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="5ffe4-140">-OutputCredentialName</span></span>
<span data-ttu-id="5ffe4-141">Namnet på Uppgiftsutdata</span><span class="sxs-lookup"><span data-stu-id="5ffe4-141">The output credential name</span></span>

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

### <span data-ttu-id="5ffe4-142">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="5ffe4-142">-OutputDatabaseObject</span></span>
<span data-ttu-id="5ffe4-143">Objektet utgående databas</span><span class="sxs-lookup"><span data-stu-id="5ffe4-143">The output database object</span></span>

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

### <span data-ttu-id="5ffe4-144">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="5ffe4-144">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="5ffe4-145">Resurs-ID för utdatafil</span><span class="sxs-lookup"><span data-stu-id="5ffe4-145">The output database resource id</span></span>

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

### <span data-ttu-id="5ffe4-146">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="5ffe4-146">-OutputSchemaName</span></span>
<span data-ttu-id="5ffe4-147">Namn på utdatafil</span><span class="sxs-lookup"><span data-stu-id="5ffe4-147">The output schema name</span></span>

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

### <span data-ttu-id="5ffe4-148">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="5ffe4-148">-OutputTableName</span></span>
<span data-ttu-id="5ffe4-149">Namn på resultat tabell</span><span class="sxs-lookup"><span data-stu-id="5ffe4-149">The output table name</span></span>

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

### <span data-ttu-id="5ffe4-150">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="5ffe4-150">-RemoveOutput</span></span>
<span data-ttu-id="5ffe4-151">Flagga som anger om utdata ska tas bort</span><span class="sxs-lookup"><span data-stu-id="5ffe4-151">The flag to indicate whether to remove output</span></span>

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

### <span data-ttu-id="5ffe4-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ffe4-152">-ResourceGroupName</span></span>
<span data-ttu-id="5ffe4-153">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="5ffe4-153">The resource group name</span></span>

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

### <span data-ttu-id="5ffe4-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ffe4-154">-ResourceId</span></span>
<span data-ttu-id="5ffe4-155">Resurs-ID för jobb steg</span><span class="sxs-lookup"><span data-stu-id="5ffe4-155">The job step resource id</span></span>

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

### <span data-ttu-id="5ffe4-156">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="5ffe4-156">-RetryAttempts</span></span>
<span data-ttu-id="5ffe4-157">Omförsöket attemps</span><span class="sxs-lookup"><span data-stu-id="5ffe4-157">The retry attemps</span></span>

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

### <span data-ttu-id="5ffe4-158">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="5ffe4-158">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="5ffe4-159">Återförsöksintervall backoff multiplikator</span><span class="sxs-lookup"><span data-stu-id="5ffe4-159">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="5ffe4-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5ffe4-160">-ServerName</span></span>
<span data-ttu-id="5ffe4-161">Server namnet</span><span class="sxs-lookup"><span data-stu-id="5ffe4-161">The server name</span></span>

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

### <span data-ttu-id="5ffe4-162">-StepId</span><span class="sxs-lookup"><span data-stu-id="5ffe4-162">-StepId</span></span>
<span data-ttu-id="5ffe4-163">Texten i steg-ID</span><span class="sxs-lookup"><span data-stu-id="5ffe4-163">The step id text</span></span>

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

### <span data-ttu-id="5ffe4-164">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="5ffe4-164">-TargetGroupName</span></span>
<span data-ttu-id="5ffe4-165">Namnet på mål gruppen</span><span class="sxs-lookup"><span data-stu-id="5ffe4-165">The target group name</span></span>

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

### <span data-ttu-id="5ffe4-166">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="5ffe4-166">-TimeoutSeconds</span></span>
<span data-ttu-id="5ffe4-167">Timeout</span><span class="sxs-lookup"><span data-stu-id="5ffe4-167">The timeout seconds</span></span>

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

### <span data-ttu-id="5ffe4-168">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5ffe4-168">-Confirm</span></span>
<span data-ttu-id="5ffe4-169">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5ffe4-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ffe4-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ffe4-170">-WhatIf</span></span>
<span data-ttu-id="5ffe4-171">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5ffe4-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ffe4-172">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5ffe4-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ffe4-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ffe4-173">CommonParameters</span></span>
<span data-ttu-id="5ffe4-174">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ffe4-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ffe4-175">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ffe4-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ffe4-176">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ffe4-176">INPUTS</span></span>

### <span data-ttu-id="5ffe4-177">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="5ffe4-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="5ffe4-178">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ffe4-178">OUTPUTS</span></span>

### <span data-ttu-id="5ffe4-179">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="5ffe4-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="5ffe4-180">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ffe4-180">NOTES</span></span>

## <span data-ttu-id="5ffe4-181">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ffe4-181">RELATED LINKS</span></span>
