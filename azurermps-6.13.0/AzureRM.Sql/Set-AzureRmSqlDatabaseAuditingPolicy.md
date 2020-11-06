---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: a9f0f2e478e94b45349efe85c6de643b5003a361
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574767"
---
# <span data-ttu-id="0452f-101">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="0452f-101">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="0452f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0452f-102">SYNOPSIS</span></span>
<span data-ttu-id="0452f-103">Anger gransknings principen för en databas.</span><span class="sxs-lookup"><span data-stu-id="0452f-103">Sets the auditing policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0452f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0452f-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditingPolicy [-AuditType <AuditType>] [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-EventType <String[]>]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-TableIdentifier <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0452f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0452f-105">DESCRIPTION</span></span>
<span data-ttu-id="0452f-106">Cmdleten **set-AzureRmSqlDatabaseAuditingPolicy** ändrar gransknings principen för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="0452f-106">The **Set-AzureRmSqlDatabaseAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL database.</span></span>
<span data-ttu-id="0452f-107">Använd cmdleten *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="0452f-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="0452f-108">Ange *StorageAccountName* -parametern för att ange lagrings konto för gransknings loggar och parametern *StorageKeyType* för att definiera lagrings nycklarna.</span><span class="sxs-lookup"><span data-stu-id="0452f-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="0452f-109">Du kan också definiera bevarande för tabellen gransknings loggar genom att ange värdet för parametrarna *RetentionInDays* och *TableIdentifier* för att definiera perioden och dirigeringen för tabell namnen för gransknings loggen.</span><span class="sxs-lookup"><span data-stu-id="0452f-109">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="0452f-110">Ange parametern *EventType* för att definiera vilka händelse typer som ska granskas.</span><span class="sxs-lookup"><span data-stu-id="0452f-110">Specify the *EventType* parameter to define which event types to audit.</span></span>
<span data-ttu-id="0452f-111">När cmdleten körs är den aktive rad.</span><span class="sxs-lookup"><span data-stu-id="0452f-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="0452f-112">För tabell granskning slutar granskning sluta använda den principen om databasen använde serverns princip för granskning innan du körde den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0452f-112">For Table Auditing, if the database used the policy of its server for auditing before you ran this cmdlet, auditing stops using that policy.</span></span> <span data-ttu-id="0452f-113">För att en BLOB-granskning ska visas om databasen använde serverns princip för granskning innan du körde den här cmdleten finns båda gransknings principerna sida vid sida.</span><span class="sxs-lookup"><span data-stu-id="0452f-113">For Blob Auditing, if the database used the policy of its server for auditing before you ran this cmdlet, both auditing policies will exist side-by-side.</span></span>
<span data-ttu-id="0452f-114">Om cmdleten lyckas och du använder *Passthru* -parametern returneras ett objekt som avbeskriverr den aktuella gransknings principen utöver databasens identifierare.</span><span class="sxs-lookup"><span data-stu-id="0452f-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="0452f-115">Databas identifierare inkluderar, men är inte begränsade till, **ResourceGroupName** , **servername** och **databasename**.</span><span class="sxs-lookup"><span data-stu-id="0452f-115">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="0452f-116">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="0452f-116">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0452f-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0452f-117">EXAMPLES</span></span>

### <span data-ttu-id="0452f-118">Exempel 1: Ange gransknings principen för en databas för att använda tabell granskning</span><span class="sxs-lookup"><span data-stu-id="0452f-118">Example 1: Set the auditing policy of a database to use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Table -StorageAccountName "Storage31"
```

<span data-ttu-id="0452f-119">Det här kommandot anger den gransknings princip för databasen som heter Database01 på Server01 för att använda lagrings kontot som heter Storage31.</span><span class="sxs-lookup"><span data-stu-id="0452f-119">This command sets the auditing policy of database named Database01 located on Server01 to use the storage account named Storage31.</span></span>

### <span data-ttu-id="0452f-120">Exempel 2: Ange lagrings konto nycklar för en befintlig gransknings princip för en databas</span><span class="sxs-lookup"><span data-stu-id="0452f-120">Example 2: Set the storage account key of an existing auditing policy of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -StorageAccountKey Secondary
```

<span data-ttu-id="0452f-121">Det här kommandot anger den gransknings princip för databasen som heter Database01 på Server01 för att fortsätta använda samma lagrings konto namn men för att nu använda den sekundära knappen.</span><span class="sxs-lookup"><span data-stu-id="0452f-121">This command sets the auditing policy of database named Database01 located on Server01 to keep using the same storage account name but to now use the secondary key.</span></span>

