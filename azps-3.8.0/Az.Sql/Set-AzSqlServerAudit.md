---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
ms.openlocfilehash: 5ba80e2b8c2ca315f9b51b9873688f0b80f1e85f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927137"
---
# <span data-ttu-id="6d53d-101">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6d53d-101">Set-AzSqlServerAudit</span></span>

## <span data-ttu-id="6d53d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d53d-102">SYNOPSIS</span></span>
<span data-ttu-id="6d53d-103">Ändrar gransknings inställningarna för en Azure SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="6d53d-103">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="6d53d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d53d-104">SYNTAX</span></span>

### <span data-ttu-id="6d53d-105">ServerParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6d53d-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d53d-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d53d-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d53d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d53d-107">DESCRIPTION</span></span>
<span data-ttu-id="6d53d-108">Cmdleten **set-AzSqlServerAudit** ändrar gransknings inställningarna för en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6d53d-108">The **Set-AzSqlServerAudit** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="6d53d-109">Använd cmdleten *ResourceGroupName* och *servername* för att identifiera servern.</span><span class="sxs-lookup"><span data-stu-id="6d53d-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="6d53d-110">När Blob Storage är ett mål för gransknings loggar anger du parametern *StorageAccountResourceId* för att bestämma lagrings konto för gransknings loggar och parametern *StorageKeyType* för att definiera lagrings nycklarna.</span><span class="sxs-lookup"><span data-stu-id="6d53d-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="6d53d-111">Du kan också definiera bevarande för gransknings loggar genom att ange värdet för *RetentionInDays* -parametern för att definiera perioden för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="6d53d-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="6d53d-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d53d-112">EXAMPLES</span></span>

