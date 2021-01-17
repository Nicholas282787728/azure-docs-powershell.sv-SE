---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
ms.openlocfilehash: e5bb853d9dd818801298254eac1f120efcc829a4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419179"
---
# <span data-ttu-id="5c5ee-101">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="5c5ee-101">Get-AzSqlSyncMember</span></span>

## <span data-ttu-id="5c5ee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5c5ee-102">SYNOPSIS</span></span>
<span data-ttu-id="5c5ee-103">Returnerar information om synkronisering av Azure SQL Database-medlemmar.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-103">Returns information about Azure SQL Database Sync Members.</span></span>

## <span data-ttu-id="5c5ee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5c5ee-104">SYNTAX</span></span>

```
Get-AzSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c5ee-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5c5ee-105">DESCRIPTION</span></span>
<span data-ttu-id="5c5ee-106">Cmdleten **Get-AzSqlSyncMember** returnerar information om en eller flera synkroniserade Azure SQL Database-medlemmar.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-106">The **Get-AzSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="5c5ee-107">Ange namnet på en synkroniserad medlem för att visa information för enbart den synkroniserade medlemmen.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="5c5ee-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5c5ee-108">EXAMPLES</span></span>

### <span data-ttu-id="5c5ee-109">Exempel 1: få alla instanser av Azure SQL Sync-medlem kopplade till en synkroniseringsresurs</span><span class="sxs-lookup"><span data-stu-id="5c5ee-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : Good 

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember02
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      :  
SyncState                   : Good
```

<span data-ttu-id="5c5ee-110">Med det här kommandot får du information om alla synkroniserade Azure SQL Database-medlemmar till SyncGroup01.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="5c5ee-111">Exempel 2: Hämta information om synkronisering av en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="5c5ee-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : Good
```

<span data-ttu-id="5c5ee-112">Det här kommandot får information om synkroniserings medlemmen av Azure SQL Database med namnet "SyncMember01"</span><span class="sxs-lookup"><span data-stu-id="5c5ee-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

### <span data-ttu-id="5c5ee-113">Exempel 3: få alla instanser av Azure SQL Sync-medlem kopplade till en synkroniseringsresurs med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="5c5ee-113">Example 3: Get all instances of Azure SQL Sync Member assigned to a sync group using filtering</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember*" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : Good 

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember02
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      :  
SyncState                   : Good
```

<span data-ttu-id="5c5ee-114">Med det här kommandot får du information om alla SyncGroup01 för Azure SQL Database-synkronisering som börjar med "SyncMember".</span><span class="sxs-lookup"><span data-stu-id="5c5ee-114">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01 that start with "SyncMember".</span></span>

## <span data-ttu-id="5c5ee-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5c5ee-115">PARAMETERS</span></span>

### <span data-ttu-id="5c5ee-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5c5ee-116">-DatabaseName</span></span>
<span data-ttu-id="5c5ee-117">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="5c5ee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c5ee-118">-DefaultProfile</span></span>
<span data-ttu-id="5c5ee-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5c5ee-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c5ee-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="5c5ee-120">-Name</span></span>
<span data-ttu-id="5c5ee-121">Synkroniserat medlems namn.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-121">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c5ee-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c5ee-122">-ResourceGroupName</span></span>
<span data-ttu-id="5c5ee-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="5c5ee-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5c5ee-124">-ServerName</span></span>
<span data-ttu-id="5c5ee-125">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="5c5ee-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="5c5ee-126">-SyncGroupName</span></span>
<span data-ttu-id="5c5ee-127">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-127">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c5ee-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c5ee-128">CommonParameters</span></span>
<span data-ttu-id="5c5ee-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c5ee-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c5ee-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c5ee-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c5ee-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5c5ee-131">INPUTS</span></span>

### <span data-ttu-id="5c5ee-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5c5ee-132">System.String</span></span>

## <span data-ttu-id="5c5ee-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5c5ee-133">OUTPUTS</span></span>

### <span data-ttu-id="5c5ee-134">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="5c5ee-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="5c5ee-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5c5ee-135">NOTES</span></span>

## <span data-ttu-id="5c5ee-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5c5ee-136">RELATED LINKS</span></span>

[<span data-ttu-id="5c5ee-137">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="5c5ee-137">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="5c5ee-138">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="5c5ee-138">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="5c5ee-139">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="5c5ee-139">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

