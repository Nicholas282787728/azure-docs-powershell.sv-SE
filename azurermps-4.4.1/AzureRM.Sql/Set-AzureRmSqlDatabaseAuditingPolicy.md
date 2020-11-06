---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: 99fb9bf57f056a869310de2fe27d00a72ce5d8c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574476"
---
# <span data-ttu-id="27fc1-101">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="27fc1-101">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="27fc1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="27fc1-102">SYNOPSIS</span></span>
<span data-ttu-id="27fc1-103">Anger gransknings principen för en databas.</span><span class="sxs-lookup"><span data-stu-id="27fc1-103">Sets the auditing policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27fc1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="27fc1-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditingPolicy [-AuditType <AuditType>] [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-EventType <String[]>]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-TableIdentifier <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27fc1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="27fc1-105">DESCRIPTION</span></span>
<span data-ttu-id="27fc1-106">Cmdleten **set-AzureRmSqlDatabaseAuditingPolicy** ändrar gransknings principen för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="27fc1-106">The **Set-AzureRmSqlDatabaseAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL database.</span></span>
<span data-ttu-id="27fc1-107">Använd cmdleten *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="27fc1-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="27fc1-108">Ange *StorageAccountName* -parametern för att ange lagrings konto för gransknings loggar och parametern *StorageKeyType* för att definiera lagrings nycklarna.</span><span class="sxs-lookup"><span data-stu-id="27fc1-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>

<span data-ttu-id="27fc1-109">Du kan också definiera bevarande för tabellen gransknings loggar genom att ange värdet för parametrarna *RetentionInDays* och *TableIdentifier* för att definiera perioden och dirigeringen för tabell namnen för gransknings loggen.</span><span class="sxs-lookup"><span data-stu-id="27fc1-109">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="27fc1-110">Ange parametern *EventType* för att definiera vilka händelse typer som ska granskas.</span><span class="sxs-lookup"><span data-stu-id="27fc1-110">Specify the *EventType* parameter to define which event types to audit.</span></span>

<span data-ttu-id="27fc1-111">När cmdleten körs är den aktive rad.</span><span class="sxs-lookup"><span data-stu-id="27fc1-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="27fc1-112">Om databasen använde serverns princip för granskning innan du körde denna cmdlet slutar granskningen att använda den principen.</span><span class="sxs-lookup"><span data-stu-id="27fc1-112">If the database used the policy of its server for auditing before you ran this cmdlet, auditing stops using that policy.</span></span>
<span data-ttu-id="27fc1-113">Om cmdleten lyckas och du använder *Passthru* -parametern returneras ett objekt som avbeskriverr den aktuella gransknings principen utöver databasens identifierare.</span><span class="sxs-lookup"><span data-stu-id="27fc1-113">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="27fc1-114">Databas identifierare inkluderar, men är inte begränsade till, **ResourceGroupName** , **servername** och **databasename**.</span><span class="sxs-lookup"><span data-stu-id="27fc1-114">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="27fc1-115">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="27fc1-115">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="27fc1-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="27fc1-116">EXAMPLES</span></span>

### <span data-ttu-id="27fc1-117">Exempel 1: Ange gransknings principen för en databas för att använda tabell granskning</span><span class="sxs-lookup"><span data-stu-id="27fc1-117">Example 1: Set the auditing policy of a database to use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Table -StorageAccountName "Storage31"
```

<span data-ttu-id="27fc1-118">Det här kommandot anger den gransknings princip för databasen som heter Database01 på Server01 för att använda lagrings kontot som heter Storage31.</span><span class="sxs-lookup"><span data-stu-id="27fc1-118">This command sets the auditing policy of database named Database01 located on Server01 to use the storage account named Storage31.</span></span>

### <span data-ttu-id="27fc1-119">Exempel 2: Ange lagrings konto nycklar för en befintlig gransknings princip för en databas</span><span class="sxs-lookup"><span data-stu-id="27fc1-119">Example 2: Set the storage account key of an existing auditing policy of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -StorageAccountKey Secondary
```

<span data-ttu-id="27fc1-120">Det här kommandot anger den gransknings princip för databasen som heter Database01 på Server01 för att fortsätta använda samma lagrings konto namn men för att nu använda den sekundära knappen.</span><span class="sxs-lookup"><span data-stu-id="27fc1-120">This command sets the auditing policy of database named Database01 located on Server01 to keep using the same storage account name but to now use the secondary key.</span></span>

