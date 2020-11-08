---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
ms.openlocfilehash: 24cc7df97e5942b966d1857052ce647150ccd817
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920636"
---
# <span data-ttu-id="ccadf-101">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ccadf-101">Get-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="ccadf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ccadf-102">SYNOPSIS</span></span>
<span data-ttu-id="ccadf-103">Hämtar gransknings inställningarna för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="ccadf-103">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="ccadf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ccadf-104">SYNTAX</span></span>

### <span data-ttu-id="ccadf-105">DatabaseParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ccadf-105">DatabaseParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccadf-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccadf-106">DatabaseObjectParameterSet</span></span>
```
Get-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ccadf-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ccadf-107">DESCRIPTION</span></span>
<span data-ttu-id="ccadf-108">Cmdleten **Get-AzSqlDatabaseAudit** hämtar gransknings inställningarna för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="ccadf-108">The **Get-AzSqlDatabaseAudit** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="ccadf-109">Använd cmdleten *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="ccadf-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="ccadf-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ccadf-110">EXAMPLES</span></span>

### <span data-ttu-id="ccadf-111">Exempel 1: Hämta gransknings inställningar för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="ccadf-111">Example 1: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="ccadf-112">Exempel 2: gå till pipeline, gransknings inställningar för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="ccadf-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Get-AzSqlDatabaseAudit
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="ccadf-113">Exempel 3: Hämta gransknings inställningar för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="ccadf-113">Example 3: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Disabled
WorkspaceResourceId                 :
```

## <span data-ttu-id="ccadf-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ccadf-114">PARAMETERS</span></span>

### <span data-ttu-id="ccadf-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ccadf-115">-DatabaseName</span></span>
<span data-ttu-id="ccadf-116">Namn på SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="ccadf-116">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccadf-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="ccadf-117">-DatabaseObject</span></span>
<span data-ttu-id="ccadf-118">Databasobjektet för att hantera dess gransknings princip.</span><span class="sxs-lookup"><span data-stu-id="ccadf-118">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccadf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccadf-119">-DefaultProfile</span></span>
<span data-ttu-id="ccadf-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ccadf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccadf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccadf-121">-ResourceGroupName</span></span>
<span data-ttu-id="ccadf-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ccadf-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccadf-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ccadf-123">-ServerName</span></span>
<span data-ttu-id="ccadf-124">SQL Server-namn.</span><span class="sxs-lookup"><span data-stu-id="ccadf-124">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccadf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccadf-125">CommonParameters</span></span>
<span data-ttu-id="ccadf-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccadf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccadf-127">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ccadf-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccadf-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ccadf-128">INPUTS</span></span>

### <span data-ttu-id="ccadf-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ccadf-129">System.String</span></span>

### <span data-ttu-id="ccadf-130">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ccadf-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ccadf-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ccadf-131">OUTPUTS</span></span>

### <span data-ttu-id="ccadf-132">Microsoft. Azure. commands. SQL. granskning. Model. DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="ccadf-132">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="ccadf-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ccadf-133">NOTES</span></span>

## <span data-ttu-id="ccadf-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ccadf-134">RELATED LINKS</span></span>