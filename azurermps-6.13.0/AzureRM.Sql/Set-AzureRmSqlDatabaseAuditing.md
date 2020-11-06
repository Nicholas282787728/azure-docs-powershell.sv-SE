---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: e28295a5f743e1475075e93a52c21bba8bd83e08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574769"
---
# <span data-ttu-id="3f890-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="3f890-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="3f890-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f890-102">SYNOPSIS</span></span>
<span data-ttu-id="3f890-103">Ändrar gransknings inställningarna för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="3f890-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f890-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f890-104">SYNTAX</span></span>

### <span data-ttu-id="3f890-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3f890-105">DefaultParameterSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f890-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="3f890-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] -StorageAccountName <String> [-StorageAccountSubscriptionId <Guid>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f890-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f890-107">DESCRIPTION</span></span>
<span data-ttu-id="3f890-108">Cmdleten **set-AzureRmSqlDatabaseAuditing** ändrar gransknings inställningarna för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="3f890-108">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="3f890-109">Använd cmdleten *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="3f890-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="3f890-110">Ange *StorageAccountName* -parametern för att ange lagrings konto för gransknings loggar och parametern *StorageKeyType* för att definiera lagrings nycklarna.</span><span class="sxs-lookup"><span data-stu-id="3f890-110">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="3f890-111">Använd parametern *State* för att aktivera/inaktivera principen.</span><span class="sxs-lookup"><span data-stu-id="3f890-111">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="3f890-112">Du kan också definiera bevarande för gransknings loggar genom att ange värdet för *RetentionInDays* -parametern för att definiera perioden för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="3f890-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="3f890-113">När cmdleten körs är den aktive rad.</span><span class="sxs-lookup"><span data-stu-id="3f890-113">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="3f890-114">Om cmdleten lyckas och du använder parametern *Passthru* returneras ett objekt som beskriver den aktuella BLOB-granskningen utöver databas identifierarna.</span><span class="sxs-lookup"><span data-stu-id="3f890-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="3f890-115">Databas identifierare inkluderar, men är inte begränsade till, **ResourceGroupName** , **servername** och **databasename**.</span><span class="sxs-lookup"><span data-stu-id="3f890-115">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="3f890-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f890-116">EXAMPLES</span></span>

### <span data-ttu-id="3f890-117">Exempel 1: Aktivera gransknings principen för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="3f890-117">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="3f890-118">Exempel 2: inaktivera en BLOB-gransknings princip för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="3f890-118">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="3f890-119">Exempel 3: Aktivera gransknings principen för en Azure SQL-databas med ett lagrings konto från ett annat abonnemang</span><span class="sxs-lookup"><span data-stu-id="3f890-119">Example 3: Enable the auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="3f890-120">Exempel 4: Aktivera utökad gransknings princip för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="3f890-120">Example 4: Enable the extended auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="3f890-121">Exempel 5: ta bort utökad gransknings princip för en Azure SQL-databas och ange en gransknings princip i stället för den.</span><span class="sxs-lookup"><span data-stu-id="3f890-121">Example 5: Remove the extended auditing policy of an Azure SQL database, and set an auditing policy instead of it.</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

## <span data-ttu-id="3f890-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f890-122">PARAMETERS</span></span>

