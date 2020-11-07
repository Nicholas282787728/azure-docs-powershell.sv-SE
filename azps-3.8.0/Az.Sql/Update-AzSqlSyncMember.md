---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: 634ce84e355dbd106865b0f1072b693bd03a623b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927013"
---
# <span data-ttu-id="f6536-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f6536-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="f6536-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6536-102">SYNOPSIS</span></span>
<span data-ttu-id="f6536-103">Uppdaterar en synkroniserad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="f6536-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="f6536-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6536-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6536-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6536-105">DESCRIPTION</span></span>
<span data-ttu-id="f6536-106">Cmdleten **Update-AzSqlSyncGroup** ändrar egenskaper för en Azure SQL Database Sync-medlem.</span><span class="sxs-lookup"><span data-stu-id="f6536-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="f6536-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6536-107">EXAMPLES</span></span>

### <span data-ttu-id="f6536-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f6536-108">Example 1</span></span>
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

<span data-ttu-id="f6536-109">Det här kommandot återställer administratörs lösen ordet för medlems databasen.</span><span class="sxs-lookup"><span data-stu-id="f6536-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="f6536-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6536-110">PARAMETERS</span></span>

### <span data-ttu-id="f6536-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f6536-111">-DatabaseName</span></span>
<span data-ttu-id="f6536-112">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="f6536-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="f6536-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6536-113">-DefaultProfile</span></span>
<span data-ttu-id="f6536-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f6536-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6536-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="f6536-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="f6536-116">Autentiseringsuppgifterna (användar namn och lösen ord) för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="f6536-116">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="f6536-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="f6536-117">-Name</span></span>
<span data-ttu-id="f6536-118">Synkroniserat medlems namn.</span><span class="sxs-lookup"><span data-stu-id="f6536-118">The sync member name.</span></span>

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

### <span data-ttu-id="f6536-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6536-119">-ResourceGroupName</span></span>
<span data-ttu-id="f6536-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f6536-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="f6536-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f6536-121">-ServerName</span></span>
<span data-ttu-id="f6536-122">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f6536-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="f6536-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="f6536-123">-SyncGroupName</span></span>
<span data-ttu-id="f6536-124">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="f6536-124">The sync group name.</span></span>

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

### <span data-ttu-id="f6536-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f6536-125">-Confirm</span></span>
<span data-ttu-id="f6536-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f6536-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6536-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6536-127">-WhatIf</span></span>
<span data-ttu-id="f6536-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f6536-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6536-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f6536-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6536-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6536-130">CommonParameters</span></span>
<span data-ttu-id="f6536-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6536-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6536-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6536-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6536-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6536-133">INPUTS</span></span>

### <span data-ttu-id="f6536-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f6536-134">System.String</span></span>

## <span data-ttu-id="f6536-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6536-135">OUTPUTS</span></span>

### <span data-ttu-id="f6536-136">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="f6536-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="f6536-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6536-137">NOTES</span></span>

## <span data-ttu-id="f6536-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6536-138">RELATED LINKS</span></span>

[<span data-ttu-id="f6536-139">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f6536-139">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="f6536-140">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f6536-140">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="f6536-141">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f6536-141">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