### <span data-ttu-id="0452f-122">Exempel 3: Ange gransknings principen för en databas för att använda en viss händelse typ</span><span class="sxs-lookup"><span data-stu-id="0452f-122">Example 3: Set the auditing policy of a database to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventType Login_Failure
```

### <span data-ttu-id="0452f-123">Exempel 4: Ange gransknings principen för en databas för att använda BLOB-granskning</span><span class="sxs-lookup"><span data-stu-id="0452f-123">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -AuditAction "UPDATE ON database::[Database01] BY [public]"  -RetentionInDays 8
```

<span data-ttu-id="0452f-124">Det här kommandot anger gransknings principen för databasen som heter Database01 på Server01.</span><span class="sxs-lookup"><span data-stu-id="0452f-124">This command sets the auditing policy of database named Database01 located on Server01.</span></span>
<span data-ttu-id="0452f-125">Principen loggar händelse typen för Login_Failure.</span><span class="sxs-lookup"><span data-stu-id="0452f-125">The policy logs the Login_Failure event type.</span></span>
<span data-ttu-id="0452f-126">Kommandot ändrar inte lagrings inställningarna.</span><span class="sxs-lookup"><span data-stu-id="0452f-126">The command does not change the storage settings.</span></span>

## <span data-ttu-id="0452f-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0452f-127">PARAMETERS</span></span>

