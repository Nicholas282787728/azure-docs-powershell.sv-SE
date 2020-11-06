---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/update-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
ms.openlocfilehash: afaa0446b46fca343b4d53ae491c67ef1ceb923a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581916"
---
# <span data-ttu-id="a4732-101">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a4732-101">Update-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="a4732-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4732-102">SYNOPSIS</span></span>
<span data-ttu-id="a4732-103">Uppdaterar en synkroniserad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="a4732-103">Updates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4732-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4732-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4732-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4732-105">DESCRIPTION</span></span>
<span data-ttu-id="a4732-106">Cmdleten **Update-AzureRmSqlSyncGroup** ändrar egenskaper för en Azure SQL Database Sync-medlem.</span><span class="sxs-lookup"><span data-stu-id="a4732-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="a4732-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4732-107">EXAMPLES</span></span>

### <span data-ttu-id="a4732-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a4732-108">Example 1</span></span>
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

<span data-ttu-id="a4732-109">Det här kommandot återställer administratörs lösen ordet för medlems databasen.</span><span class="sxs-lookup"><span data-stu-id="a4732-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="a4732-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4732-110">PARAMETERS</span></span>

### <span data-ttu-id="a4732-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a4732-111">-DatabaseName</span></span>
<span data-ttu-id="a4732-112">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="a4732-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a4732-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4732-113">-DefaultProfile</span></span>
<span data-ttu-id="a4732-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a4732-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4732-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="a4732-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="a4732-116">Autentiseringsuppgifterna (användar namn och lösen ord) för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="a4732-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4732-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="a4732-117">-Name</span></span>
<span data-ttu-id="a4732-118">Synkroniserat medlems namn.</span><span class="sxs-lookup"><span data-stu-id="a4732-118">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4732-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4732-119">-ResourceGroupName</span></span>
<span data-ttu-id="a4732-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a4732-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="a4732-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a4732-121">-ServerName</span></span>
<span data-ttu-id="a4732-122">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a4732-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="a4732-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a4732-123">-SyncGroupName</span></span>
<span data-ttu-id="a4732-124">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="a4732-124">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4732-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a4732-125">-Confirm</span></span>
<span data-ttu-id="a4732-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a4732-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4732-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4732-127">-WhatIf</span></span>
<span data-ttu-id="a4732-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a4732-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4732-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a4732-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4732-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4732-130">CommonParameters</span></span>
<span data-ttu-id="a4732-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4732-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4732-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4732-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4732-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4732-133">INPUTS</span></span>

### <span data-ttu-id="a4732-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="a4732-134">None</span></span>
<span data-ttu-id="a4732-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="a4732-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a4732-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4732-136">OUTPUTS</span></span>

### <span data-ttu-id="a4732-137">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="a4732-137">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="a4732-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4732-138">NOTES</span></span>

## <span data-ttu-id="a4732-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4732-139">RELATED LINKS</span></span>

[<span data-ttu-id="a4732-140">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a4732-140">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="a4732-141">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a4732-141">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="a4732-142">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a4732-142">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

