---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
ms.openlocfilehash: 44db866488459382a3b66f77328b5cbc9259754b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746484"
---
# <span data-ttu-id="202ca-101">Set-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="202ca-101">Set-AzSqlServerAuditing</span></span>

## <span data-ttu-id="202ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="202ca-102">SYNOPSIS</span></span>
<span data-ttu-id="202ca-103">Ändrar gransknings inställningarna för en Azure SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="202ca-103">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="202ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="202ca-104">SYNTAX</span></span>

### <span data-ttu-id="202ca-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="202ca-105">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="202ca-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="202ca-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="202ca-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="202ca-107">EventHubSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="202ca-108">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="202ca-108">LogAnalyticsSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="202ca-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="202ca-109">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="202ca-110">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="202ca-110">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="202ca-111">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="202ca-111">EventHubByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="202ca-112">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="202ca-112">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="202ca-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="202ca-113">DESCRIPTION</span></span>
<span data-ttu-id="202ca-114">Cmdleten **set-AzSqlServerAuditing** ändrar gransknings inställningarna för en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="202ca-114">The **Set-AzSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="202ca-115">Använd cmdleten *ResourceGroupName* och *servername* för att identifiera servern.</span><span class="sxs-lookup"><span data-stu-id="202ca-115">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="202ca-116">Mål platsen för gransknings loggar bestäms genom att ange en av följande växel parametrar: BlobStorage, LogAnalytics eller EventHub (om ingen är angiven är standardvärdet BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="202ca-116">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="202ca-117">Använd parametern *State* för att aktivera/inaktivera principen.</span><span class="sxs-lookup"><span data-stu-id="202ca-117">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="202ca-118">När mål för gransknings loggar är en blob-lagring anger du parametern *StorageAccountName* för att fastställa lagrings konto för gransknings loggar och parametern *StorageKeyType* för att definiera lagrings nycklarna.</span><span class="sxs-lookup"><span data-stu-id="202ca-118">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="202ca-119">Du kan också definiera bevarande för gransknings loggar genom att ange värdet för *RetentionInDays* -parametern för att definiera perioden för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="202ca-119">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="202ca-120">Om cmdleten lyckas och du använder parametern *Passthru* returneras ett objekt som beskriver de aktuella gransknings inställningarna, utöver Server-ID.</span><span class="sxs-lookup"><span data-stu-id="202ca-120">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the server identifiers.</span></span>
<span data-ttu-id="202ca-121">Server-ID: n inkluderar, men är inte begränsade till, **ResourceGroupName** och **servername**.</span><span class="sxs-lookup"><span data-stu-id="202ca-121">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="202ca-122">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="202ca-122">EXAMPLES</span></span>

### <span data-ttu-id="202ca-123">Exempel 1: Aktivera gransknings princip för blob-lagring för en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="202ca-123">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="202ca-124">Exempel 2: inaktivera gransknings princip för blob-lagring för en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="202ca-124">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="202ca-125">Exempel 3: Aktivera gransknings princip för blob-lagring för en Azure SQL Server med ett lagrings konto från ett annat abonnemang</span><span class="sxs-lookup"><span data-stu-id="202ca-125">Example 3: Enable the blob storage auditing policy of an Azure SQL server using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="202ca-126">Exempel 4: Aktivera gransknings princip för blob-lagring för en Azure SQL Server med avancerad filtrering med ett T-SQL-predikat</span><span class="sxs-lookup"><span data-stu-id="202ca-126">Example 4: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="202ca-127">Exempel 5: ta bort inställningen Advanced filter from lagrings principen för BLOB-granskning för en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="202ca-127">Example 5: Remove the advanced filtering setting from the blob auditing storage policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression ""
```

### <span data-ttu-id="202ca-128">Exempel 6: Aktivera gransknings principen för händelsehubben för en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="202ca-128">Example 6: Enable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="202ca-129">Exempel 7: inaktivera gransknings princip för en Azure SQL-Server för händelsehubben</span><span class="sxs-lookup"><span data-stu-id="202ca-129">Example 7: Disable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubName
```

### <span data-ttu-id="202ca-130">Exempel 8: Aktivera gransknings princip för logganalys för en Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="202ca-130">Example 8: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="202ca-131">Exempel 9: inaktivera gransknings principen för logganalys-SQL-servern</span><span class="sxs-lookup"><span data-stu-id="202ca-131">Example 9: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics
```

### <span data-ttu-id="202ca-132">Exempel 10: inaktivera, genom pipeline, gransknings princip för logganalys för en Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="202ca-132">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="202ca-133">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="202ca-133">PARAMETERS</span></span>

### <span data-ttu-id="202ca-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="202ca-134">-AsJob</span></span>
<span data-ttu-id="202ca-135">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="202ca-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="202ca-136">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="202ca-136">-AuditActionGroup</span></span>
<span data-ttu-id="202ca-137">Den rekommenderade uppsättningen åtgärds grupper som ska användas är följande kombination – detta granskar alla frågor och lagrade procedurer som körs mot databasen samt lyckade och misslyckade inloggningar:</span><span class="sxs-lookup"><span data-stu-id="202ca-137">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="202ca-138">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="202ca-138">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="202ca-139">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="202ca-139">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="202ca-140">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="202ca-140">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="202ca-141">Ovanstående kombination är även den uppsättning som är konfigurerad som standard.</span><span class="sxs-lookup"><span data-stu-id="202ca-141">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="202ca-142">Dessa grupper täcker alla SQL-uttryck och lagrade procedurer som körs mot databasen och ska inte användas i kombination med andra grupper eftersom detta kommer att leda till dubbletter av gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="202ca-142">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="202ca-143">Mer information finns i https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="202ca-143">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="202ca-144">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="202ca-144">-BlobStorage</span></span>
<span data-ttu-id="202ca-145">Anger att gransknings loggar destinationen är Blob Storage</span><span class="sxs-lookup"><span data-stu-id="202ca-145">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="202ca-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="202ca-146">-DefaultProfile</span></span>
<span data-ttu-id="202ca-147">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="202ca-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="202ca-148">-EventHub</span><span class="sxs-lookup"><span data-stu-id="202ca-148">-EventHub</span></span>
<span data-ttu-id="202ca-149">Anger att gransknings loggar destinationen är händelsehubben</span><span class="sxs-lookup"><span data-stu-id="202ca-149">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="202ca-150">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="202ca-150">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="202ca-151">Resurs-ID för regel för händelsehubben</span><span class="sxs-lookup"><span data-stu-id="202ca-151">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="202ca-152">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="202ca-152">-EventHubName</span></span>
<span data-ttu-id="202ca-153">Namnet på händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="202ca-153">The name of the event hub.</span></span> <span data-ttu-id="202ca-154">Om ingen anges när du tillhandahåller EventHubAuthorizationRuleResourceId väljs standard händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="202ca-154">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="202ca-155">-InputObject</span><span class="sxs-lookup"><span data-stu-id="202ca-155">-InputObject</span></span>
<span data-ttu-id="202ca-156">Serverobjektet för att hantera dess gransknings princip.</span><span class="sxs-lookup"><span data-stu-id="202ca-156">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="202ca-157">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="202ca-157">-LogAnalytics</span></span>
<span data-ttu-id="202ca-158">Anger att gransknings loggar destinationen är logg analys</span><span class="sxs-lookup"><span data-stu-id="202ca-158">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="202ca-159">-PassThru</span><span class="sxs-lookup"><span data-stu-id="202ca-159">-PassThru</span></span>
<span data-ttu-id="202ca-160">Anger om gransknings principen ska sparas när cmdlet körs</span><span class="sxs-lookup"><span data-stu-id="202ca-160">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="202ca-161">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="202ca-161">-PredicateExpression</span></span>
<span data-ttu-id="202ca-162">Uttrycket T-SQL predikat (WHERE-satsen) som används för att filtrera gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="202ca-162">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="202ca-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="202ca-163">-ResourceGroupName</span></span>
<span data-ttu-id="202ca-164">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="202ca-164">The name of the resource group.</span></span>

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

### <span data-ttu-id="202ca-165">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="202ca-165">-RetentionInDays</span></span>
<span data-ttu-id="202ca-166">Antalet bevarande dagar för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="202ca-166">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="202ca-167">-ServerName</span><span class="sxs-lookup"><span data-stu-id="202ca-167">-ServerName</span></span>
<span data-ttu-id="202ca-168">SQL Server-namn.</span><span class="sxs-lookup"><span data-stu-id="202ca-168">SQL server name.</span></span>

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

### <span data-ttu-id="202ca-169">-State</span><span class="sxs-lookup"><span data-stu-id="202ca-169">-State</span></span>
<span data-ttu-id="202ca-170">Tillståndet för policyn.</span><span class="sxs-lookup"><span data-stu-id="202ca-170">The state of the policy.</span></span>

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

### <span data-ttu-id="202ca-171">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="202ca-171">-StorageAccountName</span></span>
<span data-ttu-id="202ca-172">Namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="202ca-172">The name of the storage account.</span></span>

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

### <span data-ttu-id="202ca-173">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="202ca-173">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="202ca-174">ID för abonnemang för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="202ca-174">The storage account subscription id</span></span>

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

### <span data-ttu-id="202ca-175">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="202ca-175">-StorageKeyType</span></span>
<span data-ttu-id="202ca-176">Anger vilken av lagrings åtkomst nycklar som ska användas.</span><span class="sxs-lookup"><span data-stu-id="202ca-176">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="202ca-177">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="202ca-177">-WorkspaceResourceId</span></span>
<span data-ttu-id="202ca-178">Arbetsyte-ID (resurs-ID för en logganalys-arbetsyta) för en logganalys-arbetsyta som du vill skicka gransknings loggar till.</span><span class="sxs-lookup"><span data-stu-id="202ca-178">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="202ca-179">Exempel:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="202ca-179">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="202ca-180">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="202ca-180">-Confirm</span></span>
<span data-ttu-id="202ca-181">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="202ca-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="202ca-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="202ca-182">-WhatIf</span></span>
<span data-ttu-id="202ca-183">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="202ca-183">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="202ca-184">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="202ca-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="202ca-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="202ca-185">CommonParameters</span></span>
<span data-ttu-id="202ca-186">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="202ca-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="202ca-187">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="202ca-187">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="202ca-188">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="202ca-188">INPUTS</span></span>

### <span data-ttu-id="202ca-189">System. String</span><span class="sxs-lookup"><span data-stu-id="202ca-189">System.String</span></span>

### <span data-ttu-id="202ca-190">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="202ca-190">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="202ca-191">Microsoft. Azure. commands. SQL. granskning. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="202ca-191">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="202ca-192">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="202ca-192">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="202ca-193">System. GUID</span><span class="sxs-lookup"><span data-stu-id="202ca-193">System.Guid</span></span>

### <span data-ttu-id="202ca-194">System. Nullable ' 1 [[system. UInt32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="202ca-194">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="202ca-195">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="202ca-195">OUTPUTS</span></span>

### <span data-ttu-id="202ca-196">Microsoft. Azure. commands. SQL. granskning. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="202ca-196">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="202ca-197">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="202ca-197">NOTES</span></span>

## <span data-ttu-id="202ca-198">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="202ca-198">RELATED LINKS</span></span>
