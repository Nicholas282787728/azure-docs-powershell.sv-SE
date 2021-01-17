---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: dbc27ec87be3de4c320ad60b7dc204d704fe8f2f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419691"
---
# <span data-ttu-id="d0870-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="d0870-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="d0870-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0870-102">SYNOPSIS</span></span>
<span data-ttu-id="d0870-103">Lägger till ett jobb steg i ett jobb</span><span class="sxs-lookup"><span data-stu-id="d0870-103">Adds a job step to a job</span></span>

## <span data-ttu-id="d0870-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0870-104">SYNTAX</span></span>

### <span data-ttu-id="d0870-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d0870-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0870-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="d0870-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0870-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="d0870-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0870-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="d0870-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0870-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="d0870-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0870-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="d0870-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0870-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d0870-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0870-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d0870-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0870-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d0870-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0870-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0870-114">DESCRIPTION</span></span>
<span data-ttu-id="d0870-115">Add-AzSqlElasticJobStep cmdlet lägger till ett jobb steg i ett jobb</span><span class="sxs-lookup"><span data-stu-id="d0870-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="d0870-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0870-116">EXAMPLES</span></span>

### <span data-ttu-id="d0870-117">Exempel 1: lägger till ett steg i ett jobb</span><span class="sxs-lookup"><span data-stu-id="d0870-117">Example 1: Adds a step to a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="d0870-118">Lägger till ett jobb steg i ett jobb</span><span class="sxs-lookup"><span data-stu-id="d0870-118">Adds a job step to a job</span></span>

## <span data-ttu-id="d0870-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0870-119">PARAMETERS</span></span>

### <span data-ttu-id="d0870-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="d0870-120">-AgentName</span></span>
<span data-ttu-id="d0870-121">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="d0870-121">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0870-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="d0870-122">-CommandText</span></span>
<span data-ttu-id="d0870-123">Kommando texten</span><span class="sxs-lookup"><span data-stu-id="d0870-123">The command text</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0870-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="d0870-124">-CredentialName</span></span>
<span data-ttu-id="d0870-125">Namnet på autentiseringsuppgiften</span><span class="sxs-lookup"><span data-stu-id="d0870-125">The credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0870-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0870-126">-DefaultProfile</span></span>
<span data-ttu-id="d0870-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d0870-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0870-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="d0870-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="d0870-129">Det första återförsöksintervall för försök</span><span class="sxs-lookup"><span data-stu-id="d0870-129">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="d0870-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="d0870-130">-JobName</span></span>
<span data-ttu-id="d0870-131">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="d0870-131">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0870-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="d0870-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="d0870-133">Maximalt antal sekunder för försök</span><span class="sxs-lookup"><span data-stu-id="d0870-133">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="d0870-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="d0870-134">-Name</span></span>
<span data-ttu-id="d0870-135">Namn på projekt steget</span><span class="sxs-lookup"><span data-stu-id="d0870-135">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0870-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="d0870-136">-OutputCredentialName</span></span>
<span data-ttu-id="d0870-137">Namnet på Uppgiftsutdata</span><span class="sxs-lookup"><span data-stu-id="d0870-137">The output credential name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0870-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="d0870-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="d0870-139">Objektet utgående databas</span><span class="sxs-lookup"><span data-stu-id="d0870-139">The output database object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: WithOutputDb, WithOutputDbUsingParentObject, WithOutputDbUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0870-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="d0870-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="d0870-141">Resurs-ID för utdatafil</span><span class="sxs-lookup"><span data-stu-id="d0870-141">The output database resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDbId, WithOutputDbIdUsingParentObject, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0870-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="d0870-142">-OutputSchemaName</span></span>
<span data-ttu-id="d0870-143">Namn på utdatafil</span><span class="sxs-lookup"><span data-stu-id="d0870-143">The output schema name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0870-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="d0870-144">-OutputTableName</span></span>
<span data-ttu-id="d0870-145">Namn på resultat tabell</span><span class="sxs-lookup"><span data-stu-id="d0870-145">The output table name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0870-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d0870-146">-ParentObject</span></span>
<span data-ttu-id="d0870-147">Jobbobjektet</span><span class="sxs-lookup"><span data-stu-id="d0870-147">The job object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0870-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d0870-148">-ParentResourceId</span></span>
<span data-ttu-id="d0870-149">Jobb resurs-ID</span><span class="sxs-lookup"><span data-stu-id="d0870-149">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0870-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0870-150">-ResourceGroupName</span></span>
<span data-ttu-id="d0870-151">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="d0870-151">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0870-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="d0870-152">-RetryAttempts</span></span>
<span data-ttu-id="d0870-153">Försök igen</span><span class="sxs-lookup"><span data-stu-id="d0870-153">The retry attempts</span></span>

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

### <span data-ttu-id="d0870-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="d0870-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="d0870-155">Återförsöksintervall inaktive ras en multiplikator</span><span class="sxs-lookup"><span data-stu-id="d0870-155">The retry interval back off multiplier</span></span>

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

### <span data-ttu-id="d0870-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d0870-156">-ServerName</span></span>
<span data-ttu-id="d0870-157">Server namnet</span><span class="sxs-lookup"><span data-stu-id="d0870-157">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0870-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="d0870-158">-StepId</span></span>
<span data-ttu-id="d0870-159">Steg-ID</span><span class="sxs-lookup"><span data-stu-id="d0870-159">The step id</span></span>

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

### <span data-ttu-id="d0870-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="d0870-160">-TargetGroupName</span></span>
<span data-ttu-id="d0870-161">Namnet på mål gruppen</span><span class="sxs-lookup"><span data-stu-id="d0870-161">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId, ObjectSet, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, ResourceIdSet, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WithOutputDbUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0870-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="d0870-162">-TimeoutSeconds</span></span>
<span data-ttu-id="d0870-163">Tiden för timeout</span><span class="sxs-lookup"><span data-stu-id="d0870-163">The time out seconds</span></span>

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

### <span data-ttu-id="d0870-164">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d0870-164">-Confirm</span></span>
<span data-ttu-id="d0870-165">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d0870-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0870-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0870-166">-WhatIf</span></span>
<span data-ttu-id="d0870-167">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d0870-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0870-168">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d0870-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0870-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0870-169">CommonParameters</span></span>
<span data-ttu-id="d0870-170">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0870-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0870-171">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0870-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0870-172">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0870-172">INPUTS</span></span>

### <span data-ttu-id="d0870-173">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="d0870-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="d0870-174">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0870-174">OUTPUTS</span></span>

### <span data-ttu-id="d0870-175">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="d0870-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="d0870-176">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0870-176">NOTES</span></span>

## <span data-ttu-id="d0870-177">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0870-177">RELATED LINKS</span></span>
