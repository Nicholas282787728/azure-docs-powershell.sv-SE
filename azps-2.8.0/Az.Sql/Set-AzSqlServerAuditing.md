---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
ms.openlocfilehash: e9d3e7ca009a756526bc0cb150ebdb6c124df032
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920488"
---
# <span data-ttu-id="80763-101">Set-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="80763-101">Set-AzSqlServerAuditing</span></span>

## <span data-ttu-id="80763-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="80763-102">SYNOPSIS</span></span>
<span data-ttu-id="80763-103">**Viktigt: denna cmdlet är föråldrad, [set-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveraudit) ersätter den.**</span><span class="sxs-lookup"><span data-stu-id="80763-103">**Important: This cmdlet is deprecated, [Set-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveraudit) is replacing it.**</span></span>

<span data-ttu-id="80763-104">Ändrar gransknings inställningarna för en Azure SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="80763-104">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="80763-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="80763-105">SYNTAX</span></span>

### <span data-ttu-id="80763-106">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="80763-106">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80763-107">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="80763-107">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80763-108">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="80763-108">EventHubSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80763-109">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="80763-109">LogAnalyticsSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80763-110">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="80763-110">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80763-111">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="80763-111">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80763-112">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="80763-112">EventHubByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80763-113">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="80763-113">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80763-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="80763-114">DESCRIPTION</span></span>
<span data-ttu-id="80763-115">Cmdleten **set-AzSqlServerAuditing** ändrar gransknings inställningarna för en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="80763-115">The **Set-AzSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="80763-116">Använd cmdleten *ResourceGroupName* och *servername* för att identifiera servern.</span><span class="sxs-lookup"><span data-stu-id="80763-116">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="80763-117">Mål platsen för gransknings loggar bestäms genom att ange en av följande växel parametrar: BlobStorage, LogAnalytics eller EventHub (om ingen är angiven är standardvärdet BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="80763-117">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="80763-118">Använd parametern *State* för att aktivera/inaktivera principen.</span><span class="sxs-lookup"><span data-stu-id="80763-118">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="80763-119">När mål för gransknings loggar är en blob-lagring anger du parametern *StorageAccountName* för att fastställa lagrings konto för gransknings loggar och parametern *StorageKeyType* för att definiera lagrings nycklarna.</span><span class="sxs-lookup"><span data-stu-id="80763-119">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="80763-120">Du kan också definiera bevarande för gransknings loggar genom att ange värdet för *RetentionInDays* -parametern för att definiera perioden för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="80763-120">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="80763-121">Om cmdleten lyckas och du använder parametern *Passthru* returneras ett objekt som beskriver de aktuella gransknings inställningarna, utöver Server-ID.</span><span class="sxs-lookup"><span data-stu-id="80763-121">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the server identifiers.</span></span>
<span data-ttu-id="80763-122">Server-ID: n inkluderar, men är inte begränsade till, **ResourceGroupName** och **servername**.</span><span class="sxs-lookup"><span data-stu-id="80763-122">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="80763-123">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="80763-123">EXAMPLES</span></span>

### <span data-ttu-id="80763-124">Exempel 1: Aktivera gransknings princip för blob-lagring för en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="80763-124">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="80763-125">Exempel 2: inaktivera gransknings princip för blob-lagring för en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="80763-125">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="80763-126">Exempel 3: Aktivera gransknings princip för blob-lagring för en Azure SQL Server med ett lagrings konto från ett annat abonnemang</span><span class="sxs-lookup"><span data-stu-id="80763-126">Example 3: Enable the blob storage auditing policy of an Azure SQL server using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="80763-127">Exempel 4: Aktivera gransknings princip för blob-lagring för en Azure SQL Server med avancerad filtrering med ett T-SQL-predikat</span><span class="sxs-lookup"><span data-stu-id="80763-127">Example 4: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="80763-128">Exempel 5: ta bort inställningen Advanced filter from lagrings principen för BLOB-granskning för en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="80763-128">Example 5: Remove the advanced filtering setting from the blob auditing storage policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression ""
```

### <span data-ttu-id="80763-129">Exempel 6: Aktivera gransknings principen för händelsehubben för en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="80763-129">Example 6: Enable the event hub auditing policy of an Azure SQL server</span></span>
```
$EventHubAuthorizationRule = Get-AzEventHubAuthorizationRule `
    -ResourceGroupName "ResourceGroup01" `
    -Namespace "EventHubName" `
    -Name "SharedAccessPoliceName" 

Set-AzSqlServerAuditing `
    -State Enabled `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -EventHub `
    -EventHubName "EventHubName" `
    -EventHubAuthorizationRuleResourceId $EventHubAuthorizationRule.Id
```

### <span data-ttu-id="80763-130">Exempel 7: inaktivera gransknings princip för en Azure SQL-Server för händelsehubben</span><span class="sxs-lookup"><span data-stu-id="80763-130">Example 7: Disable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubName
```

### <span data-ttu-id="80763-131">Exempel 8: Aktivera gransknings princip för logganalys för en Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="80763-131">Example 8: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="80763-132">Exempel 9: inaktivera gransknings principen för logganalys-SQL-servern</span><span class="sxs-lookup"><span data-stu-id="80763-132">Example 9: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics
```

### <span data-ttu-id="80763-133">Exempel 10: inaktivera, genom pipeline, gransknings princip för logganalys för en Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="80763-133">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="80763-134">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="80763-134">PARAMETERS</span></span>

### <span data-ttu-id="80763-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80763-135">-AsJob</span></span>
<span data-ttu-id="80763-136">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="80763-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80763-137">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="80763-137">-AuditActionGroup</span></span>
<span data-ttu-id="80763-138">Den rekommenderade uppsättningen åtgärds grupper som ska användas är följande kombination – detta granskar alla frågor och lagrade procedurer som körs mot databasen samt lyckade och misslyckade inloggningar:</span><span class="sxs-lookup"><span data-stu-id="80763-138">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="80763-139">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="80763-139">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="80763-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="80763-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="80763-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="80763-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="80763-142">Ovanstående kombination är även den uppsättning som är konfigurerad som standard.</span><span class="sxs-lookup"><span data-stu-id="80763-142">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="80763-143">Dessa grupper täcker alla SQL-uttryck och lagrade procedurer som körs mot databasen och ska inte användas i kombination med andra grupper eftersom detta kommer att leda till dubbletter av gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="80763-143">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="80763-144">Mer information finns i https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="80763-144">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="80763-145">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="80763-145">-BlobStorage</span></span>
<span data-ttu-id="80763-146">Anger att gransknings loggar destinationen är Blob Storage</span><span class="sxs-lookup"><span data-stu-id="80763-146">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="80763-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80763-147">-DefaultProfile</span></span>
<span data-ttu-id="80763-148">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="80763-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80763-149">-EventHub</span><span class="sxs-lookup"><span data-stu-id="80763-149">-EventHub</span></span>
<span data-ttu-id="80763-150">Anger att gransknings loggar destinationen är händelsehubben</span><span class="sxs-lookup"><span data-stu-id="80763-150">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="80763-151">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="80763-151">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="80763-152">Resurs-ID för regel för händelsehubben</span><span class="sxs-lookup"><span data-stu-id="80763-152">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="80763-153">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="80763-153">-EventHubName</span></span>
<span data-ttu-id="80763-154">Namnet på händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="80763-154">The name of the event hub.</span></span> <span data-ttu-id="80763-155">Om ingen anges när du tillhandahåller EventHubAuthorizationRuleResourceId väljs standard händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="80763-155">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="80763-156">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80763-156">-InputObject</span></span>
<span data-ttu-id="80763-157">Serverobjektet för att hantera dess gransknings princip.</span><span class="sxs-lookup"><span data-stu-id="80763-157">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="80763-158">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="80763-158">-LogAnalytics</span></span>
<span data-ttu-id="80763-159">Anger att gransknings loggar destinationen är logg analys</span><span class="sxs-lookup"><span data-stu-id="80763-159">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="80763-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80763-160">-PassThru</span></span>
<span data-ttu-id="80763-161">Anger om gransknings principen ska sparas när cmdlet körs</span><span class="sxs-lookup"><span data-stu-id="80763-161">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="80763-162">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="80763-162">-PredicateExpression</span></span>
<span data-ttu-id="80763-163">Uttrycket T-SQL predikat (WHERE-satsen) som används för att filtrera gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="80763-163">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="80763-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80763-164">-ResourceGroupName</span></span>
<span data-ttu-id="80763-165">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="80763-165">The name of the resource group.</span></span>

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

### <span data-ttu-id="80763-166">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="80763-166">-RetentionInDays</span></span>
<span data-ttu-id="80763-167">Antalet bevarande dagar för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="80763-167">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="80763-168">-ServerName</span><span class="sxs-lookup"><span data-stu-id="80763-168">-ServerName</span></span>
<span data-ttu-id="80763-169">SQL Server-namn.</span><span class="sxs-lookup"><span data-stu-id="80763-169">SQL server name.</span></span>

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

### <span data-ttu-id="80763-170">-State</span><span class="sxs-lookup"><span data-stu-id="80763-170">-State</span></span>
<span data-ttu-id="80763-171">Tillståndet för policyn.</span><span class="sxs-lookup"><span data-stu-id="80763-171">The state of the policy.</span></span>

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

### <span data-ttu-id="80763-172">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="80763-172">-StorageAccountName</span></span>
<span data-ttu-id="80763-173">Namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="80763-173">The name of the storage account.</span></span>

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

### <span data-ttu-id="80763-174">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80763-174">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="80763-175">ID för abonnemang för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="80763-175">The storage account subscription id</span></span>

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

### <span data-ttu-id="80763-176">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="80763-176">-StorageKeyType</span></span>
<span data-ttu-id="80763-177">Anger vilken av lagrings åtkomst nycklar som ska användas.</span><span class="sxs-lookup"><span data-stu-id="80763-177">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="80763-178">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="80763-178">-WorkspaceResourceId</span></span>
<span data-ttu-id="80763-179">Arbetsyte-ID (resurs-ID för en logganalys-arbetsyta) för en logganalys-arbetsyta som du vill skicka gransknings loggar till.</span><span class="sxs-lookup"><span data-stu-id="80763-179">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="80763-180">Exempel:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="80763-180">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="80763-181">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="80763-181">-Confirm</span></span>
<span data-ttu-id="80763-182">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="80763-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80763-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80763-183">-WhatIf</span></span>
<span data-ttu-id="80763-184">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="80763-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80763-185">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="80763-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80763-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80763-186">CommonParameters</span></span>
<span data-ttu-id="80763-187">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80763-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80763-188">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80763-188">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80763-189">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="80763-189">INPUTS</span></span>

### <span data-ttu-id="80763-190">System. String</span><span class="sxs-lookup"><span data-stu-id="80763-190">System.String</span></span>

### <span data-ttu-id="80763-191">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="80763-191">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="80763-192">Microsoft. Azure. commands. SQL. granskning. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="80763-192">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="80763-193">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="80763-193">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="80763-194">System. GUID</span><span class="sxs-lookup"><span data-stu-id="80763-194">System.Guid</span></span>

### <span data-ttu-id="80763-195">System. Nullable ' 1 [[system. UInt32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="80763-195">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="80763-196">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="80763-196">OUTPUTS</span></span>

### <span data-ttu-id="80763-197">Microsoft. Azure. commands. SQL. granskning. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="80763-197">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="80763-198">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="80763-198">NOTES</span></span>

## <span data-ttu-id="80763-199">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="80763-199">RELATED LINKS</span></span>
