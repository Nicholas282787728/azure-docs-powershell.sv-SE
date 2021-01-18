---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: 623f52f1de9370c679f6df09b6cf05c50f38ca6b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522771"
---
# <span data-ttu-id="765f6-101">Set-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="765f6-101">Set-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="765f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="765f6-102">SYNOPSIS</span></span>
<span data-ttu-id="765f6-103">Ändrar gransknings inställningarna för Microsoft Support för en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="765f6-103">Changes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="765f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="765f6-104">SYNTAX</span></span>

### <span data-ttu-id="765f6-105">ServerParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="765f6-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerMSSupportAudit
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>]
 [-LogAnalyticsTargetState <String>] [-WorkspaceResourceId <String>]
 [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="765f6-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="765f6-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerMSSupportAudit [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="765f6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="765f6-107">DESCRIPTION</span></span>
<span data-ttu-id="765f6-108">Cmdleten **set-AzSqlServerMSSupportAudit** ändrar gransknings inställningarna för Microsoft Support för en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="765f6-108">The **Set-AzSqlServerMSSupportAudit** cmdlet changes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="765f6-109">Använd cmdleten *ResourceGroupName* och *servername* för att identifiera servern.</span><span class="sxs-lookup"><span data-stu-id="765f6-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="765f6-110">När Blob Storage är en destination för gransknings loggar anger du parametern *StorageAccountResourceId* för att fastställa lagrings kontot för gransknings loggarna.</span><span class="sxs-lookup"><span data-stu-id="765f6-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs.</span></span>

## <span data-ttu-id="765f6-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="765f6-111">EXAMPLES</span></span>

### <span data-ttu-id="765f6-112">Exempel 1: Aktivera gransknings principen för Microsoft Support åtgärd för BLOB för en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="765f6-112">Example 1: Enable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="765f6-113">Exempel 2: inaktivera gransknings princip för Microsoft Support åtgärd för BLOB för en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="765f6-113">Example 2: Disable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="765f6-114">Exempel 3: Aktivera gransknings principen för Microsofts support åtgärder för en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="765f6-114">Example 3: Enable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="765f6-115">Exempel 4: inaktivera en gransknings princip för Microsofts support åtgärder för en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="765f6-115">Example 4: Disable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="765f6-116">Exempel 5: Aktivera gransknings princip för Microsoft Support åtgärder för logganalys för en Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="765f6-116">Example 5: Enable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="765f6-117">Exempel 6: inaktivera gransknings princip för Microsoft Support åtgärder för logganalys för en Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="765f6-117">Example 6: Disable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="765f6-118">Exempel 7: inaktivera, genom pipeline, gransknings princip för Microsofts support åtgärder för en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="765f6-118">Example 7: Disable, through pipeline, the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerMSSupportAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="765f6-119">Exempel 8: inaktivera att skicka Microsoft Support åtgärds poster för en Azure SQL Server till Blob Storage och aktivera dem för att logga analyser.</span><span class="sxs-lookup"><span data-stu-id="765f6-119">Example 8: Disable sending Microsoft support operations audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="765f6-120">Exempel 9: Aktivera överföring av Microsoft Support åtgärds poster för en Azure SQL Server till Blob Storage, händelsehubben och logganalys-analys.</span><span class="sxs-lookup"><span data-stu-id="765f6-120">Example 9: Enable sending Microsoft support operations audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="765f6-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="765f6-121">PARAMETERS</span></span>

### <span data-ttu-id="765f6-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="765f6-122">-AsJob</span></span>
<span data-ttu-id="765f6-123">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="765f6-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="765f6-124">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="765f6-124">-BlobStorageTargetState</span></span>
<span data-ttu-id="765f6-125">Anger om Blob Storage är ett mål för gransknings poster för Microsoft support.</span><span class="sxs-lookup"><span data-stu-id="765f6-125">Indicates whether blob storage is a destination for Microsoft support operations audit records.</span></span>

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

### <span data-ttu-id="765f6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="765f6-126">-DefaultProfile</span></span>
<span data-ttu-id="765f6-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="765f6-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="765f6-128">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="765f6-128">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="765f6-129">Resurs-ID för regel för händelsehubben</span><span class="sxs-lookup"><span data-stu-id="765f6-129">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="765f6-130">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="765f6-130">-EventHubName</span></span>
<span data-ttu-id="765f6-131">Namnet på händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="765f6-131">The name of the event hub.</span></span> <span data-ttu-id="765f6-132">Om ingen anges när du tillhandahåller EventHubAuthorizationRuleResourceId väljs standard händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="765f6-132">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="765f6-133">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="765f6-133">-EventHubTargetState</span></span>
<span data-ttu-id="765f6-134">Anger om händelsehubben är ett mål för gransknings poster för Microsofts support åtgärder.</span><span class="sxs-lookup"><span data-stu-id="765f6-134">Indicates whether event hub is a destination for Microsoft support operations audit records.</span></span>

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

### <span data-ttu-id="765f6-135">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="765f6-135">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="765f6-136">Anger om logg analys är ett mål för gransknings poster för Microsoft support.</span><span class="sxs-lookup"><span data-stu-id="765f6-136">Indicates whether log analytics is a destination for Microsoft support operations audit records.</span></span>

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

### <span data-ttu-id="765f6-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="765f6-137">-PassThru</span></span>
<span data-ttu-id="765f6-138">Anger om gransknings princip för Microsoft-supporten ska visas när cmdlet körs</span><span class="sxs-lookup"><span data-stu-id="765f6-138">Specifies whether to output the Microsoft support operations auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="765f6-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="765f6-139">-ResourceGroupName</span></span>
<span data-ttu-id="765f6-140">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="765f6-140">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="765f6-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="765f6-141">-ServerName</span></span>
<span data-ttu-id="765f6-142">SQL Server-namn.</span><span class="sxs-lookup"><span data-stu-id="765f6-142">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="765f6-143">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="765f6-143">-ServerObject</span></span>
<span data-ttu-id="765f6-144">Serverobjektet för att hantera gransknings principer för Microsoft support.</span><span class="sxs-lookup"><span data-stu-id="765f6-144">The server object to manage its Microsoft support operations audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="765f6-145">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="765f6-145">-StorageAccountResourceId</span></span>
<span data-ttu-id="765f6-146">Resurs-ID för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="765f6-146">The storage account resource id</span></span>

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

### <span data-ttu-id="765f6-147">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="765f6-147">-WorkspaceResourceId</span></span>
<span data-ttu-id="765f6-148">Arbetsyte-ID (resurs-ID för en logganalys-arbetsyta) för en logganalys-arbetsyta till vilken du vill skicka Microsofts support processer för granskning.</span><span class="sxs-lookup"><span data-stu-id="765f6-148">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Microsoft support operations Audit Logs.</span></span> <span data-ttu-id="765f6-149">Exempel:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="765f6-149">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="765f6-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="765f6-150">-Confirm</span></span>
<span data-ttu-id="765f6-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="765f6-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="765f6-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="765f6-152">-WhatIf</span></span>
<span data-ttu-id="765f6-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="765f6-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="765f6-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="765f6-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="765f6-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="765f6-155">CommonParameters</span></span>
<span data-ttu-id="765f6-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="765f6-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="765f6-157">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="765f6-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="765f6-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="765f6-158">INPUTS</span></span>

### <span data-ttu-id="765f6-159">System. String</span><span class="sxs-lookup"><span data-stu-id="765f6-159">System.String</span></span>

### <span data-ttu-id="765f6-160">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="765f6-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="765f6-161">System. GUID</span><span class="sxs-lookup"><span data-stu-id="765f6-161">System.Guid</span></span>

### <span data-ttu-id="765f6-162">System. Nullable ' 1 [[system. UInt32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="765f6-162">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="765f6-163">Microsoft. Azure. commands. SQL. granskning. Model. ServerDevOpsAuditModel</span><span class="sxs-lookup"><span data-stu-id="765f6-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span></span>

## <span data-ttu-id="765f6-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="765f6-164">OUTPUTS</span></span>

### <span data-ttu-id="765f6-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="765f6-165">System.Boolean</span></span>

## <span data-ttu-id="765f6-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="765f6-166">NOTES</span></span>

## <span data-ttu-id="765f6-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="765f6-167">RELATED LINKS</span></span>
