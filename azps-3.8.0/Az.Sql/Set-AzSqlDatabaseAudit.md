---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
ms.openlocfilehash: f84e291c7b69ed8a61288a660b14db9ddf24d95a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088589"
---
# <span data-ttu-id="3383f-101">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="3383f-101">Set-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="3383f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3383f-102">SYNOPSIS</span></span>
<span data-ttu-id="3383f-103">Ändrar gransknings inställningarna för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="3383f-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="3383f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3383f-104">SYNTAX</span></span>

### <span data-ttu-id="3383f-105">DatabaseParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3383f-105">DatabaseParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3383f-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3383f-106">DatabaseObjectParameterSet</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -DatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3383f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3383f-107">DESCRIPTION</span></span>
<span data-ttu-id="3383f-108">Cmdleten **set-AzSqlDatabaseAudit** ändrar gransknings inställningarna för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="3383f-108">The **Set-AzSqlDatabaseAudit** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="3383f-109">Använd cmdleten *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="3383f-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="3383f-110">När Blob Storage är ett mål för gransknings loggar anger du parametern *StorageAccountResourceId* för att bestämma lagrings konto för gransknings loggar och parametern *StorageKeyType* för att definiera lagrings nycklarna.</span><span class="sxs-lookup"><span data-stu-id="3383f-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="3383f-111">Du kan också definiera bevarande för gransknings loggar genom att ange värdet för *RetentionInDays* -parametern för att definiera perioden för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="3383f-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="3383f-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3383f-112">EXAMPLES</span></span>