### <span data-ttu-id="27fc1-121">Exempel 3: Ange gransknings principen för en databas för att använda en viss händelse typ</span><span class="sxs-lookup"><span data-stu-id="27fc1-121">Example 3: Set the auditing policy of a database to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventType Login_Failure
```

### <span data-ttu-id="27fc1-122">Exempel 4: Ange gransknings principen för en databas för att använda BLOB-granskning</span><span class="sxs-lookup"><span data-stu-id="27fc1-122">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -AuditAction "UPDATE ON database::[Database01] BY [public]"  -RetentionInDays 8
```

<span data-ttu-id="27fc1-123">Det här kommandot anger gransknings principen för databasen som heter Database01 på Server01.</span><span class="sxs-lookup"><span data-stu-id="27fc1-123">This command sets the auditing policy of database named Database01 located on Server01.</span></span>
<span data-ttu-id="27fc1-124">Principen loggar händelse typen för Login_Failure.</span><span class="sxs-lookup"><span data-stu-id="27fc1-124">The policy logs the Login_Failure event type.</span></span>
<span data-ttu-id="27fc1-125">Kommandot ändrar inte lagrings inställningarna.</span><span class="sxs-lookup"><span data-stu-id="27fc1-125">The command does not change the storage settings.</span></span>

## <span data-ttu-id="27fc1-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="27fc1-126">PARAMETERS</span></span>

### <span data-ttu-id="27fc1-127">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="27fc1-127">-AuditAction</span></span>
<span data-ttu-id="27fc1-128">Ange en eller flera gransknings åtgärder.</span><span class="sxs-lookup"><span data-stu-id="27fc1-128">Specify one or more audit actions.</span></span>
<span data-ttu-id="27fc1-129">Den här parametern kan endast användas för BLOB-granskning.</span><span class="sxs-lookup"><span data-stu-id="27fc1-129">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="27fc1-130">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="27fc1-130">-AuditActionGroup</span></span>
<span data-ttu-id="27fc1-131">Ange en eller flera gransknings åtgärds grupper.</span><span class="sxs-lookup"><span data-stu-id="27fc1-131">Specify one or more audit action groups.</span></span>
<span data-ttu-id="27fc1-132">Den här parametern kan endast användas för BLOB-granskning.</span><span class="sxs-lookup"><span data-stu-id="27fc1-132">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="27fc1-133">-AuditType</span><span class="sxs-lookup"><span data-stu-id="27fc1-133">-AuditType</span></span>
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

### <span data-ttu-id="27fc1-134">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="27fc1-134">-DatabaseName</span></span>
<span data-ttu-id="27fc1-135">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="27fc1-135">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="27fc1-136">-EventType</span><span class="sxs-lookup"><span data-stu-id="27fc1-136">-EventType</span></span>
<span data-ttu-id="27fc1-137">Anger vilka händelse typer som ska granskas.</span><span class="sxs-lookup"><span data-stu-id="27fc1-137">Specifies the event types to audit.</span></span>
<span data-ttu-id="27fc1-138">Den här parametern gäller endast för tabell granskning.</span><span class="sxs-lookup"><span data-stu-id="27fc1-138">This parameter is only applicable to Table auditing.</span></span>

<span data-ttu-id="27fc1-139">Du kan ange flera händelse typer.</span><span class="sxs-lookup"><span data-stu-id="27fc1-139">You can specify several event types.</span></span>
<span data-ttu-id="27fc1-140">Du kan ange alla om du vill granska alla händelse typer eller inget för att ange att inga händelser ska granskas.</span><span class="sxs-lookup"><span data-stu-id="27fc1-140">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="27fc1-141">Om du anger alla eller ingen samtidigt körs cmdleten inte.</span><span class="sxs-lookup"><span data-stu-id="27fc1-141">If you specify All or None at the same time, the cmdlet does not run.</span></span>

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

