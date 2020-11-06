---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 71a4d20c6296c8a9d725cb9a16960d6c4a06646c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575471"
---
# <span data-ttu-id="c29d6-101">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c29d6-101">Get-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="c29d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c29d6-102">SYNOPSIS</span></span>
<span data-ttu-id="c29d6-103">Returnerar information om synkroniseringsresurser för Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="c29d6-103">Returns information about Azure SQL Database Sync Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c29d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c29d6-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c29d6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c29d6-105">DESCRIPTION</span></span>
<span data-ttu-id="c29d6-106">Cmdleten **Get-AzureRmSqlSyncGroup** returnerar information om en eller flera synkroniseringsresurser för Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="c29d6-106">The **Get-AzureRmSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="c29d6-107">Ange namnet på en synkroniseringsresurs för att visa information för enbart den synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="c29d6-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="c29d6-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c29d6-108">EXAMPLES</span></span>

### <span data-ttu-id="c29d6-109">Exempel 1: få alla instanser av Azure SQL Sync-gruppen kopplad till en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="c29d6-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :  

ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="c29d6-110">Med det här kommandot får du information om alla synkroniseringsresurser för Azure SQL Database som tilldelats till en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="c29d6-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="c29d6-111">Exempel 2: Hämta information om en Azure SQL Database Sync-grupp</span><span class="sxs-lookup"><span data-stu-id="c29d6-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="c29d6-112">Med det här kommandot får du information om synkroniseringsresursen för Azure SQL-databasen med namnet "SyncGroup01"</span><span class="sxs-lookup"><span data-stu-id="c29d6-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

## <span data-ttu-id="c29d6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c29d6-113">PARAMETERS</span></span>

### <span data-ttu-id="c29d6-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c29d6-114">-DatabaseName</span></span>
<span data-ttu-id="c29d6-115">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="c29d6-115">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c29d6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c29d6-116">-DefaultProfile</span></span>
<span data-ttu-id="c29d6-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c29d6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c29d6-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="c29d6-118">-Name</span></span>
<span data-ttu-id="c29d6-119">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="c29d6-119">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c29d6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c29d6-120">-ResourceGroupName</span></span>
<span data-ttu-id="c29d6-121">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c29d6-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="c29d6-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c29d6-122">-ServerName</span></span>
<span data-ttu-id="c29d6-123">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c29d6-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="c29d6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c29d6-124">CommonParameters</span></span>
<span data-ttu-id="c29d6-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c29d6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c29d6-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c29d6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c29d6-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c29d6-127">INPUTS</span></span>

### <span data-ttu-id="c29d6-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="c29d6-128">None</span></span>
<span data-ttu-id="c29d6-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c29d6-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c29d6-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c29d6-130">OUTPUTS</span></span>

### <span data-ttu-id="c29d6-131">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="c29d6-131">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="c29d6-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c29d6-132">NOTES</span></span>

## <span data-ttu-id="c29d6-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c29d6-133">RELATED LINKS</span></span>

[<span data-ttu-id="c29d6-134">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c29d6-134">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="c29d6-135">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c29d6-135">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="c29d6-136">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c29d6-136">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

