---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 5eedeea96f7c1c2491e7388734b51977cb0dd1c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575449"
---
# <span data-ttu-id="4973c-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="4973c-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="4973c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4973c-102">SYNOPSIS</span></span>
<span data-ttu-id="4973c-103">Ändrar gransknings inställningarna för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="4973c-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4973c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4973c-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4973c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4973c-105">DESCRIPTION</span></span>
<span data-ttu-id="4973c-106">Cmdleten **set-AzureRmSqlDatabaseAuditing** ändrar gransknings inställningarna för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="4973c-106">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="4973c-107">Använd cmdleten *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="4973c-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="4973c-108">Ange *StorageAccountName* -parametern för att ange lagrings konto för gransknings loggar och parametern *StorageKeyType* för att definiera lagrings nycklarna.</span><span class="sxs-lookup"><span data-stu-id="4973c-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="4973c-109">Använd parametern *State* för att aktivera/inaktivera principen.</span><span class="sxs-lookup"><span data-stu-id="4973c-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="4973c-110">Du kan också definiera bevarande för gransknings loggar genom att ange värdet för *RetentionInDays* -parametern för att definiera perioden för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="4973c-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="4973c-111">När cmdleten körs är den aktive rad.</span><span class="sxs-lookup"><span data-stu-id="4973c-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="4973c-112">Om cmdleten lyckas och du använder parametern *Passthru* returneras ett objekt som beskriver den aktuella BLOB-granskningen utöver databas identifierarna.</span><span class="sxs-lookup"><span data-stu-id="4973c-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="4973c-113">Databas identifierare inkluderar, men är inte begränsade till, **ResourceGroupName** , **servername** och **databasename**.</span><span class="sxs-lookup"><span data-stu-id="4973c-113">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="4973c-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4973c-114">EXAMPLES</span></span>

### <span data-ttu-id="4973c-115">Exempel 1: Aktivera gransknings principen för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="4973c-115">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="4973c-116">Exempel 2: inaktivera en BLOB-gransknings princip för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="4973c-116">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

## <span data-ttu-id="4973c-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4973c-117">PARAMETERS</span></span>

### <span data-ttu-id="4973c-118">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="4973c-118">-AuditAction</span></span>
<span data-ttu-id="4973c-119">Uppsättningen gransknings åtgärder.</span><span class="sxs-lookup"><span data-stu-id="4973c-119">The set of audit actions.</span></span>  
<span data-ttu-id="4973c-120">De åtgärder som stöds för granskning är:</span><span class="sxs-lookup"><span data-stu-id="4973c-120">The supported actions to audit are:</span></span>  
<span data-ttu-id="4973c-121">ANVÄNDA</span><span class="sxs-lookup"><span data-stu-id="4973c-121">SELECT</span></span>  
<span data-ttu-id="4973c-122">UPPDATERA</span><span class="sxs-lookup"><span data-stu-id="4973c-122">UPDATE</span></span>  
<span data-ttu-id="4973c-123">Placera</span><span class="sxs-lookup"><span data-stu-id="4973c-123">INSERT</span></span>  
<span data-ttu-id="4973c-124">TA bort</span><span class="sxs-lookup"><span data-stu-id="4973c-124">DELETE</span></span>  
<span data-ttu-id="4973c-125">GENOMFÖR</span><span class="sxs-lookup"><span data-stu-id="4973c-125">EXECUTE</span></span>  
<span data-ttu-id="4973c-126">MOTTAR</span><span class="sxs-lookup"><span data-stu-id="4973c-126">RECEIVE</span></span>  
<span data-ttu-id="4973c-127">INNEHÅLLER</span><span class="sxs-lookup"><span data-stu-id="4973c-127">REFERENCES</span></span>  

<span data-ttu-id="4973c-128">Det allmänna formuläret för att definiera en åtgärd som ska granskas är:</span><span class="sxs-lookup"><span data-stu-id="4973c-128">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="4973c-129">fattning [Object] av [kapital]</span><span class="sxs-lookup"><span data-stu-id="4973c-129">[action] ON [object] BY [principal]</span></span>

<span data-ttu-id="4973c-130">Observera att [objekt] i ovanstående format kan referera till ett objekt, till exempel en tabell, en vy eller en lagrad procedur eller en hel databas eller ett helt schema.</span><span class="sxs-lookup"><span data-stu-id="4973c-130">Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="4973c-131">För de sistnämnda fallen används formulär databasen:: [dbname] och SCHEMA:: [SchemaName].</span><span class="sxs-lookup"><span data-stu-id="4973c-131">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>

