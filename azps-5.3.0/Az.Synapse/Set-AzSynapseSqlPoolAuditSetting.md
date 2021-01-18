---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 91691741fd7b26d8f33880dee252501c626a4bc6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523909"
---
# <span data-ttu-id="a16be-101">Set-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="a16be-101">Set-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="a16be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a16be-102">SYNOPSIS</span></span>
<span data-ttu-id="a16be-103">Ändrar gransknings inställningarna för en Azure Synapse-BA SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="a16be-103">Changes the auditing settings for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a16be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a16be-104">SYNTAX</span></span>

### <span data-ttu-id="a16be-105">SetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a16be-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a16be-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a16be-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a16be-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a16be-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a16be-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a16be-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a16be-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a16be-109">DESCRIPTION</span></span>
<span data-ttu-id="a16be-110">Cmdleten **set-AzSynapseSqlPoolAuditSetting** ändrar gransknings inställningarna för en Azure SYNAPSE Analytics SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="a16be-110">The **Set-AzSynapseSqlPoolAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="a16be-111">När Blob Storage är ett mål för gransknings loggar anger du parametern *StorageAccountResourceId* för att bestämma lagrings konto för gransknings loggar och parametern *StorageKeyType* för att definiera lagrings nycklarna.</span><span class="sxs-lookup"><span data-stu-id="a16be-111">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="a16be-112">Du kan också definiera bevarande för gransknings loggar genom att ange värdet för *RetentionInDays* -parametern för att definiera perioden för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="a16be-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="a16be-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a16be-113">EXAMPLES</span></span>

### <span data-ttu-id="a16be-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a16be-114">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="a16be-115">Aktivera gransknings principen för blob-lagring för en Azure Synapse Analytics SQL-pool med namnet ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="a16be-115">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="a16be-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a16be-116">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Disabled
```

<span data-ttu-id="a16be-117">Inaktivera gransknings principen för blob-lagring för en Azure Synapse Analytics SQL-pool med namnet ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="a16be-117">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="a16be-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="a16be-118">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="a16be-119">Aktivera gransknings principen för blob-lagring för en Azure Synapse Analytics SQL-pool med namnet ContosoSqlPool med avancerad filtrering med ett T-SQL-predikat.</span><span class="sxs-lookup"><span data-stu-id="a16be-119">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="a16be-120">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="a16be-120">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PredicateExpression ""
```

<span data-ttu-id="a16be-121">Ta bort inställningen Advanced filter from gransknings principen för en Azure Synapse Analytics SQL-pool med namnet ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="a16be-121">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="a16be-122">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="a16be-122">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="a16be-123">Inaktivera gransknings principen för blob-lagring för en Azure Synapse Analytics SQL-pool med namnet ContosoSqlPool via pipeline.</span><span class="sxs-lookup"><span data-stu-id="a16be-123">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool through pipeline.</span></span>

## <span data-ttu-id="a16be-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a16be-124">PARAMETERS</span></span>

### <span data-ttu-id="a16be-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a16be-125">-AsJob</span></span>
<span data-ttu-id="a16be-126">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a16be-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a16be-127">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="a16be-127">-AuditAction</span></span>
<span data-ttu-id="a16be-128">Uppsättningen gransknings åtgärder.</span><span class="sxs-lookup"><span data-stu-id="a16be-128">The set of audit actions.</span></span>

<span data-ttu-id="a16be-129">De åtgärder som stöds för granskning är:</span><span class="sxs-lookup"><span data-stu-id="a16be-129">The supported actions to audit are:</span></span>

<span data-ttu-id="a16be-130">ANVÄNDA</span><span class="sxs-lookup"><span data-stu-id="a16be-130">SELECT</span></span>

<span data-ttu-id="a16be-131">UPPDATERA</span><span class="sxs-lookup"><span data-stu-id="a16be-131">UPDATE</span></span>

<span data-ttu-id="a16be-132">Placera</span><span class="sxs-lookup"><span data-stu-id="a16be-132">INSERT</span></span>

<span data-ttu-id="a16be-133">TA bort</span><span class="sxs-lookup"><span data-stu-id="a16be-133">DELETE</span></span>

<span data-ttu-id="a16be-134">GENOMFÖR</span><span class="sxs-lookup"><span data-stu-id="a16be-134">EXECUTE</span></span>

<span data-ttu-id="a16be-135">MOTTAR</span><span class="sxs-lookup"><span data-stu-id="a16be-135">RECEIVE</span></span>

<span data-ttu-id="a16be-136">INNEHÅLLER</span><span class="sxs-lookup"><span data-stu-id="a16be-136">REFERENCES</span></span>

<span data-ttu-id="a16be-137">Det allmänna formuläret för att definiera en åtgärd som ska granskas är:</span><span class="sxs-lookup"><span data-stu-id="a16be-137">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="a16be-138">\[åtgärd \] för \[ objekt \] efter \[ huvud konto\]</span><span class="sxs-lookup"><span data-stu-id="a16be-138">\[action\] ON \[object\] BY \[principal\]</span></span>

