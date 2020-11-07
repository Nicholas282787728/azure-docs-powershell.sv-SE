---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: 76b7366dabc648dc7f5812aedcc7fef18437b68e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920712"
---
# <span data-ttu-id="decad-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="decad-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="decad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="decad-102">SYNOPSIS</span></span>
<span data-ttu-id="decad-103">Uppdaterar en synkroniserad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="decad-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="decad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="decad-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="decad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="decad-105">DESCRIPTION</span></span>
<span data-ttu-id="decad-106">Cmdleten **Update-AzSqlSyncGroup** ändrar egenskaper för en Azure SQL Database Sync-medlem.</span><span class="sxs-lookup"><span data-stu-id="decad-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="decad-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="decad-107">EXAMPLES</span></span>

### <span data-ttu-id="decad-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="decad-108">Example 1</span></span>
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

<span data-ttu-id="decad-109">Det här kommandot återställer administratörs lösen ordet för medlems databasen.</span><span class="sxs-lookup"><span data-stu-id="decad-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="decad-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="decad-110">PARAMETERS</span></span>

### <span data-ttu-id="decad-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="decad-111">-DatabaseName</span></span>
<span data-ttu-id="decad-112">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="decad-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="decad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="decad-113">-DefaultProfile</span></span>
<span data-ttu-id="decad-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="decad-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="decad-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="decad-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="decad-116">Autentiseringsuppgifterna (användar namn och lösen ord) för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="decad-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decad-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="decad-117">-Name</span></span>
<span data-ttu-id="decad-118">Synkroniserat medlems namn.</span><span class="sxs-lookup"><span data-stu-id="decad-118">The sync member name.</span></span>

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

### <span data-ttu-id="decad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="decad-119">-ResourceGroupName</span></span>
<span data-ttu-id="decad-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="decad-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="decad-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="decad-121">-ServerName</span></span>
<span data-ttu-id="decad-122">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="decad-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="decad-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="decad-123">-SyncGroupName</span></span>
<span data-ttu-id="decad-124">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="decad-124">The sync group name.</span></span>

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

### <span data-ttu-id="decad-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="decad-125">-Confirm</span></span>
<span data-ttu-id="decad-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="decad-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="decad-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="decad-127">-WhatIf</span></span>
<span data-ttu-id="decad-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="decad-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="decad-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="decad-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="decad-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="decad-130">CommonParameters</span></span>
<span data-ttu-id="decad-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="decad-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="decad-132">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="decad-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="decad-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="decad-133">INPUTS</span></span>

### <span data-ttu-id="decad-134">System. String</span><span class="sxs-lookup"><span data-stu-id="decad-134">System.String</span></span>

## <span data-ttu-id="decad-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="decad-135">OUTPUTS</span></span>

### <span data-ttu-id="decad-136">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="decad-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="decad-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="decad-137">NOTES</span></span>

## <span data-ttu-id="decad-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="decad-138">RELATED LINKS</span></span>

[<span data-ttu-id="decad-139">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="decad-139">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="decad-140">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="decad-140">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="decad-141">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="decad-141">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