### <span data-ttu-id="27fc1-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27fc1-142">-PassThru</span></span>
<span data-ttu-id="27fc1-143">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="27fc1-143">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="27fc1-144">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="27fc1-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="27fc1-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27fc1-145">-ResourceGroupName</span></span>
<span data-ttu-id="27fc1-146">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="27fc1-146">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="27fc1-147">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="27fc1-147">-RetentionInDays</span></span>
<span data-ttu-id="27fc1-148">Anger antalet bevarande dagar för tabellen gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="27fc1-148">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="27fc1-149">Värdet noll (0) innebär att tabellen inte bevaras.</span><span class="sxs-lookup"><span data-stu-id="27fc1-149">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="27fc1-150">Standardvärdet är noll.</span><span class="sxs-lookup"><span data-stu-id="27fc1-150">The default value is zero.</span></span>
<span data-ttu-id="27fc1-151">Om du anger ett värde som är större än noll måste du ange ett värde för parametern *TableIdentifer* .</span><span class="sxs-lookup"><span data-stu-id="27fc1-151">If you specify a value greater than zero, you must specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="27fc1-152">-ServerName</span><span class="sxs-lookup"><span data-stu-id="27fc1-152">-ServerName</span></span>
<span data-ttu-id="27fc1-153">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="27fc1-153">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="27fc1-154">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="27fc1-154">-StorageAccountName</span></span>
<span data-ttu-id="27fc1-155">Anger namnet på lagrings kontot för granskning av databasen.</span><span class="sxs-lookup"><span data-stu-id="27fc1-155">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="27fc1-156">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="27fc1-156">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="27fc1-157">Denna parameter är inte obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="27fc1-157">This parameter is not required.</span></span>
<span data-ttu-id="27fc1-158">Om du inte anger den här parametern använder cmdleten det lagrings konto som har definierats tidigare som en del av gransknings principen för databasen.</span><span class="sxs-lookup"><span data-stu-id="27fc1-158">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="27fc1-159">Om det är första gången en databas gransknings princip definieras och du inte anger den här parametern Miss lyckas cmdleten.</span><span class="sxs-lookup"><span data-stu-id="27fc1-159">If this is the first time a database auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="27fc1-160">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="27fc1-160">-StorageKeyType</span></span>
<span data-ttu-id="27fc1-161">Anger vilken av lagrings åtkomst nycklar som ska användas.</span><span class="sxs-lookup"><span data-stu-id="27fc1-161">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="27fc1-162">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="27fc1-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="27fc1-163">Första</span><span class="sxs-lookup"><span data-stu-id="27fc1-163">Primary</span></span>
- <span data-ttu-id="27fc1-164">Sekundär</span><span class="sxs-lookup"><span data-stu-id="27fc1-164">Secondary</span></span>

<span data-ttu-id="27fc1-165">Standardvärdet är primärt.</span><span class="sxs-lookup"><span data-stu-id="27fc1-165">The default value is Primary.</span></span>

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

### <span data-ttu-id="27fc1-166">-TableIdentifier</span><span class="sxs-lookup"><span data-stu-id="27fc1-166">-TableIdentifier</span></span>
<span data-ttu-id="27fc1-167">Anger namnet på tabellen gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="27fc1-167">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="27fc1-168">Ange det här värdet om du anger ett värde som är större än noll för parametern *RetentionInDays* .</span><span class="sxs-lookup"><span data-stu-id="27fc1-168">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="27fc1-169">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="27fc1-169">-Confirm</span></span>
<span data-ttu-id="27fc1-170">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="27fc1-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27fc1-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27fc1-171">-WhatIf</span></span>
<span data-ttu-id="27fc1-172">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="27fc1-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27fc1-173">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="27fc1-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27fc1-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27fc1-174">-DefaultProfile</span></span>
<span data-ttu-id="27fc1-175">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="27fc1-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27fc1-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27fc1-176">CommonParameters</span></span>
<span data-ttu-id="27fc1-177">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27fc1-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27fc1-178">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27fc1-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27fc1-179">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="27fc1-179">INPUTS</span></span>

## <span data-ttu-id="27fc1-180">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="27fc1-180">OUTPUTS</span></span>

### <span data-ttu-id="27fc1-181">Microsoft. Azure. commands. SQL. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="27fc1-181">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="27fc1-182">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="27fc1-182">NOTES</span></span>

## <span data-ttu-id="27fc1-183">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="27fc1-183">RELATED LINKS</span></span>

[<span data-ttu-id="27fc1-184">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="27fc1-184">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="27fc1-185">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="27fc1-185">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="27fc1-186">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="27fc1-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


