---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
ms.openlocfilehash: f8a31171309a9c869d29078ff09ce8903288e8bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920249"
---
# <span data-ttu-id="7b5e7-101">Set-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="7b5e7-101">Set-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="7b5e7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7b5e7-102">SYNOPSIS</span></span>
<span data-ttu-id="7b5e7-103">**Viktigt: denna cmdlet är föråldrad, [set-AzSqlDatabaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseaudit) ersätter den.**</span><span class="sxs-lookup"><span data-stu-id="7b5e7-103">**Important: This cmdlet is deprecated, [Set-AzSqlDatabaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseaudit) is replacing it.**</span></span>

<span data-ttu-id="7b5e7-104">Ändrar gransknings inställningarna för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-104">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="7b5e7-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7b5e7-105">SYNTAX</span></span>

### <span data-ttu-id="7b5e7-106">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7b5e7-106">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] [-StorageAccountName <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b5e7-107">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="7b5e7-107">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] -StorageAccountName <String>
 -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b5e7-108">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="7b5e7-108">EventHubSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-EventHub] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b5e7-109">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="7b5e7-109">LogAnalyticsSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-WorkspaceResourceId <String>] [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b5e7-110">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="7b5e7-110">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b5e7-111">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="7b5e7-111">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b5e7-112">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="7b5e7-112">EventHubByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b5e7-113">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="7b5e7-113">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b5e7-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7b5e7-114">DESCRIPTION</span></span>
<span data-ttu-id="7b5e7-115">Cmdleten **set-AzSqlDatabaseAuditing** ändrar gransknings inställningarna för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-115">The **Set-AzSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="7b5e7-116">Använd cmdleten *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-116">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="7b5e7-117">Mål platsen för gransknings loggar bestäms genom att ange en av följande växel parametrar: BlobStorage, LogAnalytics eller EventHub (om ingen är angiven är standardvärdet BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="7b5e7-117">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="7b5e7-118">Använd parametern *State* för att aktivera/inaktivera principen.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-118">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="7b5e7-119">När mål för gransknings loggar är en blob-lagring anger du parametern *StorageAccountName* för att fastställa lagrings konto för gransknings loggar och parametern *StorageKeyType* för att definiera lagrings nycklarna.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-119">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="7b5e7-120">Du kan också definiera bevarande för gransknings loggar genom att ange värdet för *RetentionInDays* -parametern för att definiera perioden för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-120">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="7b5e7-121">Om cmdleten lyckas och du använder *Passthru* -parametern returneras ett objekt som beskriver de aktuella inställningarna för granskning, utöver databasens identifierare.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-121">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the database identifiers.</span></span>
<span data-ttu-id="7b5e7-122">Databas identifierare inkluderar, men är inte begränsade till, **ResourceGroupName** , **servername** och **databasename**.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-122">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="7b5e7-123">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7b5e7-123">EXAMPLES</span></span>

### <span data-ttu-id="7b5e7-124">Exempel 1: Aktivera gransknings princip för blob-lagring i en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="7b5e7-124">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="7b5e7-125">Exempel 2: inaktivera gransknings princip för blob-lagring för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="7b5e7-125">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="7b5e7-126">Exempel 3: Aktivera gransknings princip för blob-lagring för en Azure SQL-databas med ett lagrings konto från ett annat abonnemang</span><span class="sxs-lookup"><span data-stu-id="7b5e7-126">Example 3: Enable the blob storage auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="7b5e7-127">Exempel 4: Aktivera gransknings princip för blob-lagring för en Azure SQL-databas med avancerad filtrering med ett T-SQL-predikat</span><span class="sxs-lookup"><span data-stu-id="7b5e7-127">Example 4: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="7b5e7-128">Exempel 5: ta bort inställningen Advanced filter from gransknings princip för blob-lagring i en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="7b5e7-128">Example 5: Remove the advanced filtering setting from the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="7b5e7-129">Exempel 6: Aktivera gransknings principen för händelsehubben för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="7b5e7-129">Example 6: Enable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="7b5e7-130">Exempel 7: inaktivera gransknings princip för händelsehubben för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="7b5e7-130">Example 7: Disable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub
```

### <span data-ttu-id="7b5e7-131">Exempel 8: Aktivera gransknings princip för logganalys för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="7b5e7-131">Example 8: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="7b5e7-132">Exempel 9: inaktivera gransknings principen för logganalys för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="7b5e7-132">Example 9: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
```

### <span data-ttu-id="7b5e7-133">Exempel 10: inaktivera, genom pipeline, gransknings princip för logganalys för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="7b5e7-133">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="7b5e7-134">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7b5e7-134">PARAMETERS</span></span>

### <span data-ttu-id="7b5e7-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b5e7-135">-AsJob</span></span>
<span data-ttu-id="7b5e7-136">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7b5e7-136">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e7-137">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="7b5e7-137">-AuditAction</span></span>
<span data-ttu-id="7b5e7-138">Uppsättningen gransknings åtgärder.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-138">The set of audit actions.</span></span>  
<span data-ttu-id="7b5e7-139">De åtgärder som stöds för granskning är:</span><span class="sxs-lookup"><span data-stu-id="7b5e7-139">The supported actions to audit are:</span></span>  
<span data-ttu-id="7b5e7-140">ANVÄNDA</span><span class="sxs-lookup"><span data-stu-id="7b5e7-140">SELECT</span></span>  
<span data-ttu-id="7b5e7-141">UPPDATERA</span><span class="sxs-lookup"><span data-stu-id="7b5e7-141">UPDATE</span></span>  
<span data-ttu-id="7b5e7-142">Placera</span><span class="sxs-lookup"><span data-stu-id="7b5e7-142">INSERT</span></span>  
<span data-ttu-id="7b5e7-143">TA bort</span><span class="sxs-lookup"><span data-stu-id="7b5e7-143">DELETE</span></span>  
<span data-ttu-id="7b5e7-144">GENOMFÖR</span><span class="sxs-lookup"><span data-stu-id="7b5e7-144">EXECUTE</span></span>  
<span data-ttu-id="7b5e7-145">MOTTAR</span><span class="sxs-lookup"><span data-stu-id="7b5e7-145">RECEIVE</span></span>  
<span data-ttu-id="7b5e7-146">Anger att det allmänna formuläret för att definiera en åtgärd ska granskas: [åtgärd] [Object] av [huvudsaklig] Observera att [objekt] i ovanstående format kan referera till ett objekt som en tabell, en vy eller en lagrad procedur eller en hel databas eller ett schema.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-146">REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="7b5e7-147">För de sistnämnda fallen används formulär databasen:: [dbname] och SCHEMA:: [SchemaName].</span><span class="sxs-lookup"><span data-stu-id="7b5e7-147">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="7b5e7-148">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="7b5e7-148">For example:</span></span>  
<span data-ttu-id="7b5e7-149">Välj i dbo. nontable av offentlig</span><span class="sxs-lookup"><span data-stu-id="7b5e7-149">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="7b5e7-150">Välj på databas:: min databas av offentlig</span><span class="sxs-lookup"><span data-stu-id="7b5e7-150">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="7b5e7-151">Välj på SCHEMA:: mina schema av offentlig</span><span class="sxs-lookup"><span data-stu-id="7b5e7-151">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="7b5e7-152">Mer information finns i https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="7b5e7-152">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e7-153">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="7b5e7-153">-AuditActionGroup</span></span>
<span data-ttu-id="7b5e7-154">Den rekommenderade uppsättningen åtgärds grupper som ska användas är följande kombination – detta granskar alla frågor och lagrade procedurer som körs mot databasen samt lyckade och misslyckade inloggningar:</span><span class="sxs-lookup"><span data-stu-id="7b5e7-154">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="7b5e7-155">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="7b5e7-155">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="7b5e7-156">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="7b5e7-156">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="7b5e7-157">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="7b5e7-157">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="7b5e7-158">Ovanstående kombination är även den uppsättning som är konfigurerad som standard.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-158">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="7b5e7-159">Dessa grupper täcker alla SQL-uttryck och lagrade procedurer som körs mot databasen och ska inte användas i kombination med andra grupper eftersom detta kommer att leda till dubbletter av gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-159">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="7b5e7-160">Mer information finns i https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="7b5e7-160">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e7-161">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="7b5e7-161">-BlobStorage</span></span>
<span data-ttu-id="7b5e7-162">Anger att gransknings loggar destinationen är Blob Storage</span><span class="sxs-lookup"><span data-stu-id="7b5e7-162">Specifies that audit logs destination is blob storage</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e7-163">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7b5e7-163">-DatabaseName</span></span>
<span data-ttu-id="7b5e7-164">Namn på SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-164">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e7-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b5e7-165">-DefaultProfile</span></span>
<span data-ttu-id="7b5e7-166">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-166">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b5e7-167">-EventHub</span><span class="sxs-lookup"><span data-stu-id="7b5e7-167">-EventHub</span></span>
<span data-ttu-id="7b5e7-168">Anger att gransknings loggar destinationen är händelsehubben</span><span class="sxs-lookup"><span data-stu-id="7b5e7-168">Specifies that audit logs destination is event hub</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e7-169">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="7b5e7-169">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="7b5e7-170">Resurs-ID för regel för händelsehubben</span><span class="sxs-lookup"><span data-stu-id="7b5e7-170">The resource Id for the event hub authorization rule</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e7-171">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="7b5e7-171">-EventHubName</span></span>
<span data-ttu-id="7b5e7-172">Namnet på händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-172">The name of the event hub.</span></span> <span data-ttu-id="7b5e7-173">Om ingen anges när du tillhandahåller EventHubAuthorizationRuleResourceId väljs standard händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-173">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e7-174">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b5e7-174">-InputObject</span></span>
<span data-ttu-id="7b5e7-175">Databasobjektet för att hantera dess gransknings princip.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-175">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e7-176">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="7b5e7-176">-LogAnalytics</span></span>
<span data-ttu-id="7b5e7-177">Anger att gransknings loggar destinationen är logg analys</span><span class="sxs-lookup"><span data-stu-id="7b5e7-177">Specifies that audit logs destination is log analytics</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e7-178">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b5e7-178">-PassThru</span></span>
<span data-ttu-id="7b5e7-179">Anger om gransknings principen ska sparas när cmdlet körs</span><span class="sxs-lookup"><span data-stu-id="7b5e7-179">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e7-180">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="7b5e7-180">-PredicateExpression</span></span>
<span data-ttu-id="7b5e7-181">Uttrycket T-SQL predikat (WHERE-satsen) som används för att filtrera gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-181">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e7-182">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b5e7-182">-ResourceGroupName</span></span>
<span data-ttu-id="7b5e7-183">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-183">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e7-184">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7b5e7-184">-RetentionInDays</span></span>
<span data-ttu-id="7b5e7-185">Antalet bevarande dagar för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-185">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e7-186">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7b5e7-186">-ServerName</span></span>
<span data-ttu-id="7b5e7-187">SQL Server-namn.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-187">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e7-188">-State</span><span class="sxs-lookup"><span data-stu-id="7b5e7-188">-State</span></span>
<span data-ttu-id="7b5e7-189">Tillståndet för policyn.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-189">The state of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e7-190">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7b5e7-190">-StorageAccountName</span></span>
<span data-ttu-id="7b5e7-191">Namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-191">The name of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageAccountSubscriptionIdSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e7-192">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7b5e7-192">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="7b5e7-193">ID för abonnemang för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="7b5e7-193">The storage account subscription id</span></span>

```yaml
Type: System.Guid
Parameter Sets: StorageAccountSubscriptionIdSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e7-194">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="7b5e7-194">-StorageKeyType</span></span>
<span data-ttu-id="7b5e7-195">Anger vilken av lagrings åtkomst nycklar som ska användas.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-195">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e7-196">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="7b5e7-196">-WorkspaceResourceId</span></span>
<span data-ttu-id="7b5e7-197">Arbetsyte-ID (resurs-ID för en logganalys-arbetsyta) för en logganalys-arbetsyta som du vill skicka gransknings loggar till.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-197">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="7b5e7-198">Exempel:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="7b5e7-198">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

```yaml
Type: System.String
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e7-199">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7b5e7-199">-Confirm</span></span>
<span data-ttu-id="7b5e7-200">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-200">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e7-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b5e7-201">-WhatIf</span></span>
<span data-ttu-id="7b5e7-202">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b5e7-203">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-203">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e7-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b5e7-204">CommonParameters</span></span>
<span data-ttu-id="7b5e7-205">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b5e7-206">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b5e7-206">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b5e7-207">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7b5e7-207">INPUTS</span></span>

### <span data-ttu-id="7b5e7-208">System. String</span><span class="sxs-lookup"><span data-stu-id="7b5e7-208">System.String</span></span>

### <span data-ttu-id="7b5e7-209">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="7b5e7-209">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="7b5e7-210">Microsoft. Azure. commands. SQL. granskning. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="7b5e7-210">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="7b5e7-211">System. string []</span><span class="sxs-lookup"><span data-stu-id="7b5e7-211">System.String[]</span></span>

### <span data-ttu-id="7b5e7-212">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7b5e7-212">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="7b5e7-213">System. GUID</span><span class="sxs-lookup"><span data-stu-id="7b5e7-213">System.Guid</span></span>

### <span data-ttu-id="7b5e7-214">System. Nullable ' 1 [[system. UInt32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7b5e7-214">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7b5e7-215">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7b5e7-215">OUTPUTS</span></span>

### <span data-ttu-id="7b5e7-216">Microsoft. Azure. commands. SQL. granskning. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="7b5e7-216">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="7b5e7-217">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7b5e7-217">NOTES</span></span>

## <span data-ttu-id="7b5e7-218">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7b5e7-218">RELATED LINKS</span></span>