### <span data-ttu-id="3383f-113">Exempel 1: Aktivera gransknings princip för blob-lagring i en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="3383f-113">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled  -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="3383f-114">Exempel 2: inaktivera gransknings princip för blob-lagring för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="3383f-114">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="3383f-115">Exempel 3,1: Aktivera gransknings princip för blob-lagring för en Azure SQL-databas med avancerad filtrering med ett T-SQL-predikat</span><span class="sxs-lookup"><span data-stu-id="3383f-115">Example 3.1: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="3383f-116">Exempel 3,2: ta bort inställningen Advanced filter from gransknings principen för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="3383f-116">Example 3.2: Remove the advanced filtering setting from the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="3383f-117">Exempel 4: Aktivera gransknings principen för händelsehubben för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="3383f-117">Example 4: Enable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="3383f-118">Exempel 5: inaktivera gransknings princip för händelsehubben för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="3383f-118">Example 5: Disable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Disabled
```

### <span data-ttu-id="3383f-119">Exempel 6: Aktivera gransknings princip för logganalys för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="3383f-119">Example 6: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="3383f-120">Exempel 7: inaktivera gransknings principen för logganalys för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="3383f-120">Example 7: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="3383f-121">Exempel 8: inaktivera, genom pipeline, gransknings princip för logganalys för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="3383f-121">Example 8: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="3383f-122">Exempel 9: inaktivera skicka gransknings poster för en Azure SQL-databas till Blob Storage och aktivera dem för att logga analyser.</span><span class="sxs-lookup"><span data-stu-id="3383f-122">Example 9: Disable sending audit records of an Azure SQL database to blob storage, and enable sending them to log analytics.</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="3383f-123">Exempel 10: Aktivera att skicka gransknings poster för en Azure SQL-databas till Blob Storage, händelsehubben och logganalys.</span><span class="sxs-lookup"><span data-stu-id="3383f-123">Example 10: Enable sending audit records of an Azure SQL database to blob storage, event hub and log analytics.</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="3383f-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3383f-124">PARAMETERS</span></span>

### <span data-ttu-id="3383f-125">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="3383f-125">-AuditAction</span></span>
<span data-ttu-id="3383f-126">Uppsättningen gransknings åtgärder.</span><span class="sxs-lookup"><span data-stu-id="3383f-126">The set of audit actions.</span></span>  
<span data-ttu-id="3383f-127">De åtgärder som stöds för granskning är:</span><span class="sxs-lookup"><span data-stu-id="3383f-127">The supported actions to audit are:</span></span>  
<span data-ttu-id="3383f-128">ANVÄNDA</span><span class="sxs-lookup"><span data-stu-id="3383f-128">SELECT</span></span>  
<span data-ttu-id="3383f-129">UPPDATERA</span><span class="sxs-lookup"><span data-stu-id="3383f-129">UPDATE</span></span>  
<span data-ttu-id="3383f-130">Placera</span><span class="sxs-lookup"><span data-stu-id="3383f-130">INSERT</span></span>  
<span data-ttu-id="3383f-131">TA bort</span><span class="sxs-lookup"><span data-stu-id="3383f-131">DELETE</span></span>  
<span data-ttu-id="3383f-132">GENOMFÖR</span><span class="sxs-lookup"><span data-stu-id="3383f-132">EXECUTE</span></span>  
<span data-ttu-id="3383f-133">MOTTAR</span><span class="sxs-lookup"><span data-stu-id="3383f-133">RECEIVE</span></span>  
<span data-ttu-id="3383f-134">INNEHÅLLER</span><span class="sxs-lookup"><span data-stu-id="3383f-134">REFERENCES</span></span>  
<span data-ttu-id="3383f-135">Det allmänna formuläret för att definiera en åtgärd som ska granskas är: [åtgärd] [Object] av [kapital] OBS! [Object] i ovanstående format kan referera till ett objekt som en tabell, en vy eller en lagrad procedur eller en hel databas eller ett schema.</span><span class="sxs-lookup"><span data-stu-id="3383f-135">The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="3383f-136">För de sistnämnda fallen används formulär databasen:: [dbname] och SCHEMA:: [SchemaName].</span><span class="sxs-lookup"><span data-stu-id="3383f-136">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="3383f-137">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="3383f-137">For example:</span></span>  
<span data-ttu-id="3383f-138">Välj i dbo. nontable av offentlig</span><span class="sxs-lookup"><span data-stu-id="3383f-138">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="3383f-139">Välj på databas:: min databas av offentlig</span><span class="sxs-lookup"><span data-stu-id="3383f-139">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="3383f-140">Välj på SCHEMA:: mina schema av offentlig</span><span class="sxs-lookup"><span data-stu-id="3383f-140">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="3383f-141">Mer information finns i https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="3383f-141">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3383f-142">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="3383f-142">-AuditActionGroup</span></span>
<span data-ttu-id="3383f-143">Den rekommenderade uppsättningen åtgärds grupper som ska användas är följande kombination – detta granskar alla frågor och lagrade procedurer som körs mot databasen samt lyckade och misslyckade inloggningar:</span><span class="sxs-lookup"><span data-stu-id="3383f-143">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="3383f-144">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="3383f-144">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="3383f-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="3383f-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="3383f-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="3383f-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="3383f-147">Ovanstående kombination är även den uppsättning som är konfigurerad som standard.</span><span class="sxs-lookup"><span data-stu-id="3383f-147">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="3383f-148">Dessa grupper täcker alla SQL-uttryck och lagrade procedurer som körs mot databasen och ska inte användas i kombination med andra grupper eftersom detta kommer att leda till dubbletter av gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="3383f-148">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="3383f-149">Mer information finns i https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="3383f-149">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3383f-150">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="3383f-150">-BlobStorageTargetState</span></span>
<span data-ttu-id="3383f-151">Anger om Blob Storage är en destination för gransknings poster.</span><span class="sxs-lookup"><span data-stu-id="3383f-151">Indicates whether blob storage is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3383f-152">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3383f-152">-DatabaseName</span></span>
<span data-ttu-id="3383f-153">Namn på SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="3383f-153">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3383f-154">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="3383f-154">-DatabaseObject</span></span>
<span data-ttu-id="3383f-155">Databasobjektet för att hantera dess gransknings princip.</span><span class="sxs-lookup"><span data-stu-id="3383f-155">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3383f-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3383f-156">-DefaultProfile</span></span>
<span data-ttu-id="3383f-157">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3383f-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3383f-158">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="3383f-158">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="3383f-159">Resurs-ID för regel för händelsehubben</span><span class="sxs-lookup"><span data-stu-id="3383f-159">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="3383f-160">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="3383f-160">-EventHubName</span></span>
<span data-ttu-id="3383f-161">Namnet på händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="3383f-161">The name of the event hub.</span></span> <span data-ttu-id="3383f-162">Om ingen anges när du tillhandahåller EventHubAuthorizationRuleResourceId väljs standard händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="3383f-162">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="3383f-163">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="3383f-163">-EventHubTargetState</span></span>
<span data-ttu-id="3383f-164">Anger om händelsehubben är en mål för gransknings poster.</span><span class="sxs-lookup"><span data-stu-id="3383f-164">Indicates whether event hub is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3383f-165">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="3383f-165">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="3383f-166">Anger om logg analys är en destination för gransknings poster.</span><span class="sxs-lookup"><span data-stu-id="3383f-166">Indicates whether log analytics is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3383f-167">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3383f-167">-PassThru</span></span>
<span data-ttu-id="3383f-168">Anger om gransknings principen ska sparas när cmdlet körs</span><span class="sxs-lookup"><span data-stu-id="3383f-168">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="3383f-169">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="3383f-169">-PredicateExpression</span></span>
<span data-ttu-id="3383f-170">Uttrycket T-SQL predikat (WHERE-satsen) som används för att filtrera gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="3383f-170">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="3383f-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3383f-171">-ResourceGroupName</span></span>
<span data-ttu-id="3383f-172">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3383f-172">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3383f-173">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="3383f-173">-RetentionInDays</span></span>
<span data-ttu-id="3383f-174">Antalet bevarande dagar för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="3383f-174">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3383f-175">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3383f-175">-ServerName</span></span>
<span data-ttu-id="3383f-176">SQL Server-namn.</span><span class="sxs-lookup"><span data-stu-id="3383f-176">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3383f-177">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="3383f-177">-StorageAccountResourceId</span></span>
<span data-ttu-id="3383f-178">Resurs-ID för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="3383f-178">The storage account resource id</span></span>

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

### <span data-ttu-id="3383f-179">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="3383f-179">-StorageKeyType</span></span>
<span data-ttu-id="3383f-180">Anger vilken av lagrings åtkomst nycklar som ska användas.</span><span class="sxs-lookup"><span data-stu-id="3383f-180">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3383f-181">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="3383f-181">-WorkspaceResourceId</span></span>
<span data-ttu-id="3383f-182">Arbetsyte-ID (resurs-ID för en logganalys-arbetsyta) för en logganalys-arbetsyta som du vill skicka gransknings loggar till.</span><span class="sxs-lookup"><span data-stu-id="3383f-182">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="3383f-183">Exempel:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="3383f-183">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="3383f-184">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3383f-184">-Confirm</span></span>
<span data-ttu-id="3383f-185">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3383f-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3383f-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3383f-186">-WhatIf</span></span>
<span data-ttu-id="3383f-187">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3383f-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3383f-188">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3383f-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3383f-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3383f-189">CommonParameters</span></span>
<span data-ttu-id="3383f-190">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3383f-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3383f-191">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3383f-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3383f-192">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3383f-192">INPUTS</span></span>

### <span data-ttu-id="3383f-193">System. String</span><span class="sxs-lookup"><span data-stu-id="3383f-193">System.String</span></span>

### <span data-ttu-id="3383f-194">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="3383f-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="3383f-195">Microsoft. Azure. commands. SQL. granskning. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="3383f-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="3383f-196">System. string []</span><span class="sxs-lookup"><span data-stu-id="3383f-196">System.String[]</span></span>

### <span data-ttu-id="3383f-197">System. GUID</span><span class="sxs-lookup"><span data-stu-id="3383f-197">System.Guid</span></span>

### <span data-ttu-id="3383f-198">System. Nullable ' 1 [[system. UInt32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3383f-198">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3383f-199">Microsoft. Azure. commands. SQL. granskning. Model. DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="3383f-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="3383f-200">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3383f-200">OUTPUTS</span></span>

### <span data-ttu-id="3383f-201">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3383f-201">System.Boolean</span></span>

## <span data-ttu-id="3383f-202">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3383f-202">NOTES</span></span>

## <span data-ttu-id="3383f-203">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3383f-203">RELATED LINKS</span></span>
