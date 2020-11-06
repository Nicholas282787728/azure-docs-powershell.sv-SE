---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncMember.md
ms.openlocfilehash: bd828a88b870174b870d3acb963cdcb3b3c58ef1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574491"
---
# <span data-ttu-id="a0f70-101">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a0f70-101">Get-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="a0f70-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a0f70-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f70-103">Returnerar information om synkronisering av Azure SQL Database-medlemmar.</span><span class="sxs-lookup"><span data-stu-id="a0f70-103">Returns information about Azure SQL Database Sync Members.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0f70-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a0f70-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0f70-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a0f70-105">DESCRIPTION</span></span>
<span data-ttu-id="a0f70-106">Cmdleten **Get-AzureRmSqlSyncMember** returnerar information om en eller flera synkroniserade Azure SQL Database-medlemmar.</span><span class="sxs-lookup"><span data-stu-id="a0f70-106">The **Get-AzureRmSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="a0f70-107">Ange namnet på en synkroniserad medlem för att visa information för enbart den synkroniserade medlemmen.</span><span class="sxs-lookup"><span data-stu-id="a0f70-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="a0f70-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a0f70-108">EXAMPLES</span></span>

### <span data-ttu-id="a0f70-109">Exempel 1: få alla instanser av Azure SQL Sync-medlem kopplade till en synkroniseringsresurs</span><span class="sxs-lookup"><span data-stu-id="a0f70-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
```
PS C:\>Get-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" | Format-List
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

<span data-ttu-id="a0f70-110">Med det här kommandot får du information om alla synkroniserade Azure SQL Database-medlemmar till SyncGroup01.</span><span class="sxs-lookup"><span data-stu-id="a0f70-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="a0f70-111">Exempel 2: Hämta information om synkronisering av en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="a0f70-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
```
PS C:\>Get-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" | Format-List
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

<span data-ttu-id="a0f70-112">Det här kommandot får information om synkroniserings medlemmen av Azure SQL Database med namnet "SyncMember01"</span><span class="sxs-lookup"><span data-stu-id="a0f70-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

## <span data-ttu-id="a0f70-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a0f70-113">PARAMETERS</span></span>

### <span data-ttu-id="a0f70-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a0f70-114">-DatabaseName</span></span>
<span data-ttu-id="a0f70-115">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="a0f70-115">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a0f70-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="a0f70-116">-Name</span></span>
<span data-ttu-id="a0f70-117">Synkroniserat medlems namn.</span><span class="sxs-lookup"><span data-stu-id="a0f70-117">The sync member name.</span></span>

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

### <span data-ttu-id="a0f70-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0f70-118">-ResourceGroupName</span></span>
<span data-ttu-id="a0f70-119">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a0f70-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="a0f70-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a0f70-120">-ServerName</span></span>
<span data-ttu-id="a0f70-121">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a0f70-121">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="a0f70-122">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a0f70-122">-SyncGroupName</span></span>
<span data-ttu-id="a0f70-123">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="a0f70-123">The sync group name.</span></span>

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

### <span data-ttu-id="a0f70-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f70-124">-DefaultProfile</span></span>
<span data-ttu-id="a0f70-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a0f70-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0f70-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f70-126">CommonParameters</span></span>
<span data-ttu-id="a0f70-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0f70-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f70-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0f70-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f70-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a0f70-129">INPUTS</span></span>

## <span data-ttu-id="a0f70-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a0f70-130">OUTPUTS</span></span>

### <span data-ttu-id="a0f70-131">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="a0f70-131">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="a0f70-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a0f70-132">NOTES</span></span>

## <span data-ttu-id="a0f70-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a0f70-133">RELATED LINKS</span></span>

[<span data-ttu-id="a0f70-134">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a0f70-134">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="a0f70-135">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a0f70-135">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="a0f70-136">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a0f70-136">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

