---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 2a81030cdf985ae338692e59d86da30cee50694f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576389"
---
# <span data-ttu-id="29c21-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="29c21-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="29c21-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29c21-102">SYNOPSIS</span></span>
<span data-ttu-id="29c21-103">Ändrar gransknings inställningarna för en Azure SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="29c21-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29c21-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29c21-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29c21-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29c21-105">DESCRIPTION</span></span>
<span data-ttu-id="29c21-106">Cmdleten **set-AzureRmSqlServerAuditing** ändrar gransknings inställningarna för en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="29c21-106">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="29c21-107">Använd cmdleten *ResourceGroupName* och *servername* för att identifiera servern.</span><span class="sxs-lookup"><span data-stu-id="29c21-107">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="29c21-108">Ange *StorageAccountName* -parametern för att ange lagrings konto för gransknings loggar och parametern *StorageKeyType* för att definiera lagrings nycklarna.</span><span class="sxs-lookup"><span data-stu-id="29c21-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="29c21-109">Använd parametern *State* för att aktivera/inaktivera principen.</span><span class="sxs-lookup"><span data-stu-id="29c21-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="29c21-110">Du kan också definiera bevarande för gransknings loggar genom att ange värdet för *RetentionInDays* -parametern för att definiera perioden för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="29c21-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="29c21-111">När cmdleten har körts klart är granskning av de Azure SQL-databaser som är definierade i den angivna Azure SQL-servern aktive rad.</span><span class="sxs-lookup"><span data-stu-id="29c21-111">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="29c21-112">Om cmdleten lyckas och du använder parametern *Passthru* returneras ett objekt som beskriver den aktuella BLOB-granskningen utöver Server-ID: n.</span><span class="sxs-lookup"><span data-stu-id="29c21-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="29c21-113">Server-ID: n inkluderar, men är inte begränsade till, **ResourceGroupName** och **servername**.</span><span class="sxs-lookup"><span data-stu-id="29c21-113">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="29c21-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29c21-114">EXAMPLES</span></span>

### <span data-ttu-id="29c21-115">Exempel 1: Aktivera gransknings principen för en Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="29c21-115">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="29c21-116">Exempel 2: inaktivera gransknings principen för en Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="29c21-116">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

## <span data-ttu-id="29c21-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29c21-117">PARAMETERS</span></span>

### <span data-ttu-id="29c21-118">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="29c21-118">-AuditActionGroup</span></span>
<span data-ttu-id="29c21-119">Den rekommenderade uppsättningen åtgärds grupper som ska användas är följande kombination – detta granskar alla frågor och lagrade procedurer som körs mot databasen samt lyckade och misslyckade inloggningar:</span><span class="sxs-lookup"><span data-stu-id="29c21-119">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="29c21-120">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="29c21-120">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="29c21-121">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="29c21-121">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="29c21-122">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="29c21-122">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  

<span data-ttu-id="29c21-123">Ovanstående kombination är även den uppsättning som är konfigurerad som standard.</span><span class="sxs-lookup"><span data-stu-id="29c21-123">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="29c21-124">Dessa grupper täcker alla SQL-uttryck och lagrade procedurer som körs mot databasen och ska inte användas i kombination med andra grupper eftersom detta kommer att leda till dubbletter av gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="29c21-124">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="29c21-125">Mer information finns i https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="29c21-125">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="29c21-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29c21-126">-DefaultProfile</span></span>
<span data-ttu-id="29c21-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="29c21-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29c21-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29c21-128">-PassThru</span></span>
<span data-ttu-id="29c21-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="29c21-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="29c21-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29c21-130">-ResourceGroupName</span></span>
<span data-ttu-id="29c21-131">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="29c21-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="29c21-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="29c21-132">-RetentionInDays</span></span>
<span data-ttu-id="29c21-133">Antalet bevarande dagar för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="29c21-133">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="29c21-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="29c21-134">-ServerName</span></span>
<span data-ttu-id="29c21-135">SQL Server-namn.</span><span class="sxs-lookup"><span data-stu-id="29c21-135">SQL server name.</span></span>

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

### <span data-ttu-id="29c21-136">-State</span><span class="sxs-lookup"><span data-stu-id="29c21-136">-State</span></span>
<span data-ttu-id="29c21-137">Tillståndet för policyn.</span><span class="sxs-lookup"><span data-stu-id="29c21-137">The state of the policy.</span></span>

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

### <span data-ttu-id="29c21-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="29c21-138">-StorageAccountName</span></span>
<span data-ttu-id="29c21-139">Namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="29c21-139">The name of the storage account.</span></span> <span data-ttu-id="29c21-140">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="29c21-140">Wildcard characters are not permitted.</span></span>  
<span data-ttu-id="29c21-141">Denna parameter är inte obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="29c21-141">This parameter is not required.</span></span>  
<span data-ttu-id="29c21-142">Om du inte anger den här parametern använder cmdleten det lagrings konto som har definierats tidigare som en del av gransknings principen.</span><span class="sxs-lookup"><span data-stu-id="29c21-142">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>  
<span data-ttu-id="29c21-143">Om det är första gången en gransknings princip definieras och du inte anger den här parametern Miss lyckas cmdleten.</span><span class="sxs-lookup"><span data-stu-id="29c21-143">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="29c21-144">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="29c21-144">-StorageKeyType</span></span>
<span data-ttu-id="29c21-145">Anger vilken av lagrings åtkomst nycklar som ska användas.</span><span class="sxs-lookup"><span data-stu-id="29c21-145">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="29c21-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="29c21-146">-Confirm</span></span>
<span data-ttu-id="29c21-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="29c21-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29c21-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29c21-148">-WhatIf</span></span>
<span data-ttu-id="29c21-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="29c21-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29c21-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="29c21-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29c21-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29c21-151">CommonParameters</span></span>
<span data-ttu-id="29c21-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29c21-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29c21-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29c21-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29c21-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29c21-154">INPUTS</span></span>

### <span data-ttu-id="29c21-155">Ingen</span><span class="sxs-lookup"><span data-stu-id="29c21-155">None</span></span>
<span data-ttu-id="29c21-156">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="29c21-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="29c21-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29c21-157">OUTPUTS</span></span>

### <span data-ttu-id="29c21-158">Microsoft. Azure. commands. SQL. Security. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="29c21-158">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="29c21-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29c21-159">NOTES</span></span>

## <span data-ttu-id="29c21-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29c21-160">RELATED LINKS</span></span>
