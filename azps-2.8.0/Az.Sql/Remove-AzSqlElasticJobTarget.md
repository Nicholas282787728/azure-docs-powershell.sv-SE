---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
ms.openlocfilehash: 5b52a3b7601e98c8ae74866e88c996ab599added
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920548"
---
# <span data-ttu-id="01c88-101">Remove-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="01c88-101">Remove-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="01c88-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="01c88-102">SYNOPSIS</span></span>
<span data-ttu-id="01c88-103">Tar bort målet från mål gruppen</span><span class="sxs-lookup"><span data-stu-id="01c88-103">Removes the target from the target group</span></span>

## <span data-ttu-id="01c88-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="01c88-104">SYNTAX</span></span>

### <span data-ttu-id="01c88-105">SqlDatabase (standard)</span><span class="sxs-lookup"><span data-stu-id="01c88-105">SqlDatabase (Default)</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01c88-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="01c88-106">SqlServerOrElasticPool</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>] -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01c88-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="01c88-107">SqlShardMap</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String> -DatabaseName <String>
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01c88-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="01c88-108">SqlDatabaseUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01c88-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="01c88-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01c88-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="01c88-110">SqlShardMapUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01c88-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="01c88-111">SqlDatabaseUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01c88-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="01c88-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01c88-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="01c88-113">SqlShardMapUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01c88-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="01c88-114">DESCRIPTION</span></span>
<span data-ttu-id="01c88-115">Remove-AzSqlElasticJobTarget cmdlet tar bort en mål resurs till en mål grupp</span><span class="sxs-lookup"><span data-stu-id="01c88-115">The Remove-AzSqlElasticJobTarget cmdlet removes a target resource to a target group</span></span>

## <span data-ttu-id="01c88-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="01c88-116">EXAMPLES</span></span>

### <span data-ttu-id="01c88-117">Exempel 1 – ta bort ett Server mål</span><span class="sxs-lookup"><span data-stu-id="01c88-117">Example 1 - Remove a server target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="01c88-118">Exempel 2 – ta bort ett databas mål</span><span class="sxs-lookup"><span data-stu-id="01c88-118">Example 2 - Remove a database target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="01c88-119">Exempel 3 – ta bort ett elastiskt pool-mål</span><span class="sxs-lookup"><span data-stu-id="01c88-119">Example 3 - Remove an elastic pool target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="01c88-120">Exempel 4 – ta bort ett Shard kart mål</span><span class="sxs-lookup"><span data-stu-id="01c88-120">Example 4 - Remove a shard map target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="01c88-121">Tar bort ett mål (Server, elastisk pool, databas och Shard karta) från en mål grupp</span><span class="sxs-lookup"><span data-stu-id="01c88-121">Removes a target (server, elastic pool, database, and shard map) from a target group</span></span>

## <span data-ttu-id="01c88-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="01c88-122">PARAMETERS</span></span>

### <span data-ttu-id="01c88-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="01c88-123">-AgentName</span></span>
<span data-ttu-id="01c88-124">Namn på SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="01c88-124">SQL Database Agent Name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c88-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="01c88-125">-AgentServerName</span></span>
<span data-ttu-id="01c88-126">Namn på Server för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="01c88-126">SQL Database Agent Server Name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c88-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="01c88-127">-DatabaseName</span></span>
<span data-ttu-id="01c88-128">Namn på databas mål</span><span class="sxs-lookup"><span data-stu-id="01c88-128">Database Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlShardMap, SqlDatabaseUsingParentObject, SqlShardMapUsingParentObject, SqlDatabaseUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01c88-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01c88-129">-DefaultProfile</span></span>
<span data-ttu-id="01c88-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="01c88-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01c88-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="01c88-131">-ElasticPoolName</span></span>
<span data-ttu-id="01c88-132">Mål namn för elastisk pool</span><span class="sxs-lookup"><span data-stu-id="01c88-132">Elastic Pool Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool, SqlServerOrElasticPoolUsingParentObject, SqlServerOrElasticPoolUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01c88-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="01c88-133">-ParentObject</span></span>
<span data-ttu-id="01c88-134">Mål grupps objekt.</span><span class="sxs-lookup"><span data-stu-id="01c88-134">The target group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel
Parameter Sets: SqlDatabaseUsingParentObject, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01c88-135">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="01c88-135">-ParentResourceId</span></span>
<span data-ttu-id="01c88-136">Resurs-ID för mål grupp.</span><span class="sxs-lookup"><span data-stu-id="01c88-136">The target group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabaseUsingParentResourceId, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01c88-137">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="01c88-137">-RefreshCredentialName</span></span>
<span data-ttu-id="01c88-138">Uppdatera namn på autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="01c88-138">Refresh Credential Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool, SqlShardMap, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c88-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01c88-139">-ResourceGroupName</span></span>
<span data-ttu-id="01c88-140">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="01c88-140">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c88-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="01c88-141">-ServerName</span></span>
<span data-ttu-id="01c88-142">Server måls namn</span><span class="sxs-lookup"><span data-stu-id="01c88-142">Server Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlShardMap, SqlDatabaseUsingParentObject, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject, SqlDatabaseUsingParentResourceId, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01c88-143">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="01c88-143">-ShardMapName</span></span>
<span data-ttu-id="01c88-144">Shard kartans målnamn</span><span class="sxs-lookup"><span data-stu-id="01c88-144">Shard Map Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlShardMap, SqlShardMapUsingParentObject, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01c88-145">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="01c88-145">-TargetGroupName</span></span>
<span data-ttu-id="01c88-146">Namn på SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="01c88-146">SQL Database Agent Name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c88-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="01c88-147">-Confirm</span></span>
<span data-ttu-id="01c88-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="01c88-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01c88-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01c88-149">-WhatIf</span></span>
<span data-ttu-id="01c88-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="01c88-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01c88-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="01c88-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01c88-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01c88-152">CommonParameters</span></span>
<span data-ttu-id="01c88-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01c88-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01c88-154">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01c88-154">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01c88-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="01c88-155">INPUTS</span></span>

### <span data-ttu-id="01c88-156">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="01c88-156">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="01c88-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="01c88-157">OUTPUTS</span></span>

### <span data-ttu-id="01c88-158">Microsoft. Azure. Management. SQL. Models. JobTarget</span><span class="sxs-lookup"><span data-stu-id="01c88-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="01c88-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="01c88-159">NOTES</span></span>

## <span data-ttu-id="01c88-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="01c88-160">RELATED LINKS</span></span>
