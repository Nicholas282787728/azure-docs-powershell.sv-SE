---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: 503f7be9d4d7f595ac8d337568038d7e7e724d1f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920560"
---
# <span data-ttu-id="3290d-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="3290d-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="3290d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3290d-102">SYNOPSIS</span></span>
<span data-ttu-id="3290d-103">Skapar en synkroniserad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="3290d-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="3290d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3290d-104">SYNTAX</span></span>

### <span data-ttu-id="3290d-105">AzureSqlDatabase (standard)</span><span class="sxs-lookup"><span data-stu-id="3290d-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3290d-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="3290d-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3290d-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="3290d-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3290d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3290d-108">DESCRIPTION</span></span>
<span data-ttu-id="3290d-109">Cmdleten **New-AzSqlSyncMember** skapar en Sync-medlem för Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="3290d-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="3290d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3290d-110">EXAMPLES</span></span>

### <span data-ttu-id="3290d-111">Exempel 1: skapa en synkroniserad medlem för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="3290d-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
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

<span data-ttu-id="3290d-112">Det här kommandot skapar en synkronisera medlem för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="3290d-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="3290d-113">Exempel 2: skapa en synkroniserad medlem för en lokal SQL Server-databas</span><span class="sxs-lookup"><span data-stu-id="3290d-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
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

<span data-ttu-id="3290d-114">Det här kommandot skapar en synkronisera medlem för en lokal SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="3290d-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="3290d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3290d-115">PARAMETERS</span></span>

### <span data-ttu-id="3290d-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3290d-116">-DatabaseName</span></span>
<span data-ttu-id="3290d-117">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="3290d-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="3290d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3290d-118">-DefaultProfile</span></span>
<span data-ttu-id="3290d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3290d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3290d-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="3290d-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="3290d-121">Autentiseringsuppgifterna (användar namn och lösen ord) för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="3290d-121">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="3290d-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="3290d-122">-MemberDatabaseName</span></span>
<span data-ttu-id="3290d-123">Namn på medlems databasen i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="3290d-123">The Azure SQL Database name of the member database.</span></span>

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

### <span data-ttu-id="3290d-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="3290d-124">-MemberDatabaseType</span></span>
<span data-ttu-id="3290d-125">Databas typen för medlems databasen.</span><span class="sxs-lookup"><span data-stu-id="3290d-125">The database type of the member database.</span></span>

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

### <span data-ttu-id="3290d-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="3290d-126">-MemberServerName</span></span>
<span data-ttu-id="3290d-127">Namn på medlems databasen för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3290d-127">The Azure SQL Server Name of the member database.</span></span>

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

### <span data-ttu-id="3290d-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="3290d-128">-Name</span></span>
<span data-ttu-id="3290d-129">Synkroniserat medlems namn.</span><span class="sxs-lookup"><span data-stu-id="3290d-129">The sync member name.</span></span>

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

### <span data-ttu-id="3290d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3290d-130">-ResourceGroupName</span></span>
<span data-ttu-id="3290d-131">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3290d-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="3290d-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3290d-132">-ServerName</span></span>
<span data-ttu-id="3290d-133">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3290d-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="3290d-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="3290d-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="3290d-135">ID för SQL Server-databasen som är ansluten av synkroniseringsklienten.</span><span class="sxs-lookup"><span data-stu-id="3290d-135">The id of the SQL server database which is connected by the sync agent.</span></span>

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

### <span data-ttu-id="3290d-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="3290d-136">-SyncAgentName</span></span>
<span data-ttu-id="3290d-137">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="3290d-137">The name of the sync agent.</span></span>

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

### <span data-ttu-id="3290d-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3290d-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="3290d-139">Namnet på resurs gruppen där synkroniseringsresursen finns.</span><span class="sxs-lookup"><span data-stu-id="3290d-139">The name of the resource group where the sync agent is under.</span></span>

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

### <span data-ttu-id="3290d-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="3290d-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="3290d-141">Resurs-ID för synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="3290d-141">The resource ID of the sync agent.</span></span>

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

### <span data-ttu-id="3290d-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="3290d-142">-SyncAgentServerName</span></span>
<span data-ttu-id="3290d-143">Namnet på den Azure SQL-Server där synkroniseringsresursen finns.</span><span class="sxs-lookup"><span data-stu-id="3290d-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

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

### <span data-ttu-id="3290d-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="3290d-144">-SyncDirection</span></span>
<span data-ttu-id="3290d-145">Synkroniseringens synkroniseringsstatus.</span><span class="sxs-lookup"><span data-stu-id="3290d-145">The sync direction of this sync member.</span></span>

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

### <span data-ttu-id="3290d-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="3290d-146">-SyncGroupName</span></span>
<span data-ttu-id="3290d-147">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="3290d-147">The sync group name.</span></span>

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

### <span data-ttu-id="3290d-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3290d-148">-Confirm</span></span>
<span data-ttu-id="3290d-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3290d-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3290d-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3290d-150">-WhatIf</span></span>
<span data-ttu-id="3290d-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3290d-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3290d-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3290d-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3290d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3290d-153">CommonParameters</span></span>
<span data-ttu-id="3290d-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3290d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3290d-155">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3290d-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3290d-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3290d-156">INPUTS</span></span>

### <span data-ttu-id="3290d-157">System. String</span><span class="sxs-lookup"><span data-stu-id="3290d-157">System.String</span></span>

## <span data-ttu-id="3290d-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3290d-158">OUTPUTS</span></span>

### <span data-ttu-id="3290d-159">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="3290d-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="3290d-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3290d-160">NOTES</span></span>

## <span data-ttu-id="3290d-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3290d-161">RELATED LINKS</span></span>

[<span data-ttu-id="3290d-162">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="3290d-162">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="3290d-163">Set-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="3290d-163">Set-AzSqlSyncMember</span></span>](./Set-AzSqlSyncMember.md)

[<span data-ttu-id="3290d-164">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="3290d-164">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

