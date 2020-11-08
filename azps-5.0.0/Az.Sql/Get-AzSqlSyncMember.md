---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
ms.openlocfilehash: e5bb853d9dd818801298254eac1f120efcc829a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263393"
---
# <span data-ttu-id="d1c48-101">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d1c48-101">Get-AzSqlSyncMember</span></span>

## <span data-ttu-id="d1c48-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1c48-102">SYNOPSIS</span></span>
<span data-ttu-id="d1c48-103">Returnerar information om synkronisering av Azure SQL Database-medlemmar.</span><span class="sxs-lookup"><span data-stu-id="d1c48-103">Returns information about Azure SQL Database Sync Members.</span></span>

## <span data-ttu-id="d1c48-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1c48-104">SYNTAX</span></span>

```
Get-AzSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1c48-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1c48-105">DESCRIPTION</span></span>
<span data-ttu-id="d1c48-106">Cmdleten **Get-AzSqlSyncMember** returnerar information om en eller flera synkroniserade Azure SQL Database-medlemmar.</span><span class="sxs-lookup"><span data-stu-id="d1c48-106">The **Get-AzSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="d1c48-107">Ange namnet på en synkroniserad medlem för att visa information för enbart den synkroniserade medlemmen.</span><span class="sxs-lookup"><span data-stu-id="d1c48-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="d1c48-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1c48-108">EXAMPLES</span></span>

### <span data-ttu-id="d1c48-109">Exempel 1: få alla instanser av Azure SQL Sync-medlem kopplade till en synkroniseringsresurs</span><span class="sxs-lookup"><span data-stu-id="d1c48-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
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

<span data-ttu-id="d1c48-110">Med det här kommandot får du information om alla synkroniserade Azure SQL Database-medlemmar till SyncGroup01.</span><span class="sxs-lookup"><span data-stu-id="d1c48-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="d1c48-111">Exempel 2: Hämta information om synkronisering av en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="d1c48-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
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

<span data-ttu-id="d1c48-112">Det här kommandot får information om synkroniserings medlemmen av Azure SQL Database med namnet "SyncMember01"</span><span class="sxs-lookup"><span data-stu-id="d1c48-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

### <span data-ttu-id="d1c48-113">Exempel 3: få alla instanser av Azure SQL Sync-medlem kopplade till en synkroniseringsresurs med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="d1c48-113">Example 3: Get all instances of Azure SQL Sync Member assigned to a sync group using filtering</span></span>
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

<span data-ttu-id="d1c48-114">Med det här kommandot får du information om alla SyncGroup01 för Azure SQL Database-synkronisering som börjar med "SyncMember".</span><span class="sxs-lookup"><span data-stu-id="d1c48-114">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01 that start with "SyncMember".</span></span>

## <span data-ttu-id="d1c48-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1c48-115">PARAMETERS</span></span>

### <span data-ttu-id="d1c48-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d1c48-116">-DatabaseName</span></span>
<span data-ttu-id="d1c48-117">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="d1c48-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d1c48-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1c48-118">-DefaultProfile</span></span>
<span data-ttu-id="d1c48-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d1c48-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1c48-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="d1c48-120">-Name</span></span>
<span data-ttu-id="d1c48-121">Synkroniserat medlems namn.</span><span class="sxs-lookup"><span data-stu-id="d1c48-121">The sync member name.</span></span>

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

### <span data-ttu-id="d1c48-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1c48-122">-ResourceGroupName</span></span>
<span data-ttu-id="d1c48-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d1c48-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="d1c48-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d1c48-124">-ServerName</span></span>
<span data-ttu-id="d1c48-125">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d1c48-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="d1c48-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="d1c48-126">-SyncGroupName</span></span>
<span data-ttu-id="d1c48-127">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="d1c48-127">The sync group name.</span></span>

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

### <span data-ttu-id="d1c48-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1c48-128">CommonParameters</span></span>
<span data-ttu-id="d1c48-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1c48-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1c48-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1c48-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1c48-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1c48-131">INPUTS</span></span>

### <span data-ttu-id="d1c48-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d1c48-132">System.String</span></span>

## <span data-ttu-id="d1c48-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1c48-133">OUTPUTS</span></span>

### <span data-ttu-id="d1c48-134">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="d1c48-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="d1c48-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1c48-135">NOTES</span></span>

## <span data-ttu-id="d1c48-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1c48-136">RELATED LINKS</span></span>

[<span data-ttu-id="d1c48-137">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d1c48-137">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="d1c48-138">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d1c48-138">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="d1c48-139">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d1c48-139">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