<span data-ttu-id="a16be-139">Observera att \[ objektet \] i ovanstående format kan referera till ett objekt, till exempel en tabell, en vy eller en lagrad procedur eller en hel databas eller ett helt schema.</span><span class="sxs-lookup"><span data-stu-id="a16be-139">Note that \[object\] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span>
<span data-ttu-id="a16be-140">För de sistnämnda fallen är formulär databasen:: \[ dbname \] och schema:: \[ SchemaName \] används.</span><span class="sxs-lookup"><span data-stu-id="a16be-140">For the latter cases, the forms DATABASE::\[dbname\] and SCHEMA::\[schemaname\] are used, respectively.</span></span>

<span data-ttu-id="a16be-141">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="a16be-141">For example:</span></span>

<span data-ttu-id="a16be-142">Välj i dbo. nontable av offentlig</span><span class="sxs-lookup"><span data-stu-id="a16be-142">SELECT on dbo.myTable by public</span></span>

<span data-ttu-id="a16be-143">Välj på databas:: min databas av offentlig</span><span class="sxs-lookup"><span data-stu-id="a16be-143">SELECT on DATABASE::myDatabase by public</span></span>

<span data-ttu-id="a16be-144">Välj på SCHEMA:: mina schema av offentlig</span><span class="sxs-lookup"><span data-stu-id="a16be-144">SELECT on SCHEMA::mySchema by public</span></span>

<span data-ttu-id="a16be-145">Mer information finns i https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="a16be-145">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16be-146">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="a16be-146">-AuditActionGroup</span></span>
<span data-ttu-id="a16be-147">Den rekommenderade uppsättningen åtgärds grupper som ska användas är följande kombination – detta granskar alla frågor och lagrade procedurer som körs mot databasen samt lyckade och misslyckade inloggningar:</span><span class="sxs-lookup"><span data-stu-id="a16be-147">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="a16be-148">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="a16be-148">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="a16be-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="a16be-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="a16be-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="a16be-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="a16be-151">Ovanstående kombination är även den uppsättning som är konfigurerad som standard.</span><span class="sxs-lookup"><span data-stu-id="a16be-151">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="a16be-152">Dessa grupper täcker alla SQL-uttryck och lagrade procedurer som körs mot databasen och ska inte användas i kombination med andra grupper eftersom detta kommer att leda till dubbletter av gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="a16be-152">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="a16be-153">Mer information finns i https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="a16be-153">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.AuditActionGroup[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16be-154">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="a16be-154">-BlobStorageTargetState</span></span>
<span data-ttu-id="a16be-155">Anger om Blob Storage är en destination för gransknings poster.</span><span class="sxs-lookup"><span data-stu-id="a16be-155">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="a16be-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a16be-156">-DefaultProfile</span></span>
<span data-ttu-id="a16be-157">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a16be-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a16be-158">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a16be-158">-InputObject</span></span>
<span data-ttu-id="a16be-159">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="a16be-159">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a16be-160">-Namn</span><span class="sxs-lookup"><span data-stu-id="a16be-160">-Name</span></span>
<span data-ttu-id="a16be-161">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="a16be-161">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16be-162">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a16be-162">-PassThru</span></span>
<span data-ttu-id="a16be-163">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="a16be-163">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a16be-164">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="a16be-164">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a16be-165">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="a16be-165">-PredicateExpression</span></span>
<span data-ttu-id="a16be-166">Uttrycket T-SQL predikat (WHERE-satsen) som används för att filtrera gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="a16be-166">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="a16be-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a16be-167">-ResourceGroupName</span></span>
<span data-ttu-id="a16be-168">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="a16be-168">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16be-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a16be-169">-ResourceId</span></span>
<span data-ttu-id="a16be-170">Resurs-ID för Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="a16be-170">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16be-171">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="a16be-171">-RetentionInDays</span></span>
<span data-ttu-id="a16be-172">Antalet bevarande dagar för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="a16be-172">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="a16be-173">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="a16be-173">-StorageAccountResourceId</span></span>
<span data-ttu-id="a16be-174">Resurs-ID för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="a16be-174">The storage account resource id</span></span>

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

### <span data-ttu-id="a16be-175">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="a16be-175">-StorageKeyType</span></span>
<span data-ttu-id="a16be-176">Anger vilken av lagrings åtkomst nycklar som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a16be-176">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="a16be-177">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a16be-177">-WorkspaceName</span></span>
<span data-ttu-id="a16be-178">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="a16be-178">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16be-179">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a16be-179">-WorkspaceObject</span></span>
<span data-ttu-id="a16be-180">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="a16be-180">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a16be-181">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a16be-181">-Confirm</span></span>
<span data-ttu-id="a16be-182">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a16be-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a16be-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a16be-183">-WhatIf</span></span>
<span data-ttu-id="a16be-184">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a16be-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a16be-185">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a16be-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a16be-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a16be-186">CommonParameters</span></span>
<span data-ttu-id="a16be-187">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a16be-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a16be-188">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a16be-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a16be-189">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a16be-189">INPUTS</span></span>

### <span data-ttu-id="a16be-190">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a16be-190">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a16be-191">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a16be-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a16be-192">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a16be-192">OUTPUTS</span></span>

### <span data-ttu-id="a16be-193">Microsoft. Azure. commands. Synapse. Models. SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="a16be-193">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="a16be-194">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a16be-194">NOTES</span></span>

## <span data-ttu-id="a16be-195">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a16be-195">RELATED LINKS</span></span>
