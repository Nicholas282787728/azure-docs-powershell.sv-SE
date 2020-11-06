---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 3041d7a25ad87e6e2b9242043645a66219ac7e46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579324"
---
# <span data-ttu-id="b9e47-101">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="b9e47-101">Get-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="b9e47-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b9e47-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e47-103">Returnerar information om Azure SQL Sync-agenter.</span><span class="sxs-lookup"><span data-stu-id="b9e47-103">Returns information about Azure SQL Sync Agents.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9e47-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b9e47-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9e47-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b9e47-105">DESCRIPTION</span></span>
<span data-ttu-id="b9e47-106">Cmdleten **Get-AzureRmSqlSyncAgent** returnerar information om en eller flera Sync-agenter för Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b9e47-106">The **Get-AzureRmSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="b9e47-107">Ange namnet på en synkroniseringsresurs för att visa information för enbart den synkroniseringsklienten.</span><span class="sxs-lookup"><span data-stu-id="b9e47-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="b9e47-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b9e47-108">EXAMPLES</span></span>

### <span data-ttu-id="b9e47-109">Exempel 1: få alla instanser av Azure SQL Sync agent tilldelad till en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="b9e47-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
```
PS C:\>Get-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
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

<span data-ttu-id="b9e47-110">Med det här kommandot får du information om alla de Azure SQL Sync-agenter som tilldelats en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b9e47-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="b9e47-111">Exempel 2: Hämta information om en Azure SQL Sync-agent</span><span class="sxs-lookup"><span data-stu-id="b9e47-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
```
PS C:\>Get-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" | Format-List
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

<span data-ttu-id="b9e47-112">Det här kommandot får information om Synkroniseringshanteraren för Azure SQL Database med namnet "SyncAgent01"</span><span class="sxs-lookup"><span data-stu-id="b9e47-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

## <span data-ttu-id="b9e47-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b9e47-113">PARAMETERS</span></span>

### <span data-ttu-id="b9e47-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e47-114">-DefaultProfile</span></span>
<span data-ttu-id="b9e47-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b9e47-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9e47-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="b9e47-116">-Name</span></span>
<span data-ttu-id="b9e47-117">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="b9e47-117">The sync agent name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e47-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9e47-118">-ResourceGroupName</span></span>
<span data-ttu-id="b9e47-119">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b9e47-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="b9e47-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b9e47-120">-ServerName</span></span>
<span data-ttu-id="b9e47-121">Namnet på den Azure SQL-Server som synkroniseringsresursen finns i.</span><span class="sxs-lookup"><span data-stu-id="b9e47-121">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="b9e47-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e47-122">CommonParameters</span></span>
<span data-ttu-id="b9e47-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9e47-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e47-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9e47-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e47-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b9e47-125">INPUTS</span></span>

### <span data-ttu-id="b9e47-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="b9e47-126">None</span></span>
<span data-ttu-id="b9e47-127">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b9e47-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b9e47-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b9e47-128">OUTPUTS</span></span>

### <span data-ttu-id="b9e47-129">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="b9e47-129">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="b9e47-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b9e47-130">NOTES</span></span>

## <span data-ttu-id="b9e47-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b9e47-131">RELATED LINKS</span></span>

[<span data-ttu-id="b9e47-132">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="b9e47-132">Remove-AzureRmSqlSyncAgent</span></span>](./Remove-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="b9e47-133">New-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="b9e47-133">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)

