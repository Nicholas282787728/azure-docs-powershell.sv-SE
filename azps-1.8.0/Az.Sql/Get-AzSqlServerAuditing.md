---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
ms.openlocfilehash: ba225571780d4d09dfd5ecc1b47132462468b734
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746677"
---
# <span data-ttu-id="b8669-101">Get-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="b8669-101">Get-AzSqlServerAuditing</span></span>

## <span data-ttu-id="b8669-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8669-102">SYNOPSIS</span></span>
<span data-ttu-id="b8669-103">Hämtar gransknings inställningarna för en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b8669-103">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="b8669-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8669-104">SYNTAX</span></span>

### <span data-ttu-id="b8669-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b8669-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8669-106">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="b8669-106">EventHubSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8669-107">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="b8669-107">LogAnalyticsSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8669-108">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="b8669-108">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8669-109">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="b8669-109">EventHubByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8669-110">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="b8669-110">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8669-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8669-111">DESCRIPTION</span></span>
<span data-ttu-id="b8669-112">Cmdleten **Get-AzSqlServerAuditing** hämtar gransknings inställningarna för en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b8669-112">The **Get-AzSqlServerAuditing** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="b8669-113">Ange parametrarna *ResourceGroupName* och *servername* för att identifiera servern.</span><span class="sxs-lookup"><span data-stu-id="b8669-113">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="b8669-114">Mål platsen för gransknings loggar bestäms genom att ange en av följande växel parametrar: BlobStorage, LogAnalytics eller EventHub (om ingen är angiven är standardvärdet BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="b8669-114">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="b8669-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8669-115">EXAMPLES</span></span>

### <span data-ttu-id="b8669-116">Exempel 1: Hämta gransknings inställningar för en Azure SQL-Server för blob-lagring</span><span class="sxs-lookup"><span data-stu-id="b8669-116">Example 1: Get the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

### <span data-ttu-id="b8669-117">Exempel 2: Hämta gransknings inställningar för blob-lagring för en Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="b8669-117">Example 2: Get the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -BlobStorage
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

### <span data-ttu-id="b8669-118">Exempel 3: Hämta, genom pipeline, gransknings inställningar för blob-lagring för en Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="b8669-118">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerAuditing -BlobStorage
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

### <span data-ttu-id="b8669-119">Exempel 4: Hämta gransknings inställningar för en Azure SQL-Server för Event Hub</span><span class="sxs-lookup"><span data-stu-id="b8669-119">Example 4: Get the event hub auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -EventHub
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
PredicateExpression                 : statement <> 'select 1'
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
```

### <span data-ttu-id="b8669-120">Exempel 5: Hämta, genom pipeline, gransknings inställningar för en Azure SQL-Server i Event Hub</span><span class="sxs-lookup"><span data-stu-id="b8669-120">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL server</span></span>
```
PS C:\>$server = Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
PS C:\>$server | Get-AzSqlServerAuditing -EventHub
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
PredicateExpression                 : statement <> 'select 1'
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
```

### <span data-ttu-id="b8669-121">Exempel 6: Hämta gransknings inställningar för logganalys för en Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="b8669-121">Example 6: Get the log analytics auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -LogAnalytics
AuditActionGroup    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName   : resourcegroup01
ServerName          : server01
AuditState          : Enabled
PredicateExpression : statement <> 'select 1'
WorkspaceResourceId : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="b8669-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8669-122">PARAMETERS</span></span>

### <span data-ttu-id="b8669-123">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="b8669-123">-BlobStorage</span></span>
<span data-ttu-id="b8669-124">Anger att gransknings loggar destinationen är Blob Storage</span><span class="sxs-lookup"><span data-stu-id="b8669-124">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="b8669-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8669-125">-DefaultProfile</span></span>
<span data-ttu-id="b8669-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b8669-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8669-127">-EventHub</span><span class="sxs-lookup"><span data-stu-id="b8669-127">-EventHub</span></span>
<span data-ttu-id="b8669-128">Anger att gransknings loggar destinationen är händelsehubben</span><span class="sxs-lookup"><span data-stu-id="b8669-128">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="b8669-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8669-129">-InputObject</span></span>
<span data-ttu-id="b8669-130">Serverobjektet för att hantera dess gransknings princip.</span><span class="sxs-lookup"><span data-stu-id="b8669-130">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: BlobStorageByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8669-131">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="b8669-131">-LogAnalytics</span></span>
<span data-ttu-id="b8669-132">Anger att gransknings loggar destinationen är logg analys</span><span class="sxs-lookup"><span data-stu-id="b8669-132">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="b8669-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8669-133">-ResourceGroupName</span></span>
<span data-ttu-id="b8669-134">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b8669-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="b8669-135">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b8669-135">-ServerName</span></span>
<span data-ttu-id="b8669-136">SQL Server-namn.</span><span class="sxs-lookup"><span data-stu-id="b8669-136">SQL server name.</span></span>

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

### <span data-ttu-id="b8669-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b8669-137">-Confirm</span></span>
<span data-ttu-id="b8669-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b8669-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8669-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8669-139">-WhatIf</span></span>
<span data-ttu-id="b8669-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b8669-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8669-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b8669-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8669-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8669-142">CommonParameters</span></span>
<span data-ttu-id="b8669-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8669-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8669-144">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8669-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8669-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8669-145">INPUTS</span></span>

### <span data-ttu-id="b8669-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b8669-146">System.String</span></span>

### <span data-ttu-id="b8669-147">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="b8669-147">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="b8669-148">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b8669-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b8669-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8669-149">OUTPUTS</span></span>

### <span data-ttu-id="b8669-150">Microsoft. Azure. commands. SQL. granskning. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="b8669-150">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="b8669-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8669-151">NOTES</span></span>

## <span data-ttu-id="b8669-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8669-152">RELATED LINKS</span></span>