### <span data-ttu-id="0452f-128">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="0452f-128">-AuditAction</span></span>
<span data-ttu-id="0452f-129">Ange en eller flera gransknings åtgärder.</span><span class="sxs-lookup"><span data-stu-id="0452f-129">Specify one or more audit actions.</span></span>
<span data-ttu-id="0452f-130">Den här parametern kan endast användas för BLOB-granskning.</span><span class="sxs-lookup"><span data-stu-id="0452f-130">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="0452f-131">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="0452f-131">-AuditActionGroup</span></span>
<span data-ttu-id="0452f-132">Ange en eller flera gransknings åtgärds grupper.</span><span class="sxs-lookup"><span data-stu-id="0452f-132">Specify one or more audit action groups.</span></span>
<span data-ttu-id="0452f-133">Den här parametern kan endast användas för BLOB-granskning.</span><span class="sxs-lookup"><span data-stu-id="0452f-133">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="0452f-134">-AuditType</span><span class="sxs-lookup"><span data-stu-id="0452f-134">-AuditType</span></span>
```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditType
Parameter Sets: (All)
Aliases:
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0452f-135">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0452f-135">-DatabaseName</span></span>
<span data-ttu-id="0452f-136">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="0452f-136">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="0452f-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0452f-137">-DefaultProfile</span></span>
<span data-ttu-id="0452f-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0452f-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0452f-139">-EventType</span><span class="sxs-lookup"><span data-stu-id="0452f-139">-EventType</span></span>
<span data-ttu-id="0452f-140">Anger vilka händelse typer som ska granskas.</span><span class="sxs-lookup"><span data-stu-id="0452f-140">Specifies the event types to audit.</span></span>
<span data-ttu-id="0452f-141">Den här parametern gäller endast för tabell granskning.</span><span class="sxs-lookup"><span data-stu-id="0452f-141">This parameter is only applicable to Table auditing.</span></span>
<span data-ttu-id="0452f-142">Du kan ange flera händelse typer.</span><span class="sxs-lookup"><span data-stu-id="0452f-142">You can specify several event types.</span></span>
<span data-ttu-id="0452f-143">Du kan ange alla om du vill granska alla händelse typer eller inget för att ange att inga händelser ska granskas.</span><span class="sxs-lookup"><span data-stu-id="0452f-143">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="0452f-144">Om du anger alla eller ingen samtidigt körs cmdleten inte.</span><span class="sxs-lookup"><span data-stu-id="0452f-144">If you specify All or None at the same time, the cmdlet does not run.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0452f-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0452f-145">-PassThru</span></span>
<span data-ttu-id="0452f-146">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="0452f-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0452f-147">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="0452f-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0452f-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0452f-148">-ResourceGroupName</span></span>
<span data-ttu-id="0452f-149">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="0452f-149">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="0452f-150">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="0452f-150">-RetentionInDays</span></span>
<span data-ttu-id="0452f-151">Anger antalet bevarande dagar för tabellen gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="0452f-151">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="0452f-152">Värdet noll (0) innebär att tabellen inte bevaras.</span><span class="sxs-lookup"><span data-stu-id="0452f-152">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="0452f-153">Standardvärdet är noll.</span><span class="sxs-lookup"><span data-stu-id="0452f-153">The default value is zero.</span></span>
<span data-ttu-id="0452f-154">Om du anger ett värde som är större än noll måste du ange ett värde för parametern *TableIdentifer* .</span><span class="sxs-lookup"><span data-stu-id="0452f-154">If you specify a value greater than zero, you must specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="0452f-155">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0452f-155">-ServerName</span></span>
<span data-ttu-id="0452f-156">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="0452f-156">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="0452f-157">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0452f-157">-StorageAccountName</span></span>
<span data-ttu-id="0452f-158">Anger namnet på lagrings kontot för granskning av databasen.</span><span class="sxs-lookup"><span data-stu-id="0452f-158">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="0452f-159">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="0452f-159">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="0452f-160">Denna parameter är inte obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="0452f-160">This parameter is not required.</span></span>
<span data-ttu-id="0452f-161">Om du inte anger den här parametern använder cmdleten det lagrings konto som har definierats tidigare som en del av gransknings principen för databasen.</span><span class="sxs-lookup"><span data-stu-id="0452f-161">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="0452f-162">Om det är första gången en databas gransknings princip definieras och du inte anger den här parametern Miss lyckas cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0452f-162">If this is the first time a database auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="0452f-163">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="0452f-163">-StorageKeyType</span></span>
<span data-ttu-id="0452f-164">Anger vilken av lagrings åtkomst nycklar som ska användas.</span><span class="sxs-lookup"><span data-stu-id="0452f-164">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="0452f-165">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0452f-165">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0452f-166">Första</span><span class="sxs-lookup"><span data-stu-id="0452f-166">Primary</span></span>
- <span data-ttu-id="0452f-167">Sekundär standardvärdet är primärt.</span><span class="sxs-lookup"><span data-stu-id="0452f-167">Secondary The default value is Primary.</span></span>

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

### <span data-ttu-id="0452f-168">-TableIdentifier</span><span class="sxs-lookup"><span data-stu-id="0452f-168">-TableIdentifier</span></span>
<span data-ttu-id="0452f-169">Anger namnet på tabellen gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="0452f-169">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="0452f-170">Ange det här värdet om du anger ett värde som är större än noll för parametern *RetentionInDays* .</span><span class="sxs-lookup"><span data-stu-id="0452f-170">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="0452f-171">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0452f-171">-Confirm</span></span>
<span data-ttu-id="0452f-172">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0452f-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0452f-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0452f-173">-WhatIf</span></span>
<span data-ttu-id="0452f-174">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0452f-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0452f-175">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0452f-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0452f-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0452f-176">CommonParameters</span></span>
<span data-ttu-id="0452f-177">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0452f-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0452f-178">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0452f-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0452f-179">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0452f-179">INPUTS</span></span>

### <span data-ttu-id="0452f-180">Microsoft. Azure. commands. SQL. granskning. Model. AuditType</span><span class="sxs-lookup"><span data-stu-id="0452f-180">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditType</span></span>

### <span data-ttu-id="0452f-181">Microsoft. Azure. commands. SQL. granskning. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="0452f-181">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="0452f-182">System. string []</span><span class="sxs-lookup"><span data-stu-id="0452f-182">System.String[]</span></span>

### <span data-ttu-id="0452f-183">System. String</span><span class="sxs-lookup"><span data-stu-id="0452f-183">System.String</span></span>

### <span data-ttu-id="0452f-184">System. Nullable ' 1 [[system. UInt32, mscorlib, version = 4.0.0.0; Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0452f-184">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="0452f-185">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0452f-185">OUTPUTS</span></span>

### <span data-ttu-id="0452f-186">Microsoft. Azure. commands. SQL. granskning. Model. AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="0452f-186">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="0452f-187">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0452f-187">NOTES</span></span>

## <span data-ttu-id="0452f-188">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0452f-188">RELATED LINKS</span></span>

[<span data-ttu-id="0452f-189">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="0452f-189">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="0452f-190">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="0452f-190">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="0452f-191">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="0452f-191">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


