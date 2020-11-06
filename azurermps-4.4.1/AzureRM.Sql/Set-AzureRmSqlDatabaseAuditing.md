---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: a6d09b573225efa5f8467e9ca02edb65a87ebe10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576682"
---
# <span data-ttu-id="9b4e0-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="9b4e0-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="9b4e0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b4e0-102">SYNOPSIS</span></span>
<span data-ttu-id="9b4e0-103">Ändrar gransknings inställningarna för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="9b4e0-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b4e0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b4e0-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b4e0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b4e0-105">DESCRIPTION</span></span>
<span data-ttu-id="9b4e0-106">Cmdleten **set-AzureRmSqlDatabaseAuditing** ändrar gransknings inställningarna för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="9b4e0-106">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="9b4e0-107">Använd cmdleten *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="9b4e0-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="9b4e0-108">Ange *StorageAccountName* -parametern för att ange lagrings konto för gransknings loggar och parametern *StorageKeyType* för att definiera lagrings nycklarna.</span><span class="sxs-lookup"><span data-stu-id="9b4e0-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="9b4e0-109">Använd parametern *State* för att aktivera/inaktivera principen.</span><span class="sxs-lookup"><span data-stu-id="9b4e0-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="9b4e0-110">Du kan också definiera bevarande för gransknings loggar genom att ange värdet för *RetentionInDays* -parametern för att definiera perioden för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="9b4e0-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="9b4e0-111">När cmdleten körs är den aktive rad.</span><span class="sxs-lookup"><span data-stu-id="9b4e0-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="9b4e0-112">Om cmdleten lyckas och du använder parametern *Passthru* returneras ett objekt som beskriver den aktuella BLOB-granskningen utöver databas identifierarna.</span><span class="sxs-lookup"><span data-stu-id="9b4e0-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="9b4e0-113">Databas identifierare inkluderar, men är inte begränsade till, **ResourceGroupName** , **servername** och **databasename**.</span><span class="sxs-lookup"><span data-stu-id="9b4e0-113">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="9b4e0-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b4e0-114">EXAMPLES</span></span>

### <span data-ttu-id="9b4e0-115">Exempel 1: Aktivera gransknings principen för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="9b4e0-115">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="9b4e0-116">Exempel 2: inaktivera en BLOB-gransknings princip för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="9b4e0-116">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

## <span data-ttu-id="9b4e0-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b4e0-117">PARAMETERS</span></span>

### <span data-ttu-id="9b4e0-118">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="9b4e0-118">-AuditAction</span></span>
<span data-ttu-id="9b4e0-119">Uppsättningen gransknings åtgärder</span><span class="sxs-lookup"><span data-stu-id="9b4e0-119">The set of the audit actions</span></span>

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

### <span data-ttu-id="9b4e0-120">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="9b4e0-120">-AuditActionGroup</span></span>
<span data-ttu-id="9b4e0-121">Uppsättningen gransknings åtgärds grupper</span><span class="sxs-lookup"><span data-stu-id="9b4e0-121">The set of the audit action groups</span></span>

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

### <span data-ttu-id="9b4e0-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9b4e0-122">-DatabaseName</span></span>
<span data-ttu-id="9b4e0-123">Namn på SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="9b4e0-123">SQL Database name.</span></span>

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

### <span data-ttu-id="9b4e0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b4e0-124">-PassThru</span></span>
<span data-ttu-id="9b4e0-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9b4e0-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9b4e0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b4e0-126">-ResourceGroupName</span></span>
<span data-ttu-id="9b4e0-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9b4e0-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="9b4e0-128">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="9b4e0-128">-RetentionInDays</span></span>
<span data-ttu-id="9b4e0-129">Antalet bevarande dagar för gransknings loggar</span><span class="sxs-lookup"><span data-stu-id="9b4e0-129">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="9b4e0-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9b4e0-130">-ServerName</span></span>
<span data-ttu-id="9b4e0-131">Server namn för SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="9b4e0-131">SQL Database server name.</span></span>

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

### <span data-ttu-id="9b4e0-132">-State</span><span class="sxs-lookup"><span data-stu-id="9b4e0-132">-State</span></span>
<span data-ttu-id="9b4e0-133">Tillståndet för gransknings policyn</span><span class="sxs-lookup"><span data-stu-id="9b4e0-133">The state of the auditing policy</span></span>

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

### <span data-ttu-id="9b4e0-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9b4e0-134">-StorageAccountName</span></span>
<span data-ttu-id="9b4e0-135">Namnet på lagrings kontot</span><span class="sxs-lookup"><span data-stu-id="9b4e0-135">The name of the storage account</span></span>

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

### <span data-ttu-id="9b4e0-136">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="9b4e0-136">-StorageKeyType</span></span>
<span data-ttu-id="9b4e0-137">Typ av lagrings plats</span><span class="sxs-lookup"><span data-stu-id="9b4e0-137">The type of the storage key</span></span>

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

### <span data-ttu-id="9b4e0-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9b4e0-138">-Confirm</span></span>
<span data-ttu-id="9b4e0-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9b4e0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b4e0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b4e0-140">-WhatIf</span></span>
<span data-ttu-id="9b4e0-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9b4e0-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b4e0-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9b4e0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b4e0-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b4e0-143">-DefaultProfile</span></span>
<span data-ttu-id="9b4e0-144">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9b4e0-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b4e0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b4e0-145">CommonParameters</span></span>
<span data-ttu-id="9b4e0-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b4e0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b4e0-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b4e0-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b4e0-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b4e0-148">INPUTS</span></span>

## <span data-ttu-id="9b4e0-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b4e0-149">OUTPUTS</span></span>

### <span data-ttu-id="9b4e0-150">Microsoft. Azure. commands. SQL. Security. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="9b4e0-150">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="9b4e0-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b4e0-151">NOTES</span></span>

## <span data-ttu-id="9b4e0-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b4e0-152">RELATED LINKS</span></span>

