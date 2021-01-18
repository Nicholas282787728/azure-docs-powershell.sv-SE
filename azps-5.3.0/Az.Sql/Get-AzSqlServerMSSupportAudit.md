---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: c4f3687b2e520783c4b0392e1711dcea976e0c05
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520343"
---
# <span data-ttu-id="db093-101">Get-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="db093-101">Get-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="db093-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db093-102">SYNOPSIS</span></span>
<span data-ttu-id="db093-103">Hämtar gransknings inställningar för Microsoft Support för en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="db093-103">Gets the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="db093-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db093-104">SYNTAX</span></span>

### <span data-ttu-id="db093-105">ServerParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="db093-105">ServerParameterSet (Default)</span></span>
```
Get-AzSqlServerMSSupportAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db093-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db093-106">ServerObjectParameterSet</span></span>
```
Get-AzSqlServerMSSupportAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db093-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db093-107">DESCRIPTION</span></span>
<span data-ttu-id="db093-108">Cmdleten **Get-AzSqlServerMSSupportAudit** får Microsofts support åtgärder gransknings inställningar för en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="db093-108">The **Get-AzSqlServerMSSupportAudit** cmdlet gets the Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="db093-109">Ange parametrarna *ResourceGroupName* och *servername* för att identifiera servern.</span><span class="sxs-lookup"><span data-stu-id="db093-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="db093-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db093-110">EXAMPLES</span></span>

### <span data-ttu-id="db093-111">Exempel 1: Hämta gransknings inställningar för Microsoft Support för en Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="db093-111">Example 1: Get the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerMSSupportAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="db093-112">Exempel 2: gå till pipeline, gransknings inställningar för Microsoft-supporten för en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="db093-112">Example 2: Get, through pipeline, the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerMSSupportAudit
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="db093-113">Exempel 3: Hämta gransknings inställningar för Microsoft Support för en Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="db093-113">Example 3: Get the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerMSSupportAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Disabled
WorkspaceResourceId                 :
```

## <span data-ttu-id="db093-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db093-114">PARAMETERS</span></span>

### <span data-ttu-id="db093-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db093-115">-AsJob</span></span>
<span data-ttu-id="db093-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="db093-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db093-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db093-117">-DefaultProfile</span></span>
<span data-ttu-id="db093-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="db093-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db093-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db093-119">-ResourceGroupName</span></span>
<span data-ttu-id="db093-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="db093-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="db093-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="db093-121">-ServerName</span></span>
<span data-ttu-id="db093-122">SQL Server-namn.</span><span class="sxs-lookup"><span data-stu-id="db093-122">SQL server name.</span></span>

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

### <span data-ttu-id="db093-123">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="db093-123">-ServerObject</span></span>
<span data-ttu-id="db093-124">Serverobjektet för att hantera dess gransknings princip.</span><span class="sxs-lookup"><span data-stu-id="db093-124">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="db093-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db093-125">CommonParameters</span></span>
<span data-ttu-id="db093-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db093-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db093-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db093-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db093-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db093-128">INPUTS</span></span>

### <span data-ttu-id="db093-129">System. String</span><span class="sxs-lookup"><span data-stu-id="db093-129">System.String</span></span>

### <span data-ttu-id="db093-130">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="db093-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="db093-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db093-131">OUTPUTS</span></span>

### <span data-ttu-id="db093-132">Microsoft. Azure. commands. SQL. granskning. Model. ServerDevOpsAuditModel</span><span class="sxs-lookup"><span data-stu-id="db093-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span></span>

## <span data-ttu-id="db093-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db093-133">NOTES</span></span>

## <span data-ttu-id="db093-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db093-134">RELATED LINKS</span></span>
