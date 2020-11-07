---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
ms.openlocfilehash: f72091d142b57cc7ef3897eceda2219634376daf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756323"
---
# <span data-ttu-id="917ae-101">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="917ae-101">Update-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="917ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="917ae-102">SYNOPSIS</span></span>
<span data-ttu-id="917ae-103">Uppdaterar en synkroniserad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="917ae-103">Updates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="917ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="917ae-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="917ae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="917ae-105">DESCRIPTION</span></span>
<span data-ttu-id="917ae-106">Cmdleten **Update-AzureRmSqlSyncGroup** ändrar egenskaper för en Azure SQL Database Sync-medlem.</span><span class="sxs-lookup"><span data-stu-id="917ae-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="917ae-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="917ae-107">EXAMPLES</span></span>

### <span data-ttu-id="917ae-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="917ae-108">Example 1</span></span>
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

<span data-ttu-id="917ae-109">Det här kommandot återställer administratörs lösen ordet för medlems databasen.</span><span class="sxs-lookup"><span data-stu-id="917ae-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="917ae-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="917ae-110">PARAMETERS</span></span>

### <span data-ttu-id="917ae-111">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="917ae-111">-Confirm</span></span>
<span data-ttu-id="917ae-112">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="917ae-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="917ae-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="917ae-113">-DatabaseName</span></span>
<span data-ttu-id="917ae-114">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="917ae-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="917ae-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="917ae-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="917ae-116">Autentiseringsuppgifterna (användar namn och lösen ord) för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="917ae-116">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="917ae-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="917ae-117">-Name</span></span>
<span data-ttu-id="917ae-118">Synkroniserat medlems namn.</span><span class="sxs-lookup"><span data-stu-id="917ae-118">The sync member name.</span></span>

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

### <span data-ttu-id="917ae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="917ae-119">-ResourceGroupName</span></span>
<span data-ttu-id="917ae-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="917ae-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="917ae-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="917ae-121">-ServerName</span></span>
<span data-ttu-id="917ae-122">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="917ae-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="917ae-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="917ae-123">-SyncGroupName</span></span>
<span data-ttu-id="917ae-124">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="917ae-124">The sync group name.</span></span>

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

### <span data-ttu-id="917ae-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="917ae-125">-WhatIf</span></span>
<span data-ttu-id="917ae-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="917ae-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="917ae-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="917ae-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="917ae-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="917ae-128">-DefaultProfile</span></span>
<span data-ttu-id="917ae-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="917ae-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="917ae-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="917ae-130">CommonParameters</span></span>
<span data-ttu-id="917ae-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="917ae-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="917ae-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="917ae-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="917ae-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="917ae-133">INPUTS</span></span>

## <span data-ttu-id="917ae-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="917ae-134">OUTPUTS</span></span>

### <span data-ttu-id="917ae-135">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="917ae-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="917ae-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="917ae-136">NOTES</span></span>

## <span data-ttu-id="917ae-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="917ae-137">RELATED LINKS</span></span>

[<span data-ttu-id="917ae-138">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="917ae-138">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="917ae-139">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="917ae-139">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="917ae-140">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="917ae-140">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

