---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: eff96559dce38bd1a78fa4e8c789c514ea7b93ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100770"
---
# <span data-ttu-id="b9fb4-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="b9fb4-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="b9fb4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b9fb4-102">SYNOPSIS</span></span>
<span data-ttu-id="b9fb4-103">Uppdaterar en synkroniserad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="b9fb4-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="b9fb4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b9fb4-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> [-MemberDatabaseCredential <PSCredential>]
 [-UsePrivateLinkConnection <Boolean>] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9fb4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b9fb4-105">DESCRIPTION</span></span>
<span data-ttu-id="b9fb4-106">Cmdleten **Update-AzSqlSyncGroup** ändrar egenskaper för en Azure SQL Database Sync-medlem.</span><span class="sxs-lookup"><span data-stu-id="b9fb4-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="b9fb4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b9fb4-107">EXAMPLES</span></span>

### <span data-ttu-id="b9fb4-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b9fb4-108">Example 1</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01"
-MemberDatabaseCredential $credential | Format-List
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
MemberDatabaseUserName      : myAccount-new
MemberDatabasePassword      : 
SyncState                   : Good
```

<span data-ttu-id="b9fb4-109">Det här kommandot återställer administratörs lösen ordet för medlems databasen.</span><span class="sxs-lookup"><span data-stu-id="b9fb4-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="b9fb4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b9fb4-110">PARAMETERS</span></span>

### <span data-ttu-id="b9fb4-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b9fb4-111">-DatabaseName</span></span>
<span data-ttu-id="b9fb4-112">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="b9fb4-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="b9fb4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9fb4-113">-DefaultProfile</span></span>
<span data-ttu-id="b9fb4-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b9fb4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9fb4-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="b9fb4-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="b9fb4-116">Autentiseringsuppgifterna (användar namn och lösen ord) för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="b9fb4-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9fb4-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="b9fb4-117">-Name</span></span>
<span data-ttu-id="b9fb4-118">Synkroniserat medlems namn.</span><span class="sxs-lookup"><span data-stu-id="b9fb4-118">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9fb4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9fb4-119">-ResourceGroupName</span></span>
<span data-ttu-id="b9fb4-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b9fb4-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="b9fb4-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b9fb4-121">-ServerName</span></span>
<span data-ttu-id="b9fb4-122">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b9fb4-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="b9fb4-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="b9fb4-123">-SyncGroupName</span></span>
<span data-ttu-id="b9fb4-124">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="b9fb4-124">The sync group name.</span></span>

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

### <span data-ttu-id="b9fb4-125">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="b9fb4-125">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="b9fb4-126">Resurs-ID för den synkroniserade medlems databasen, används om UsePrivateLinkConnection är inställt på True.</span><span class="sxs-lookup"><span data-stu-id="b9fb4-126">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9fb4-127">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="b9fb4-127">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="b9fb4-128">Om du vill använda privat länk när du ansluter till den här synkroniserade medlemmen.</span><span class="sxs-lookup"><span data-stu-id="b9fb4-128">Whether to use private link when connecting to this sync member.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9fb4-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b9fb4-129">-Confirm</span></span>
<span data-ttu-id="b9fb4-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b9fb4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9fb4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9fb4-131">-WhatIf</span></span>
<span data-ttu-id="b9fb4-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b9fb4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9fb4-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b9fb4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9fb4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9fb4-134">CommonParameters</span></span>
<span data-ttu-id="b9fb4-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9fb4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9fb4-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9fb4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9fb4-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b9fb4-137">INPUTS</span></span>

### <span data-ttu-id="b9fb4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b9fb4-138">System.String</span></span>

## <span data-ttu-id="b9fb4-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b9fb4-139">OUTPUTS</span></span>

### <span data-ttu-id="b9fb4-140">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="b9fb4-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="b9fb4-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b9fb4-141">NOTES</span></span>

## <span data-ttu-id="b9fb4-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b9fb4-142">RELATED LINKS</span></span>

[<span data-ttu-id="b9fb4-143">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="b9fb4-143">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="b9fb4-144">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="b9fb4-144">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="b9fb4-145">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="b9fb4-145">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)
