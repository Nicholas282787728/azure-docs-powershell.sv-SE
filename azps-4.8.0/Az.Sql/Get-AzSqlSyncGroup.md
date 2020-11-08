---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
ms.openlocfilehash: d117ef9685a235528cb91c82a148ff0dddb2d96c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259845"
---
# <span data-ttu-id="14d14-101">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="14d14-101">Get-AzSqlSyncGroup</span></span>

## <span data-ttu-id="14d14-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14d14-102">SYNOPSIS</span></span>
<span data-ttu-id="14d14-103">Returnerar information om synkroniseringsresurser för Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="14d14-103">Returns information about Azure SQL Database Sync Groups.</span></span>

## <span data-ttu-id="14d14-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14d14-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14d14-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14d14-105">DESCRIPTION</span></span>
<span data-ttu-id="14d14-106">Cmdleten **Get-AzSqlSyncGroup** returnerar information om en eller flera synkroniseringsresurser för Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="14d14-106">The **Get-AzSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="14d14-107">Ange namnet på en synkroniseringsresurs för att visa information för enbart den synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="14d14-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="14d14-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14d14-108">EXAMPLES</span></span>

### <span data-ttu-id="14d14-109">Exempel 1: få alla instanser av Azure SQL Sync-gruppen kopplad till en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="14d14-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Format-List
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

<span data-ttu-id="14d14-110">Med det här kommandot får du information om alla synkroniseringsresurser för Azure SQL Database som tilldelats till en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="14d14-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="14d14-111">Exempel 2: Hämta information om en Azure SQL Database Sync-grupp</span><span class="sxs-lookup"><span data-stu-id="14d14-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" | Format-List
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

<span data-ttu-id="14d14-112">Med det här kommandot får du information om synkroniseringsresursen för Azure SQL-databasen med namnet "SyncGroup01"</span><span class="sxs-lookup"><span data-stu-id="14d14-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

### <span data-ttu-id="14d14-113">Exempel 3: Hämta alla instanser av Azure SQL Sync-gruppen som är kopplad till en Azure SQL-databas med filter</span><span class="sxs-lookup"><span data-stu-id="14d14-113">Example 3: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database using filtering</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup*" | Format-List
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

<span data-ttu-id="14d14-114">Med det här kommandot får du information om alla synkroniseringsresurser för Azure SQL-databaser som har tilldelats till en Azure SQL-databas som börjar med "SyncGroup".</span><span class="sxs-lookup"><span data-stu-id="14d14-114">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database that start with "SyncGroup".</span></span>

## <span data-ttu-id="14d14-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14d14-115">PARAMETERS</span></span>

### <span data-ttu-id="14d14-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="14d14-116">-DatabaseName</span></span>
<span data-ttu-id="14d14-117">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="14d14-117">The name of the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d14-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14d14-118">-DefaultProfile</span></span>
<span data-ttu-id="14d14-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="14d14-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14d14-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="14d14-120">-Name</span></span>
<span data-ttu-id="14d14-121">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="14d14-121">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d14-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14d14-122">-ResourceGroupName</span></span>
<span data-ttu-id="14d14-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="14d14-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="14d14-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="14d14-124">-ServerName</span></span>
<span data-ttu-id="14d14-125">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="14d14-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="14d14-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14d14-126">CommonParameters</span></span>
<span data-ttu-id="14d14-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14d14-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14d14-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14d14-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14d14-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14d14-129">INPUTS</span></span>

### <span data-ttu-id="14d14-130">System. String</span><span class="sxs-lookup"><span data-stu-id="14d14-130">System.String</span></span>

## <span data-ttu-id="14d14-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14d14-131">OUTPUTS</span></span>

### <span data-ttu-id="14d14-132">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="14d14-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="14d14-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14d14-133">NOTES</span></span>

## <span data-ttu-id="14d14-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14d14-134">RELATED LINKS</span></span>

[<span data-ttu-id="14d14-135">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="14d14-135">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="14d14-136">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="14d14-136">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="14d14-137">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="14d14-137">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