<span data-ttu-id="4973c-132">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="4973c-132">For example:</span></span>  
<span data-ttu-id="4973c-133">Välj i dbo. nontable av offentlig</span><span class="sxs-lookup"><span data-stu-id="4973c-133">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="4973c-134">Välj på databas:: min databas av offentlig</span><span class="sxs-lookup"><span data-stu-id="4973c-134">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="4973c-135">Välj på SCHEMA:: mina schema av offentlig</span><span class="sxs-lookup"><span data-stu-id="4973c-135">SELECT on SCHEMA::mySchema by public</span></span>  

<span data-ttu-id="4973c-136">Mer information finns i https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="4973c-136">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4973c-137">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="4973c-137">-AuditActionGroup</span></span>
<span data-ttu-id="4973c-138">Den rekommenderade uppsättningen åtgärds grupper som ska användas är följande kombination – detta granskar alla frågor och lagrade procedurer som körs mot databasen samt lyckade och misslyckade inloggningar:</span><span class="sxs-lookup"><span data-stu-id="4973c-138">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="4973c-139">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="4973c-139">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="4973c-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="4973c-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="4973c-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="4973c-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  

<span data-ttu-id="4973c-142">Ovanstående kombination är även den uppsättning som är konfigurerad som standard.</span><span class="sxs-lookup"><span data-stu-id="4973c-142">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="4973c-143">Dessa grupper täcker alla SQL-uttryck och lagrade procedurer som körs mot databasen och ska inte användas i kombination med andra grupper eftersom detta kommer att leda till dubbletter av gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="4973c-143">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="4973c-144">Mer information finns i https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="4973c-144">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4973c-145">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4973c-145">-DatabaseName</span></span>
<span data-ttu-id="4973c-146">Namn på SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="4973c-146">SQL Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4973c-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4973c-147">-DefaultProfile</span></span>
<span data-ttu-id="4973c-148">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4973c-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4973c-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4973c-149">-PassThru</span></span>
<span data-ttu-id="4973c-150">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4973c-150">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4973c-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4973c-151">-ResourceGroupName</span></span>
<span data-ttu-id="4973c-152">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4973c-152">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4973c-153">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="4973c-153">-RetentionInDays</span></span>
<span data-ttu-id="4973c-154">Antalet bevarande dagar för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="4973c-154">The number of retention days for the audit logs.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4973c-155">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4973c-155">-ServerName</span></span>
<span data-ttu-id="4973c-156">Server namn för SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="4973c-156">SQL Database server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4973c-157">-State</span><span class="sxs-lookup"><span data-stu-id="4973c-157">-State</span></span>
<span data-ttu-id="4973c-158">Tillståndet för policyn.</span><span class="sxs-lookup"><span data-stu-id="4973c-158">The state of the policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4973c-159">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4973c-159">-StorageAccountName</span></span>
<span data-ttu-id="4973c-160">Namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="4973c-160">The name of the storage account.</span></span> <span data-ttu-id="4973c-161">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="4973c-161">Wildcard characters are not permitted.</span></span>  
<span data-ttu-id="4973c-162">Denna parameter är inte obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="4973c-162">This parameter is not required.</span></span>  
<span data-ttu-id="4973c-163">Om du inte anger den här parametern använder cmdleten det lagrings konto som har definierats tidigare som en del av gransknings principen.</span><span class="sxs-lookup"><span data-stu-id="4973c-163">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>  
<span data-ttu-id="4973c-164">Om det är första gången en gransknings princip definieras och du inte anger den här parametern Miss lyckas cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4973c-164">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4973c-165">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="4973c-165">-StorageKeyType</span></span>
<span data-ttu-id="4973c-166">Anger vilken av lagrings åtkomst nycklar som ska användas.</span><span class="sxs-lookup"><span data-stu-id="4973c-166">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4973c-167">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4973c-167">-Confirm</span></span>
<span data-ttu-id="4973c-168">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4973c-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4973c-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4973c-169">-WhatIf</span></span>
<span data-ttu-id="4973c-170">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4973c-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4973c-171">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4973c-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4973c-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4973c-172">CommonParameters</span></span>
<span data-ttu-id="4973c-173">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4973c-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4973c-174">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4973c-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4973c-175">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4973c-175">INPUTS</span></span>

### <span data-ttu-id="4973c-176">Ingen</span><span class="sxs-lookup"><span data-stu-id="4973c-176">None</span></span>
<span data-ttu-id="4973c-177">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4973c-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4973c-178">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4973c-178">OUTPUTS</span></span>

### <span data-ttu-id="4973c-179">Microsoft. Azure. commands. SQL. Security. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="4973c-179">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="4973c-180">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4973c-180">NOTES</span></span>

## <span data-ttu-id="4973c-181">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4973c-181">RELATED LINKS</span></span>