### <span data-ttu-id="6d53d-113">Exempel 1: Aktivera gransknings princip för blob-lagring för en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="6d53d-113">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="6d53d-114">Exempel 2: inaktivera gransknings princip för blob-lagring för en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="6d53d-114">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="6d53d-115">Exempel 3,1: Aktivera gransknings princip för blob-lagring för en Azure SQL Server med avancerad filtrering med ett T-SQL-predikat</span><span class="sxs-lookup"><span data-stu-id="6d53d-115">Example 3.1: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="6d53d-116">Exempel 3,2: ta bort inställningen Advanced filter from gransknings principen för en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="6d53d-116">Example 3.2: Remove the advanced filtering setting from the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -PredicateExpression ""
```

### <span data-ttu-id="6d53d-117">Exempel 4: Aktivera gransknings principen för händelsehubben för en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="6d53d-117">Example 4: Enable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="6d53d-118">Exempel 5: inaktivera gransknings princip för en Azure SQL-Server för Event Hub</span><span class="sxs-lookup"><span data-stu-id="6d53d-118">Example 5: Disable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="6d53d-119">Exempel 6: Aktivera gransknings princip för logganalys för en Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="6d53d-119">Example 6: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="6d53d-120">Exempel 7: inaktivera gransknings principen för logganalys för en Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="6d53d-120">Example 7: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="6d53d-121">Exempel 8: inaktivera, genom pipeline, gransknings princip för logganalys för en Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="6d53d-121">Example 8: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="6d53d-122">Exempel 9: inaktivera skicka gransknings poster för en Azure SQL Server till Blob Storage och aktivera dem för att logga analyser.</span><span class="sxs-lookup"><span data-stu-id="6d53d-122">Example 9: Disable sending audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="6d53d-123">Exempel 10: Aktivera att skicka gransknings poster för en Azure SQL Server till Blob Storage, hubb och logganalys-analys.</span><span class="sxs-lookup"><span data-stu-id="6d53d-123">Example 10: Enable sending audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="6d53d-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d53d-124">PARAMETERS</span></span>

### <span data-ttu-id="6d53d-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d53d-125">-AsJob</span></span>
<span data-ttu-id="6d53d-126">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6d53d-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d53d-127">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="6d53d-127">-AuditActionGroup</span></span>
<span data-ttu-id="6d53d-128">Den rekommenderade uppsättningen åtgärds grupper som ska användas är följande kombination – detta granskar alla frågor och lagrade procedurer som körs mot databasen samt lyckade och misslyckade inloggningar:</span><span class="sxs-lookup"><span data-stu-id="6d53d-128">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="6d53d-129">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="6d53d-129">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="6d53d-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="6d53d-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="6d53d-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="6d53d-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="6d53d-132">Ovanstående kombination är även den uppsättning som är konfigurerad som standard.</span><span class="sxs-lookup"><span data-stu-id="6d53d-132">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="6d53d-133">Dessa grupper täcker alla SQL-uttryck och lagrade procedurer som körs mot databasen och ska inte användas i kombination med andra grupper eftersom detta kommer att leda till dubbletter av gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="6d53d-133">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="6d53d-134">Mer information finns i https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="6d53d-134">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="6d53d-135">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="6d53d-135">-BlobStorageTargetState</span></span>
<span data-ttu-id="6d53d-136">Anger om Blob Storage är en destination för gransknings poster.</span><span class="sxs-lookup"><span data-stu-id="6d53d-136">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="6d53d-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d53d-137">-DefaultProfile</span></span>
<span data-ttu-id="6d53d-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6d53d-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d53d-139">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="6d53d-139">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="6d53d-140">Resurs-ID för regel för händelsehubben</span><span class="sxs-lookup"><span data-stu-id="6d53d-140">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="6d53d-141">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="6d53d-141">-EventHubName</span></span>
<span data-ttu-id="6d53d-142">Namnet på händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="6d53d-142">The name of the event hub.</span></span> <span data-ttu-id="6d53d-143">Om ingen anges när du tillhandahåller EventHubAuthorizationRuleResourceId väljs standard händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="6d53d-143">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="6d53d-144">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="6d53d-144">-EventHubTargetState</span></span>
<span data-ttu-id="6d53d-145">Anger om händelsehubben är en mål för gransknings poster.</span><span class="sxs-lookup"><span data-stu-id="6d53d-145">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="6d53d-146">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="6d53d-146">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="6d53d-147">Anger om logg analys är en destination för gransknings poster.</span><span class="sxs-lookup"><span data-stu-id="6d53d-147">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="6d53d-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d53d-148">-PassThru</span></span>
<span data-ttu-id="6d53d-149">Anger om gransknings principen ska sparas när cmdlet körs</span><span class="sxs-lookup"><span data-stu-id="6d53d-149">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="6d53d-150">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="6d53d-150">-PredicateExpression</span></span>
<span data-ttu-id="6d53d-151">Uttrycket T-SQL predikat (WHERE-satsen) som används för att filtrera gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="6d53d-151">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="6d53d-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d53d-152">-ResourceGroupName</span></span>
<span data-ttu-id="6d53d-153">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6d53d-153">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d53d-154">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="6d53d-154">-RetentionInDays</span></span>
<span data-ttu-id="6d53d-155">Antalet bevarande dagar för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="6d53d-155">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="6d53d-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6d53d-156">-ServerName</span></span>
<span data-ttu-id="6d53d-157">SQL Server-namn.</span><span class="sxs-lookup"><span data-stu-id="6d53d-157">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d53d-158">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="6d53d-158">-ServerObject</span></span>
<span data-ttu-id="6d53d-159">Serverobjektet för att hantera dess gransknings princip.</span><span class="sxs-lookup"><span data-stu-id="6d53d-159">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d53d-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="6d53d-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="6d53d-161">Resurs-ID för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="6d53d-161">The storage account resource id</span></span>

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

### <span data-ttu-id="6d53d-162">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="6d53d-162">-StorageKeyType</span></span>
<span data-ttu-id="6d53d-163">Anger vilken av lagrings åtkomst nycklar som ska användas.</span><span class="sxs-lookup"><span data-stu-id="6d53d-163">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="6d53d-164">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="6d53d-164">-WorkspaceResourceId</span></span>
<span data-ttu-id="6d53d-165">Arbetsyte-ID (resurs-ID för en logganalys-arbetsyta) för en logganalys-arbetsyta som du vill skicka gransknings loggar till.</span><span class="sxs-lookup"><span data-stu-id="6d53d-165">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="6d53d-166">Exempel:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="6d53d-166">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="6d53d-167">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6d53d-167">-Confirm</span></span>
<span data-ttu-id="6d53d-168">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6d53d-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d53d-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d53d-169">-WhatIf</span></span>
<span data-ttu-id="6d53d-170">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6d53d-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d53d-171">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6d53d-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d53d-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d53d-172">CommonParameters</span></span>
<span data-ttu-id="6d53d-173">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d53d-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d53d-174">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d53d-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d53d-175">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d53d-175">INPUTS</span></span>

### <span data-ttu-id="6d53d-176">System. String</span><span class="sxs-lookup"><span data-stu-id="6d53d-176">System.String</span></span>

### <span data-ttu-id="6d53d-177">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="6d53d-177">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="6d53d-178">Microsoft. Azure. commands. SQL. granskning. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="6d53d-178">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="6d53d-179">System. GUID</span><span class="sxs-lookup"><span data-stu-id="6d53d-179">System.Guid</span></span>

### <span data-ttu-id="6d53d-180">System. Nullable ' 1 [[system. UInt32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6d53d-180">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6d53d-181">Microsoft. Azure. commands. SQL. granskning. Model. ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="6d53d-181">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="6d53d-182">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d53d-182">OUTPUTS</span></span>

### <span data-ttu-id="6d53d-183">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6d53d-183">System.Boolean</span></span>

## <span data-ttu-id="6d53d-184">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d53d-184">NOTES</span></span>

## <span data-ttu-id="6d53d-185">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d53d-185">RELATED LINKS</span></span>