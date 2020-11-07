---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
ms.openlocfilehash: e581f0bd94e58f725055c0dc1a4f1d704b891c86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755421"
---
# <span data-ttu-id="df52c-101">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="df52c-101">Get-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="df52c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df52c-102">SYNOPSIS</span></span>
<span data-ttu-id="df52c-103">Returnerar information om synkroniseringsresurser för Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="df52c-103">Returns information about Azure SQL Database Sync Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df52c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df52c-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df52c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df52c-105">DESCRIPTION</span></span>
<span data-ttu-id="df52c-106">Cmdleten **Get-AzureRmSqlSyncGroup** returnerar information om en eller flera synkroniseringsresurser för Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="df52c-106">The **Get-AzureRmSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="df52c-107">Ange namnet på en synkroniseringsresurs för att visa information för enbart den synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="df52c-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="df52c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df52c-108">EXAMPLES</span></span>

### <span data-ttu-id="df52c-109">Exempel 1: få alla instanser av Azure SQL Sync-gruppen kopplad till en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="df52c-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
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

<span data-ttu-id="df52c-110">Med det här kommandot får du information om alla synkroniseringsresurser för Azure SQL Database som tilldelats till en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="df52c-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="df52c-111">Exempel 2: Hämta information om en Azure SQL Database Sync-grupp</span><span class="sxs-lookup"><span data-stu-id="df52c-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
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

<span data-ttu-id="df52c-112">Med det här kommandot får du information om synkroniseringsresursen för Azure SQL-databasen med namnet "SyncGroup01"</span><span class="sxs-lookup"><span data-stu-id="df52c-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

## <span data-ttu-id="df52c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df52c-113">PARAMETERS</span></span>

### <span data-ttu-id="df52c-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="df52c-114">-DatabaseName</span></span>
<span data-ttu-id="df52c-115">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="df52c-115">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="df52c-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="df52c-116">-Name</span></span>
<span data-ttu-id="df52c-117">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="df52c-117">The sync group name.</span></span>

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

### <span data-ttu-id="df52c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df52c-118">-ResourceGroupName</span></span>
<span data-ttu-id="df52c-119">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="df52c-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="df52c-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="df52c-120">-ServerName</span></span>
<span data-ttu-id="df52c-121">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="df52c-121">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="df52c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df52c-122">-DefaultProfile</span></span>
<span data-ttu-id="df52c-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="df52c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df52c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df52c-124">CommonParameters</span></span>
<span data-ttu-id="df52c-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df52c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df52c-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df52c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df52c-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df52c-127">INPUTS</span></span>

## <span data-ttu-id="df52c-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df52c-128">OUTPUTS</span></span>

### <span data-ttu-id="df52c-129">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="df52c-129">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="df52c-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df52c-130">NOTES</span></span>

## <span data-ttu-id="df52c-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df52c-131">RELATED LINKS</span></span>

[<span data-ttu-id="df52c-132">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="df52c-132">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="df52c-133">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="df52c-133">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="df52c-134">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="df52c-134">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

