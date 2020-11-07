---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: 1decf3d7b179123a116bb570199840118115313f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926382"
---
# <span data-ttu-id="f43b7-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f43b7-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="f43b7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f43b7-102">SYNOPSIS</span></span>
<span data-ttu-id="f43b7-103">Skapar en synkroniserad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="f43b7-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="f43b7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f43b7-104">SYNTAX</span></span>

### <span data-ttu-id="f43b7-105">AzureSqlDatabase (standard)</span><span class="sxs-lookup"><span data-stu-id="f43b7-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f43b7-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="f43b7-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f43b7-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="f43b7-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f43b7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f43b7-108">DESCRIPTION</span></span>
<span data-ttu-id="f43b7-109">Cmdleten **New-AzSqlSyncMember** skapar en Sync-medlem för Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="f43b7-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="f43b7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f43b7-110">EXAMPLES</span></span>

### <span data-ttu-id="f43b7-111">Exempel 1: skapa en synkroniserad medlem för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="f43b7-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
-MemberDatabaseType "AzureSqlDatabase" -MemberServerName "memberServer01.full.dns.name" -MemberDatabaseName "memberDatabase01" -MemberDatabaseCredential $credential | Format-List
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
SyncState                   : UnProvisioned
```

<span data-ttu-id="f43b7-112">Det här kommandot skapar en synkronisera medlem för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="f43b7-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="f43b7-113">Exempel 2: skapa en synkroniserad medlem för en lokal SQL Server-databas</span><span class="sxs-lookup"><span data-stu-id="f43b7-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
-MemberDatabaseType "SqlServerDatabase" -SqlServerDatabaseId "dbId" -syncAgentResourceGroupName "syncAgentResourceGroupName" -syncAgentServerName "syncAgentServerName" 
-syncAgentDatabaseName "syncAgentDatabaseName" -syncAgentName "agentName" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : /subscriptions/{subscriptionId}/resourceGroups/{syncAgentResourceGroupName}/servers/{syncAgentServerName}/syncAgents/{syncAgentId}
SqlServerDatabaseId         : dbId
MemberServerName            : 
MemberDatabaseName          : 
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : UnProvisioned
```

<span data-ttu-id="f43b7-114">Det här kommandot skapar en synkronisera medlem för en lokal SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="f43b7-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="f43b7-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f43b7-115">PARAMETERS</span></span>

### <span data-ttu-id="f43b7-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f43b7-116">-DatabaseName</span></span>
<span data-ttu-id="f43b7-117">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="f43b7-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="f43b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f43b7-118">-DefaultProfile</span></span>
<span data-ttu-id="f43b7-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f43b7-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f43b7-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="f43b7-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="f43b7-121">Autentiseringsuppgifterna (användar namn och lösen ord) för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="f43b7-121">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f43b7-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="f43b7-122">-MemberDatabaseName</span></span>
<span data-ttu-id="f43b7-123">Namn på medlems databasen i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="f43b7-123">The Azure SQL Database name of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f43b7-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="f43b7-124">-MemberDatabaseType</span></span>
<span data-ttu-id="f43b7-125">Databas typen för medlems databasen.</span><span class="sxs-lookup"><span data-stu-id="f43b7-125">The database type of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SqlServerDatabase, AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f43b7-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="f43b7-126">-MemberServerName</span></span>
<span data-ttu-id="f43b7-127">Namn på medlems databasen för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f43b7-127">The Azure SQL Server Name of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f43b7-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="f43b7-128">-Name</span></span>
<span data-ttu-id="f43b7-129">Synkroniserat medlems namn.</span><span class="sxs-lookup"><span data-stu-id="f43b7-129">The sync member name.</span></span>

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

### <span data-ttu-id="f43b7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f43b7-130">-ResourceGroupName</span></span>
<span data-ttu-id="f43b7-131">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f43b7-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="f43b7-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f43b7-132">-ServerName</span></span>
<span data-ttu-id="f43b7-133">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f43b7-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="f43b7-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="f43b7-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="f43b7-135">ID för SQL Server-databasen som är ansluten av synkroniseringsklienten.</span><span class="sxs-lookup"><span data-stu-id="f43b7-135">The id of the SQL server database which is connected by the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent, OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f43b7-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="f43b7-136">-SyncAgentName</span></span>
<span data-ttu-id="f43b7-137">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="f43b7-137">The name of the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f43b7-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f43b7-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="f43b7-139">Namnet på resurs gruppen där synkroniseringsresursen finns.</span><span class="sxs-lookup"><span data-stu-id="f43b7-139">The name of the resource group where the sync agent is under.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f43b7-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="f43b7-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="f43b7-141">Resurs-ID för synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="f43b7-141">The resource ID of the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f43b7-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="f43b7-142">-SyncAgentServerName</span></span>
<span data-ttu-id="f43b7-143">Namnet på den Azure SQL-Server där synkroniseringsresursen finns.</span><span class="sxs-lookup"><span data-stu-id="f43b7-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f43b7-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="f43b7-144">-SyncDirection</span></span>
<span data-ttu-id="f43b7-145">Synkroniseringens synkroniseringsstatus.</span><span class="sxs-lookup"><span data-stu-id="f43b7-145">The sync direction of this sync member.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Bidirectional, OneWayMemberToHub, OneWayHubToMember

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f43b7-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="f43b7-146">-SyncGroupName</span></span>
<span data-ttu-id="f43b7-147">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="f43b7-147">The sync group name.</span></span>

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

### <span data-ttu-id="f43b7-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f43b7-148">-Confirm</span></span>
<span data-ttu-id="f43b7-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f43b7-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f43b7-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f43b7-150">-WhatIf</span></span>
<span data-ttu-id="f43b7-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f43b7-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f43b7-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f43b7-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f43b7-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f43b7-153">CommonParameters</span></span>
<span data-ttu-id="f43b7-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f43b7-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f43b7-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f43b7-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f43b7-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f43b7-156">INPUTS</span></span>

### <span data-ttu-id="f43b7-157">System. String</span><span class="sxs-lookup"><span data-stu-id="f43b7-157">System.String</span></span>

## <span data-ttu-id="f43b7-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f43b7-158">OUTPUTS</span></span>

### <span data-ttu-id="f43b7-159">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="f43b7-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="f43b7-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f43b7-160">NOTES</span></span>

## <span data-ttu-id="f43b7-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f43b7-161">RELATED LINKS</span></span>

[<span data-ttu-id="f43b7-162">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f43b7-162">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="f43b7-163">Set-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f43b7-163">Set-AzSqlSyncMember</span></span>](./Set-AzSqlSyncMember.md)

[<span data-ttu-id="f43b7-164">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f43b7-164">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

