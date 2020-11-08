---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
ms.openlocfilehash: 6ade592fde11c3bd614f602070fba87b60cdcda3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088997"
---
# <span data-ttu-id="dad17-101">Add-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="dad17-101">Add-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="dad17-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dad17-102">SYNOPSIS</span></span>
<span data-ttu-id="dad17-103">Lägger till ett mål i en mål grupp</span><span class="sxs-lookup"><span data-stu-id="dad17-103">Adds a target to a target group</span></span>

## <span data-ttu-id="dad17-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dad17-104">SYNTAX</span></span>

### <span data-ttu-id="dad17-105">SqlDatabase (standard)</span><span class="sxs-lookup"><span data-stu-id="dad17-105">SqlDatabase (Default)</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dad17-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="dad17-106">SqlServerOrElasticPool</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dad17-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="dad17-107">SqlShardMap</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dad17-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="dad17-108">SqlDatabaseUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dad17-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="dad17-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dad17-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="dad17-110">SqlShardMapUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dad17-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="dad17-111">SqlDatabaseUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dad17-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="dad17-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dad17-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="dad17-113">SqlShardMapUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dad17-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dad17-114">DESCRIPTION</span></span>
<span data-ttu-id="dad17-115">Add-AzSqlElasticJobTarget cmdlet lägger till en mål resurs i en mål grupp</span><span class="sxs-lookup"><span data-stu-id="dad17-115">The Add-AzSqlElasticJobTarget cmdlet adds a target resource to a target group</span></span>

## <span data-ttu-id="dad17-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dad17-116">EXAMPLES</span></span>

### <span data-ttu-id="dad17-117">Exempel 1 – Lägg till ett Server mål</span><span class="sxs-lookup"><span data-stu-id="dad17-117">Example 1 - Add a server target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="dad17-118">Exempel 2 – Lägg till ett databas mål</span><span class="sxs-lookup"><span data-stu-id="dad17-118">Example 2 - Add a database target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="dad17-119">Exempel 3 – Lägg till ett elastiskt pool-mål</span><span class="sxs-lookup"><span data-stu-id="dad17-119">Example 3 - Add an elastic pool target</span></span>
```
PS C:\> $tg | Add-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="dad17-120">Exempel 4 – Lägg till ett Shard</span><span class="sxs-lookup"><span data-stu-id="dad17-120">Example 4 - Add a shard map target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="dad17-121">Lägger till ett mål (Server, elastisk pool, databas och Shard karta) till en mål grupp</span><span class="sxs-lookup"><span data-stu-id="dad17-121">Adds a target (server, elastic pool, database, and shard map) to a target group</span></span>

## <span data-ttu-id="dad17-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dad17-122">PARAMETERS</span></span>

### <span data-ttu-id="dad17-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="dad17-123">-AgentName</span></span>
<span data-ttu-id="dad17-124">Namnet på agenten.</span><span class="sxs-lookup"><span data-stu-id="dad17-124">The agent name.</span></span>

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

### <span data-ttu-id="dad17-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="dad17-125">-AgentServerName</span></span>
<span data-ttu-id="dad17-126">Server namnet.</span><span class="sxs-lookup"><span data-stu-id="dad17-126">The server name.</span></span>

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

### <span data-ttu-id="dad17-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dad17-127">-DatabaseName</span></span>
<span data-ttu-id="dad17-128">Namn på databas mål</span><span class="sxs-lookup"><span data-stu-id="dad17-128">Database Target Name</span></span>

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

### <span data-ttu-id="dad17-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dad17-129">-DefaultProfile</span></span>
<span data-ttu-id="dad17-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dad17-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dad17-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="dad17-131">-ElasticPoolName</span></span>
<span data-ttu-id="dad17-132">Mål namn för elastisk pool</span><span class="sxs-lookup"><span data-stu-id="dad17-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="dad17-133">-Exkludera</span><span class="sxs-lookup"><span data-stu-id="dad17-133">-Exclude</span></span>
<span data-ttu-id="dad17-134">Utesluter ett mål.</span><span class="sxs-lookup"><span data-stu-id="dad17-134">Excludes a target.</span></span>

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

### <span data-ttu-id="dad17-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dad17-135">-ParentObject</span></span>
<span data-ttu-id="dad17-136">Mål grupps objekt.</span><span class="sxs-lookup"><span data-stu-id="dad17-136">The target group object.</span></span>

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

### <span data-ttu-id="dad17-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="dad17-137">-ParentResourceId</span></span>
<span data-ttu-id="dad17-138">Resurs-ID för mål grupp.</span><span class="sxs-lookup"><span data-stu-id="dad17-138">The target group resource id.</span></span>

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

### <span data-ttu-id="dad17-139">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="dad17-139">-RefreshCredentialName</span></span>
<span data-ttu-id="dad17-140">Uppdatera namn på autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="dad17-140">Refresh Credential Name</span></span>

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

### <span data-ttu-id="dad17-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dad17-141">-ResourceGroupName</span></span>
<span data-ttu-id="dad17-142">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="dad17-142">Resource Group Name</span></span>

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

### <span data-ttu-id="dad17-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dad17-143">-ServerName</span></span>
<span data-ttu-id="dad17-144">Server måls namn</span><span class="sxs-lookup"><span data-stu-id="dad17-144">Server Target Name</span></span>

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

### <span data-ttu-id="dad17-145">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="dad17-145">-ShardMapName</span></span>
<span data-ttu-id="dad17-146">Shard kartans målnamn</span><span class="sxs-lookup"><span data-stu-id="dad17-146">Shard Map Target Name</span></span>

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

### <span data-ttu-id="dad17-147">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="dad17-147">-TargetGroupName</span></span>
<span data-ttu-id="dad17-148">Namnet på mål gruppen.</span><span class="sxs-lookup"><span data-stu-id="dad17-148">The target group name.</span></span>

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

### <span data-ttu-id="dad17-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dad17-149">-Confirm</span></span>
<span data-ttu-id="dad17-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dad17-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dad17-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dad17-151">-WhatIf</span></span>
<span data-ttu-id="dad17-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dad17-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dad17-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dad17-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dad17-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad17-154">CommonParameters</span></span>
<span data-ttu-id="dad17-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dad17-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad17-156">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dad17-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad17-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dad17-157">INPUTS</span></span>

### <span data-ttu-id="dad17-158">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="dad17-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="dad17-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dad17-159">OUTPUTS</span></span>

### <span data-ttu-id="dad17-160">Microsoft. Azure. Management. SQL. Models. JobTarget</span><span class="sxs-lookup"><span data-stu-id="dad17-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="dad17-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dad17-161">NOTES</span></span>

## <span data-ttu-id="dad17-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dad17-162">RELATED LINKS</span></span>
