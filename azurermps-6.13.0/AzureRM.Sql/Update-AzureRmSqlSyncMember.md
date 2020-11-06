---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/update-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
ms.openlocfilehash: 7737baa8459cc9acae86cbd3e632dd73f9433056
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583403"
---
# <span data-ttu-id="52cb9-101">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="52cb9-101">Update-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="52cb9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52cb9-102">SYNOPSIS</span></span>
<span data-ttu-id="52cb9-103">Uppdaterar en synkroniserad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="52cb9-103">Updates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52cb9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52cb9-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52cb9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52cb9-105">DESCRIPTION</span></span>
<span data-ttu-id="52cb9-106">Cmdleten **Update-AzureRmSqlSyncGroup** ändrar egenskaper för en Azure SQL Database Sync-medlem.</span><span class="sxs-lookup"><span data-stu-id="52cb9-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="52cb9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52cb9-107">EXAMPLES</span></span>

### <span data-ttu-id="52cb9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="52cb9-108">Example 1</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01"
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

<span data-ttu-id="52cb9-109">Det här kommandot återställer administratörs lösen ordet för medlems databasen.</span><span class="sxs-lookup"><span data-stu-id="52cb9-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="52cb9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52cb9-110">PARAMETERS</span></span>

### <span data-ttu-id="52cb9-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="52cb9-111">-DatabaseName</span></span>
<span data-ttu-id="52cb9-112">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="52cb9-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="52cb9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52cb9-113">-DefaultProfile</span></span>
<span data-ttu-id="52cb9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="52cb9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52cb9-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="52cb9-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="52cb9-116">Autentiseringsuppgifterna (användar namn och lösen ord) för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="52cb9-116">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="52cb9-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="52cb9-117">-Name</span></span>
<span data-ttu-id="52cb9-118">Synkroniserat medlems namn.</span><span class="sxs-lookup"><span data-stu-id="52cb9-118">The sync member name.</span></span>

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

### <span data-ttu-id="52cb9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52cb9-119">-ResourceGroupName</span></span>
<span data-ttu-id="52cb9-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="52cb9-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="52cb9-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="52cb9-121">-ServerName</span></span>
<span data-ttu-id="52cb9-122">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="52cb9-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="52cb9-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="52cb9-123">-SyncGroupName</span></span>
<span data-ttu-id="52cb9-124">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="52cb9-124">The sync group name.</span></span>

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

### <span data-ttu-id="52cb9-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="52cb9-125">-Confirm</span></span>
<span data-ttu-id="52cb9-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="52cb9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52cb9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52cb9-127">-WhatIf</span></span>
<span data-ttu-id="52cb9-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="52cb9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52cb9-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="52cb9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52cb9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52cb9-130">CommonParameters</span></span>
<span data-ttu-id="52cb9-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52cb9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52cb9-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52cb9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52cb9-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52cb9-133">INPUTS</span></span>

### <span data-ttu-id="52cb9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="52cb9-134">System.String</span></span>

## <span data-ttu-id="52cb9-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52cb9-135">OUTPUTS</span></span>

### <span data-ttu-id="52cb9-136">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="52cb9-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="52cb9-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52cb9-137">NOTES</span></span>

## <span data-ttu-id="52cb9-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52cb9-138">RELATED LINKS</span></span>

[<span data-ttu-id="52cb9-139">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="52cb9-139">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="52cb9-140">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="52cb9-140">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="52cb9-141">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="52cb9-141">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