### <span data-ttu-id="3f890-123">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="3f890-123">-AuditAction</span></span>
<span data-ttu-id="3f890-124">Uppsättningen gransknings åtgärder.</span><span class="sxs-lookup"><span data-stu-id="3f890-124">The set of audit actions.</span></span>
<span data-ttu-id="3f890-125">De åtgärder du kan vidta för att granska är: Välj uppdatering Infoga ta emot referenser det allmänna formuläret för att definiera en åtgärd som ska granskas är: [åtgärd] [Object] BY [kapital] OBS! [Object] i ovanstående format kan referera till ett objekt som en tabell, en vy eller en lagrad databas eller ett helt schema.</span><span class="sxs-lookup"><span data-stu-id="3f890-125">The supported actions to audit are: SELECT UPDATE INSERT DELETE EXECUTE RECEIVE REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="3f890-126">För de sistnämnda fallen används formulär databasen:: [dbname] och SCHEMA:: [SchemaName].</span><span class="sxs-lookup"><span data-stu-id="3f890-126">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="3f890-127">Till exempel: Välj i dbo. nontable av Public SELECT on databas:: min databas genom Public SELECT on SCHEMA:: preschema by Public mer information finns i https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="3f890-127">For example: SELECT on dbo.myTable by public SELECT on DATABASE::myDatabase by public SELECT on SCHEMA::mySchema by public For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="3f890-128">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="3f890-128">-AuditActionGroup</span></span>
<span data-ttu-id="3f890-129">Den rekommenderade uppsättningen av åtgärds grupper som ska användas är följande kombination – detta granskar alla frågor och lagrade procedurer som körs mot databasen samt lyckade och misslyckade inloggningar: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" ovan är den uppsättning som är konfigurerad som standard.</span><span class="sxs-lookup"><span data-stu-id="3f890-129">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="3f890-130">Dessa grupper täcker alla SQL-uttryck och lagrade procedurer som körs mot databasen och ska inte användas i kombination med andra grupper eftersom detta kommer att leda till dubbletter av gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="3f890-130">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span> <span data-ttu-id="3f890-131">Mer information finns i https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="3f890-131">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f890-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3f890-132">-DatabaseName</span></span>
<span data-ttu-id="3f890-133">Namn på SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="3f890-133">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f890-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f890-134">-DefaultProfile</span></span>
<span data-ttu-id="3f890-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3f890-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f890-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f890-136">-PassThru</span></span>
<span data-ttu-id="3f890-137">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3f890-137">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3f890-138">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="3f890-138">-PredicateExpression</span></span>
<span data-ttu-id="3f890-139">Uttrycket för WHERE-satsen som används för att filtrera gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="3f890-139">The statement of the Where Clause used to filter audit logs.</span></span>

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

### <span data-ttu-id="3f890-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f890-140">-ResourceGroupName</span></span>
<span data-ttu-id="3f890-141">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3f890-141">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f890-142">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="3f890-142">-RetentionInDays</span></span>
<span data-ttu-id="3f890-143">Antalet bevarande dagar för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="3f890-143">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f890-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3f890-144">-ServerName</span></span>
<span data-ttu-id="3f890-145">Server namn för SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="3f890-145">SQL Database server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f890-146">-State</span><span class="sxs-lookup"><span data-stu-id="3f890-146">-State</span></span>
<span data-ttu-id="3f890-147">Tillståndet för policyn.</span><span class="sxs-lookup"><span data-stu-id="3f890-147">The state of the policy.</span></span>

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

### <span data-ttu-id="3f890-148">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3f890-148">-StorageAccountName</span></span>
<span data-ttu-id="3f890-149">Namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="3f890-149">The name of the storage account.</span></span> <span data-ttu-id="3f890-150">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="3f890-150">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="3f890-151">Denna parameter är inte obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="3f890-151">This parameter is not required.</span></span>
<span data-ttu-id="3f890-152">Om du inte anger den här parametern använder cmdleten det lagrings konto som har definierats tidigare som en del av gransknings principen.</span><span class="sxs-lookup"><span data-stu-id="3f890-152">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>
<span data-ttu-id="3f890-153">Om det är första gången en gransknings princip definieras och du inte anger den här parametern Miss lyckas cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3f890-153">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageAccountSubscriptionIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f890-154">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f890-154">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="3f890-155">Anger abonnemangs-ID för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="3f890-155">Specifies storage account subscription id</span></span>

```yaml
Type: System.Guid
Parameter Sets: StorageAccountSubscriptionIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f890-156">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="3f890-156">-StorageKeyType</span></span>
<span data-ttu-id="3f890-157">Anger vilken av lagrings åtkomst nycklar som ska användas.</span><span class="sxs-lookup"><span data-stu-id="3f890-157">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f890-158">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3f890-158">-Confirm</span></span>
<span data-ttu-id="3f890-159">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3f890-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f890-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f890-160">-WhatIf</span></span>
<span data-ttu-id="3f890-161">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3f890-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f890-162">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3f890-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f890-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f890-163">CommonParameters</span></span>
<span data-ttu-id="3f890-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f890-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f890-165">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f890-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f890-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f890-166">INPUTS</span></span>

## <span data-ttu-id="3f890-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f890-167">OUTPUTS</span></span>

## <span data-ttu-id="3f890-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f890-168">NOTES</span></span>

## <span data-ttu-id="3f890-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f890-169">RELATED LINKS</span></span>
