---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4FCC7D8B-A46E-4E5B-8BE2-F62B3D3E715D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: dd3c54b8e2769e1b7643d154b259b4f47fd51f2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755671"
---
# <span data-ttu-id="d096b-101">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d096b-101">Set-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="d096b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d096b-102">SYNOPSIS</span></span>
<span data-ttu-id="d096b-103">Ändrar gransknings principen för en SQL-databasserver.</span><span class="sxs-lookup"><span data-stu-id="d096b-103">Changes the auditing policy of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d096b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d096b-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditingPolicy [-AuditType <AuditType>] [-AuditActionGroup <AuditActionGroups[]>]
 [-PassThru] [-EventType <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-TableIdentifier <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d096b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d096b-105">DESCRIPTION</span></span>
<span data-ttu-id="d096b-106">Cmdleten **set-AzureRmSqlServerAuditingPolicy** ändrar gransknings principen för en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="d096b-106">The **Set-AzureRmSqlServerAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL Database server.</span></span>
<span data-ttu-id="d096b-107">Ange parametrarna *ResourceGroupName* och *servername* för att identifiera servern, parametern *StorageAccountName* för att ange lagrings konto för gransknings loggarna och parametern *StorageKeyType* för att definiera vilka lagrings nycklar som ska användas.</span><span class="sxs-lookup"><span data-stu-id="d096b-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server, the *StorageAccountName* parameter to specify the storage account for the audit logs, and the *StorageKeyType* parameter to define the storage keys to use.</span></span>
<span data-ttu-id="d096b-108">Du kan också definiera bevarande för tabellen gransknings loggar genom att ange värdet för parametrarna *RetentionInDays* och *TableIdentifier* för att definiera perioden och dirigeringen för tabell namnen för gransknings loggen.</span><span class="sxs-lookup"><span data-stu-id="d096b-108">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="d096b-109">Ange parametern *EventType* för att definiera vilka händelse typer som ska granskas.</span><span class="sxs-lookup"><span data-stu-id="d096b-109">Specify the *EventType* parameter to define which event types to audit.</span></span>
<span data-ttu-id="d096b-110">När du har kört denna cmdlet aktive ras granskning av databaserna som använder princip för den här servern.</span><span class="sxs-lookup"><span data-stu-id="d096b-110">After you run this cmdlet, auditing of the databases that use the policy of this server is enabled.</span></span>
<span data-ttu-id="d096b-111">Om cmdleten lyckas och du anger parametern *Passthru* returnerar cmdleten ett objekt som beskriver den aktuella gransknings principen och Server-ID: n.</span><span class="sxs-lookup"><span data-stu-id="d096b-111">If the cmdlet succeeds and you specify the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy, and the server identifiers.</span></span>
<span data-ttu-id="d096b-112">Server-ID: n är **ResourceGroupName** och **servername**.</span><span class="sxs-lookup"><span data-stu-id="d096b-112">Server identifiers include **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="d096b-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d096b-113">EXAMPLES</span></span>

### <span data-ttu-id="d096b-114">Exempel 1: Ange gransknings principen för en Azure SQL Server med tabell granskning</span><span class="sxs-lookup"><span data-stu-id="d096b-114">Example 1: Set the auditing policy of an Azure SQL server use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Table -StorageAccountName "Storage22"
```

<span data-ttu-id="d096b-115">Det här kommandot anger gransknings principen för servern som heter Server01 för att använda ett lagrings konto med namnet Storage22.</span><span class="sxs-lookup"><span data-stu-id="d096b-115">This command sets the auditing policy of the server named Server01 to use a storage account named Storage22.</span></span>

### <span data-ttu-id="d096b-116">Exempel 2: Ange lagrings kontots nycklar för en befintlig gransknings princip för en Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="d096b-116">Example 2: Set the storage account key of an existing auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountKey Secondary
```

<span data-ttu-id="d096b-117">Det här kommandot anger gransknings principen för servern som heter Server01 för att använda den sekundära knappen.</span><span class="sxs-lookup"><span data-stu-id="d096b-117">This command sets the auditing policy of the server named Server01 to use the secondary key.</span></span>
<span data-ttu-id="d096b-118">Kommandot ändrar inte namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="d096b-118">The command does not modify the storage account name.</span></span>

### <span data-ttu-id="d096b-119">Exempel 3: Konfigurera gransknings principen för en Azure SQL Server att använda en viss händelse typ</span><span class="sxs-lookup"><span data-stu-id="d096b-119">Example 3: Set the auditing policy of an Azure SQL server to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventType Login_Failure
```

### <span data-ttu-id="d096b-120">Exempel 4: Ange gransknings principen för en databas för att använda BLOB-granskning</span><span class="sxs-lookup"><span data-stu-id="d096b-120">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -RetentionInDays 8
```

<span data-ttu-id="d096b-121">Det här kommandot anger gransknings principen för servern som heter Server01 för att använda händelse typen Login_Failure.</span><span class="sxs-lookup"><span data-stu-id="d096b-121">This command sets the auditing policy of the server named Server01 to use the Login_Failure event type.</span></span>
<span data-ttu-id="d096b-122">Det här kommandot ändrar inte någon annan inställning.</span><span class="sxs-lookup"><span data-stu-id="d096b-122">This command does not modify any other setting.</span></span>

## <span data-ttu-id="d096b-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d096b-123">PARAMETERS</span></span>

### <span data-ttu-id="d096b-124">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="d096b-124">-AuditActionGroup</span></span>
<span data-ttu-id="d096b-125">Ange en eller flera gransknings åtgärds grupper.</span><span class="sxs-lookup"><span data-stu-id="d096b-125">Specify one or more audit action groups.</span></span> <span data-ttu-id="d096b-126">Den här parametern kan endast användas för BLOB-granskning.</span><span class="sxs-lookup"><span data-stu-id="d096b-126">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="d096b-127">-AuditType</span><span class="sxs-lookup"><span data-stu-id="d096b-127">-AuditType</span></span>
<span data-ttu-id="d096b-128">Ange gransknings typen.</span><span class="sxs-lookup"><span data-stu-id="d096b-128">Specify the audit type.</span></span> <span data-ttu-id="d096b-129">Gransknings loggar kan skrivas till register lagring eller Blob-lagring.</span><span class="sxs-lookup"><span data-stu-id="d096b-129">Audit logs can be written to Table storage or Blob storage.</span></span> <span data-ttu-id="d096b-130">BLOB-granskning ger högre prestanda och stöder granskning på objekt nivå.</span><span class="sxs-lookup"><span data-stu-id="d096b-130">Blob auditing provides higher performance and supports object-level auditing.</span></span>

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

### <span data-ttu-id="d096b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d096b-131">-DefaultProfile</span></span>
<span data-ttu-id="d096b-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d096b-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d096b-133">-EventType</span><span class="sxs-lookup"><span data-stu-id="d096b-133">-EventType</span></span>
<span data-ttu-id="d096b-134">Anger vilka händelse typer som ska granskas.</span><span class="sxs-lookup"><span data-stu-id="d096b-134">Specifies the event types to audit.</span></span>
<span data-ttu-id="d096b-135">Den här parametern gäller endast för tabell granskning.</span><span class="sxs-lookup"><span data-stu-id="d096b-135">This parameter is only applicable to Table auditing.</span></span>
<span data-ttu-id="d096b-136">Du kan ange flera händelse typer.</span><span class="sxs-lookup"><span data-stu-id="d096b-136">You can specify several event types.</span></span>
<span data-ttu-id="d096b-137">Du kan ange alla om du vill granska alla händelse typer eller inget för att ange att inga händelser ska granskas.</span><span class="sxs-lookup"><span data-stu-id="d096b-137">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="d096b-138">Om du anger alla eller ingen samtidigt visas kommandot.</span><span class="sxs-lookup"><span data-stu-id="d096b-138">If you specify All or None at the same time, the command fails.</span></span>

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

### <span data-ttu-id="d096b-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d096b-139">-PassThru</span></span>
<span data-ttu-id="d096b-140">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="d096b-140">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d096b-141">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="d096b-141">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d096b-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d096b-142">-ResourceGroupName</span></span>
<span data-ttu-id="d096b-143">Anger namnet på den resurs grupp som innehåller databasen.</span><span class="sxs-lookup"><span data-stu-id="d096b-143">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="d096b-144">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d096b-144">-RetentionInDays</span></span>
<span data-ttu-id="d096b-145">Anger antalet bevarande dagar för tabellen gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="d096b-145">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="d096b-146">Värdet noll (0) innebär att tabellen inte bevaras.</span><span class="sxs-lookup"><span data-stu-id="d096b-146">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="d096b-147">Det här är standardinställningen.</span><span class="sxs-lookup"><span data-stu-id="d096b-147">this is the default.</span></span>
<span data-ttu-id="d096b-148">Om du anger ett värde som är större än noll måste du också ange ett värde för parametern *TableIdentifer* .</span><span class="sxs-lookup"><span data-stu-id="d096b-148">If you specify a value greater than zero, you must also specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="d096b-149">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d096b-149">-ServerName</span></span>
<span data-ttu-id="d096b-150">Anger namnet på den server som innehåller databasen.</span><span class="sxs-lookup"><span data-stu-id="d096b-150">Specifies the name of the server that contains the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d096b-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d096b-151">-StorageAccountName</span></span>
<span data-ttu-id="d096b-152">Anger namnet på lagrings kontot för granskning av databasen.</span><span class="sxs-lookup"><span data-stu-id="d096b-152">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="d096b-153">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="d096b-153">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="d096b-154">Om du inte anger den här parametern använder cmdleten det lagrings konto som har definierats tidigare som en del av gransknings principen för databasen.</span><span class="sxs-lookup"><span data-stu-id="d096b-154">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="d096b-155">Om det är första gången en databas gransknings princip definieras och du inte anger den här parametern Miss lyckas kommandot.</span><span class="sxs-lookup"><span data-stu-id="d096b-155">If this is the first time a database auditing policy is defined and you do not specify this parameter, the command fails.</span></span>

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

### <span data-ttu-id="d096b-156">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="d096b-156">-StorageKeyType</span></span>
<span data-ttu-id="d096b-157">Anger vilken av lagrings åtkomst nycklar som ska användas.</span><span class="sxs-lookup"><span data-stu-id="d096b-157">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="d096b-158">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d096b-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d096b-159">Första</span><span class="sxs-lookup"><span data-stu-id="d096b-159">Primary</span></span>
- <span data-ttu-id="d096b-160">Sekundär standardvärdet är primärt.</span><span class="sxs-lookup"><span data-stu-id="d096b-160">Secondary The default value is Primary.</span></span>

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

### <span data-ttu-id="d096b-161">-TableIdentifier</span><span class="sxs-lookup"><span data-stu-id="d096b-161">-TableIdentifier</span></span>
<span data-ttu-id="d096b-162">Anger namnet på tabellen gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="d096b-162">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="d096b-163">Ange det här värdet om du anger ett värde som är större än noll för parametern *RetentionInDays* .</span><span class="sxs-lookup"><span data-stu-id="d096b-163">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="d096b-164">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d096b-164">-Confirm</span></span>
<span data-ttu-id="d096b-165">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d096b-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d096b-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d096b-166">-WhatIf</span></span>
<span data-ttu-id="d096b-167">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d096b-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d096b-168">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d096b-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d096b-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d096b-169">CommonParameters</span></span>
<span data-ttu-id="d096b-170">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d096b-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d096b-171">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d096b-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d096b-172">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d096b-172">INPUTS</span></span>

### <span data-ttu-id="d096b-173">Microsoft. Azure. commands. SQL. granskning. Model. AuditType</span><span class="sxs-lookup"><span data-stu-id="d096b-173">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditType</span></span>

### <span data-ttu-id="d096b-174">Microsoft. Azure. commands. SQL. granskning. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="d096b-174">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="d096b-175">System. string []</span><span class="sxs-lookup"><span data-stu-id="d096b-175">System.String[]</span></span>

### <span data-ttu-id="d096b-176">System. String</span><span class="sxs-lookup"><span data-stu-id="d096b-176">System.String</span></span>

### <span data-ttu-id="d096b-177">System. Nullable ' 1 [[system. UInt32, mscorlib, version = 4.0.0.0; Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d096b-177">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d096b-178">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d096b-178">OUTPUTS</span></span>

### <span data-ttu-id="d096b-179">Microsoft. Azure. commands. SQL. granskning. Model. AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d096b-179">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="d096b-180">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d096b-180">NOTES</span></span>

## <span data-ttu-id="d096b-181">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d096b-181">RELATED LINKS</span></span>

[<span data-ttu-id="d096b-182">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d096b-182">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="d096b-183">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d096b-183">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="d096b-184">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="d096b-184">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


