---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: ae09bb11b56bd6c5fa0add402ace850fe560b293
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424035"
---
# <span data-ttu-id="96c28-101">Set-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="96c28-101">Set-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="96c28-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96c28-102">SYNOPSIS</span></span>
<span data-ttu-id="96c28-103">Ändrar gransknings inställningarna för en Azure Synapse Analytics-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="96c28-103">Changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="96c28-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96c28-104">SYNTAX</span></span>

### <span data-ttu-id="96c28-105">SetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="96c28-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96c28-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96c28-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96c28-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="96c28-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96c28-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96c28-108">DESCRIPTION</span></span>
<span data-ttu-id="96c28-109">Cmdleten **set-AzSynapseSqlAuditSetting** ändrar gransknings inställningarna för en Azure Synapse Analytics-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="96c28-109">The **Set-AzSynapseSqlAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>
<span data-ttu-id="96c28-110">När Blob Storage är ett mål för gransknings loggar anger du parametern *StorageAccountResourceId* för att bestämma lagrings konto för gransknings loggar och parametern *StorageKeyType* för att definiera lagrings nycklarna.</span><span class="sxs-lookup"><span data-stu-id="96c28-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="96c28-111">Du kan också definiera bevarande för gransknings loggar genom att ange värdet för *RetentionInDays* -parametern för att definiera perioden för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="96c28-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="96c28-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96c28-112">EXAMPLES</span></span>

### <span data-ttu-id="96c28-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="96c28-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="96c28-114">Aktivera gransknings principen för blob-lagring för en Azure Synapse-arbetsyta med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="96c28-114">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="96c28-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="96c28-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Disabled
```

<span data-ttu-id="96c28-116">Inaktivera gransknings principen för blob-lagring för en Azure Synapse-arbetsyta med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="96c28-116">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="96c28-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="96c28-117">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="96c28-118">Aktivera gransknings principen för blob-lagring för en Azure Synapse-arbetsyta med namnet ContosoWorkspace med avancerad filtrering med ett T-SQL-predikat.</span><span class="sxs-lookup"><span data-stu-id="96c28-118">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="96c28-119">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="96c28-119">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -PredicateExpression ""
```

<span data-ttu-id="96c28-120">Ta bort inställningen Advanced filter from gransknings principen för en Azure Synapse Analytics-arbetsyta med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="96c28-120">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="96c28-121">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="96c28-121">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Set-AzSynapseSqlAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="96c28-122">Inaktivera gransknings principen för blob-lagring för en Azure Synapse-arbetsyta med namnet ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="96c28-122">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="96c28-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96c28-123">PARAMETERS</span></span>

### <span data-ttu-id="96c28-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96c28-124">-AsJob</span></span>
<span data-ttu-id="96c28-125">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="96c28-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96c28-126">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="96c28-126">-AuditActionGroup</span></span>
<span data-ttu-id="96c28-127">Den rekommenderade uppsättningen åtgärds grupper som ska användas är följande kombination – detta granskar alla frågor och lagrade procedurer som körs mot databasen samt lyckade och misslyckade inloggningar:</span><span class="sxs-lookup"><span data-stu-id="96c28-127">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="96c28-128">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="96c28-128">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="96c28-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="96c28-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="96c28-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="96c28-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="96c28-131">Ovanstående kombination är även den uppsättning som är konfigurerad som standard.</span><span class="sxs-lookup"><span data-stu-id="96c28-131">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="96c28-132">Dessa grupper täcker alla SQL-uttryck och lagrade procedurer som körs mot databasen och ska inte användas i kombination med andra grupper eftersom detta kommer att leda till dubbletter av gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="96c28-132">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="96c28-133">Mer information finns i https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="96c28-133">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="96c28-134">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="96c28-134">-BlobStorageTargetState</span></span>
<span data-ttu-id="96c28-135">Anger om Blob Storage är en destination för gransknings poster.</span><span class="sxs-lookup"><span data-stu-id="96c28-135">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="96c28-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c28-136">-DefaultProfile</span></span>
<span data-ttu-id="96c28-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="96c28-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96c28-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96c28-138">-InputObject</span></span>
<span data-ttu-id="96c28-139">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="96c28-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96c28-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96c28-140">-PassThru</span></span>
<span data-ttu-id="96c28-141">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="96c28-141">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="96c28-142">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="96c28-142">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="96c28-143">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="96c28-143">-PredicateExpression</span></span>
<span data-ttu-id="96c28-144">Uttrycket T-SQL predikat (WHERE-satsen) som används för att filtrera gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="96c28-144">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="96c28-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96c28-145">-ResourceGroupName</span></span>
<span data-ttu-id="96c28-146">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="96c28-146">Resource group name.</span></span>

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

### <span data-ttu-id="96c28-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96c28-147">-ResourceId</span></span>
<span data-ttu-id="96c28-148">Resurs-ID för Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="96c28-148">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="96c28-149">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="96c28-149">-RetentionInDays</span></span>
<span data-ttu-id="96c28-150">Antalet bevarande dagar för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="96c28-150">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="96c28-151">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="96c28-151">-StorageAccountResourceId</span></span>
<span data-ttu-id="96c28-152">Resurs-ID för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="96c28-152">The storage account resource id</span></span>

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

### <span data-ttu-id="96c28-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="96c28-153">-StorageKeyType</span></span>
<span data-ttu-id="96c28-154">Anger vilken av lagrings åtkomst nycklar som ska användas.</span><span class="sxs-lookup"><span data-stu-id="96c28-154">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="96c28-155">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="96c28-155">-WorkspaceName</span></span>
<span data-ttu-id="96c28-156">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="96c28-156">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="96c28-157">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="96c28-157">-Confirm</span></span>
<span data-ttu-id="96c28-158">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="96c28-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96c28-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96c28-159">-WhatIf</span></span>
<span data-ttu-id="96c28-160">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="96c28-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96c28-161">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="96c28-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96c28-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c28-162">CommonParameters</span></span>
<span data-ttu-id="96c28-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96c28-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c28-164">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96c28-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c28-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96c28-165">INPUTS</span></span>

### <span data-ttu-id="96c28-166">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="96c28-166">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="96c28-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96c28-167">OUTPUTS</span></span>

### <span data-ttu-id="96c28-168">Microsoft. Azure. commands. Synapse. Models. WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="96c28-168">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="96c28-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96c28-169">NOTES</span></span>

## <span data-ttu-id="96c28-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96c28-170">RELATED LINKS</span></span>
