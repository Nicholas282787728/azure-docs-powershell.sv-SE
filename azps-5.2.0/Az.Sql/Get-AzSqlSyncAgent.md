---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
ms.openlocfilehash: 8bb031ffa2924ce0cace8d2c7daf94be97713eec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406000"
---
# <span data-ttu-id="46aea-101">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="46aea-101">Get-AzSqlSyncAgent</span></span>

## <span data-ttu-id="46aea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46aea-102">SYNOPSIS</span></span>
<span data-ttu-id="46aea-103">Returnerar information om Azure SQL Sync-agenter.</span><span class="sxs-lookup"><span data-stu-id="46aea-103">Returns information about Azure SQL Sync Agents.</span></span>

## <span data-ttu-id="46aea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46aea-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46aea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46aea-105">DESCRIPTION</span></span>
<span data-ttu-id="46aea-106">Cmdleten **Get-AzSqlSyncAgent** returnerar information om en eller flera Sync-agenter för Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="46aea-106">The **Get-AzSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="46aea-107">Ange namnet på en synkroniseringsresurs för att visa information för enbart den synkroniseringsklienten.</span><span class="sxs-lookup"><span data-stu-id="46aea-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="46aea-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46aea-108">EXAMPLES</span></span>

### <span data-ttu-id="46aea-109">Exempel 1: få alla instanser av Azure SQL Sync agent tilldelad till en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="46aea-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="46aea-110">Med det här kommandot får du information om alla de Azure SQL Sync-agenter som tilldelats en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="46aea-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="46aea-111">Exempel 2: Hämta information om en Azure SQL Sync-agent</span><span class="sxs-lookup"><span data-stu-id="46aea-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="46aea-112">Det här kommandot får information om Synkroniseringshanteraren för Azure SQL Database med namnet "SyncAgent01"</span><span class="sxs-lookup"><span data-stu-id="46aea-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

### <span data-ttu-id="46aea-113">Exempel 3: Hämta alla instanser av Azure SQL Sync agent som är tilldelad en Azure SQL-Server med filter</span><span class="sxs-lookup"><span data-stu-id="46aea-113">Example 3: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server using filtering</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name SyncAgent* | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="46aea-114">Med det här kommandot får du information om alla de Azure SQL Sync-agenter som tilldelats en Azure SQL-Server som börjar med "SyncAgent".</span><span class="sxs-lookup"><span data-stu-id="46aea-114">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server that start with "SyncAgent".</span></span>

## <span data-ttu-id="46aea-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46aea-115">PARAMETERS</span></span>

### <span data-ttu-id="46aea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46aea-116">-DefaultProfile</span></span>
<span data-ttu-id="46aea-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="46aea-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46aea-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="46aea-118">-Name</span></span>
<span data-ttu-id="46aea-119">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="46aea-119">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46aea-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46aea-120">-ResourceGroupName</span></span>
<span data-ttu-id="46aea-121">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="46aea-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="46aea-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="46aea-122">-ServerName</span></span>
<span data-ttu-id="46aea-123">Namnet på den Azure SQL-Server som synkroniseringsresursen finns i.</span><span class="sxs-lookup"><span data-stu-id="46aea-123">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="46aea-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46aea-124">CommonParameters</span></span>
<span data-ttu-id="46aea-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46aea-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46aea-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46aea-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46aea-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46aea-127">INPUTS</span></span>

### <span data-ttu-id="46aea-128">System. String</span><span class="sxs-lookup"><span data-stu-id="46aea-128">System.String</span></span>

## <span data-ttu-id="46aea-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46aea-129">OUTPUTS</span></span>

### <span data-ttu-id="46aea-130">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="46aea-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="46aea-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46aea-131">NOTES</span></span>

## <span data-ttu-id="46aea-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46aea-132">RELATED LINKS</span></span>

[<span data-ttu-id="46aea-133">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="46aea-133">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="46aea-134">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="46aea-134">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

