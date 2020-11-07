---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
ms.openlocfilehash: 641ab27f75950a2c15035a7787346250a41f9ab9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920423"
---
# <span data-ttu-id="102f4-101">Get-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="102f4-101">Get-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="102f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="102f4-102">SYNOPSIS</span></span>
<span data-ttu-id="102f4-103">**Viktigt: denna cmdlet är föråldrad och [AzSqlDatbaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseaudit) ersätter den.**</span><span class="sxs-lookup"><span data-stu-id="102f4-103">**Important: This cmdlet is deprecated, [Get-AzSqlDatbaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseaudit) is replacing it.**</span></span>

<span data-ttu-id="102f4-104">Hämtar gransknings inställningarna för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="102f4-104">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="102f4-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="102f4-105">SYNTAX</span></span>

### <span data-ttu-id="102f4-106">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="102f4-106">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-BlobStorage] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="102f4-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="102f4-107">EventHubSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-EventHub] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="102f4-108">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="102f4-108">LogAnalyticsSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="102f4-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="102f4-109">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="102f4-110">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="102f4-110">EventHubByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="102f4-111">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="102f4-111">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="102f4-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="102f4-112">DESCRIPTION</span></span>
<span data-ttu-id="102f4-113">Cmdleten **Get-AzSqlDatabaseAuditing** hämtar gransknings inställningarna för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="102f4-113">The **Get-AzSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="102f4-114">Använd cmdleten *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="102f4-114">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="102f4-115">Mål platsen för gransknings loggar bestäms genom att ange en av följande växel parametrar: BlobStorage, LogAnalytics eller EventHub (om ingen är angiven är standardvärdet BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="102f4-115">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="102f4-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="102f4-116">EXAMPLES</span></span>

### <span data-ttu-id="102f4-117">Exempel 1: Hämta gransknings inställningar för blob-lagring för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="102f4-117">Example 1: Get the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="102f4-118">Exempel 2: Hämta gransknings inställningar för blob-lagring för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="102f4-118">Example 2: Get the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorage
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="102f4-119">Exempel 3: Hämta och gå igenom pipeline, gransknings inställningar för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="102f4-119">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Get-AzSqlDatabaseAuditing
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="102f4-120">Exempel 4: Hämta gransknings inställningar för en Azure SQL-databas till Event Hub</span><span class="sxs-lookup"><span data-stu-id="102f4-120">Example 4: Get the event hub auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHub
DatabaseName                        : database01
AuditAction                         : {}
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
PredicateExpression                 : statement <> 'select 1'
```

### <span data-ttu-id="102f4-121">Exempel 5: Hämta, genom pipeline, gransknings inställningar för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="102f4-121">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL database</span></span>
```
PS C:\>$database = Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\>$database | Get-AzSqlDatabaseAuditing -EventHub
DatabaseName                        : database01
AuditAction                         : {}
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
PredicateExpression                 : statement <> 'select 1'
```

### <span data-ttu-id="102f4-122">Exempel 6: Hämta gransknings inställningar för logganalys för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="102f4-122">Example 6: Get the log analytics auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
DatabaseName        : database01
AuditAction         : {}
AuditActionGroup    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName   : resourcegroup01
ServerName          : server01
AuditState          : Enabled
PredicateExpression : statement <> 'select 1'
WorkspaceResourceId : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="102f4-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="102f4-123">PARAMETERS</span></span>

### <span data-ttu-id="102f4-124">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="102f4-124">-BlobStorage</span></span>
<span data-ttu-id="102f4-125">Anger att gransknings loggar destinationen är Blob Storage</span><span class="sxs-lookup"><span data-stu-id="102f4-125">Specifies that audit logs destination is blob storage</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="102f4-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="102f4-126">-DatabaseName</span></span>
<span data-ttu-id="102f4-127">Namn på SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="102f4-127">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="102f4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="102f4-128">-DefaultProfile</span></span>
<span data-ttu-id="102f4-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="102f4-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="102f4-130">-EventHub</span><span class="sxs-lookup"><span data-stu-id="102f4-130">-EventHub</span></span>
<span data-ttu-id="102f4-131">Anger att gransknings loggar destinationen är händelsehubben</span><span class="sxs-lookup"><span data-stu-id="102f4-131">Specifies that audit logs destination is event hub</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="102f4-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="102f4-132">-InputObject</span></span>
<span data-ttu-id="102f4-133">Databasobjektet för att hantera dess gransknings princip.</span><span class="sxs-lookup"><span data-stu-id="102f4-133">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: BlobStorageByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="102f4-134">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="102f4-134">-LogAnalytics</span></span>
<span data-ttu-id="102f4-135">Anger att gransknings loggar destinationen är logg analys</span><span class="sxs-lookup"><span data-stu-id="102f4-135">Specifies that audit logs destination is log analytics</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="102f4-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="102f4-136">-ResourceGroupName</span></span>
<span data-ttu-id="102f4-137">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="102f4-137">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="102f4-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="102f4-138">-ServerName</span></span>
<span data-ttu-id="102f4-139">SQL Server-namn.</span><span class="sxs-lookup"><span data-stu-id="102f4-139">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="102f4-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="102f4-140">-Confirm</span></span>
<span data-ttu-id="102f4-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="102f4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="102f4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="102f4-142">-WhatIf</span></span>
<span data-ttu-id="102f4-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="102f4-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="102f4-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="102f4-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="102f4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="102f4-145">CommonParameters</span></span>
<span data-ttu-id="102f4-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="102f4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="102f4-147">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="102f4-147">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="102f4-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="102f4-148">INPUTS</span></span>

### <span data-ttu-id="102f4-149">System. String</span><span class="sxs-lookup"><span data-stu-id="102f4-149">System.String</span></span>

### <span data-ttu-id="102f4-150">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="102f4-150">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="102f4-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="102f4-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="102f4-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="102f4-152">OUTPUTS</span></span>

### <span data-ttu-id="102f4-153">Microsoft. Azure. commands. SQL. granskning. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="102f4-153">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="102f4-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="102f4-154">NOTES</span></span>

## <span data-ttu-id="102f4-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="102f4-155">RELATED LINKS</span></span>
