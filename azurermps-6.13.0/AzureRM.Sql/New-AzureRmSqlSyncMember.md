---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncMember.md
ms.openlocfilehash: a779217b67cc73f25223661ae8671b4588a8cd2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578768"
---
# <span data-ttu-id="3d964-101">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="3d964-101">New-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="3d964-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d964-102">SYNOPSIS</span></span>
<span data-ttu-id="3d964-103">Skapar en synkroniserad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="3d964-103">Creates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d964-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d964-104">SYNTAX</span></span>

### <span data-ttu-id="3d964-105">AzureSqlDatabase (standard)</span><span class="sxs-lookup"><span data-stu-id="3d964-105">AzureSqlDatabase (Default)</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d964-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="3d964-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d964-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="3d964-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d964-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d964-108">DESCRIPTION</span></span>
<span data-ttu-id="3d964-109">Cmdleten **New-AzureRmSqlSyncMember** skapar en Sync-medlem för Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="3d964-109">The **New-AzureRmSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="3d964-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d964-110">EXAMPLES</span></span>

### <span data-ttu-id="3d964-111">Exempel 1: skapa en synkroniserad medlem för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="3d964-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
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

<span data-ttu-id="3d964-112">Det här kommandot skapar en synkronisera medlem för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="3d964-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="3d964-113">Exempel 2: skapa en synkroniserad medlem för en lokal SQL Server-databas</span><span class="sxs-lookup"><span data-stu-id="3d964-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
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

<span data-ttu-id="3d964-114">Det här kommandot skapar en synkronisera medlem för en lokal SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="3d964-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="3d964-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d964-115">PARAMETERS</span></span>

### <span data-ttu-id="3d964-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3d964-116">-DatabaseName</span></span>
<span data-ttu-id="3d964-117">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="3d964-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="3d964-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d964-118">-DefaultProfile</span></span>
<span data-ttu-id="3d964-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3d964-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d964-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="3d964-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="3d964-121">Autentiseringsuppgifterna (användar namn och lösen ord) för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="3d964-121">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="3d964-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="3d964-122">-MemberDatabaseName</span></span>
<span data-ttu-id="3d964-123">Namn på medlems databasen i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="3d964-123">The Azure SQL Database name of the member database.</span></span>

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

### <span data-ttu-id="3d964-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="3d964-124">-MemberDatabaseType</span></span>
<span data-ttu-id="3d964-125">Databas typen för medlems databasen.</span><span class="sxs-lookup"><span data-stu-id="3d964-125">The database type of the member database.</span></span>

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

### <span data-ttu-id="3d964-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="3d964-126">-MemberServerName</span></span>
<span data-ttu-id="3d964-127">Namn på medlems databasen för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3d964-127">The Azure SQL Server Name of the member database.</span></span>

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

### <span data-ttu-id="3d964-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="3d964-128">-Name</span></span>
<span data-ttu-id="3d964-129">Synkroniserat medlems namn.</span><span class="sxs-lookup"><span data-stu-id="3d964-129">The sync member name.</span></span>

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

### <span data-ttu-id="3d964-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d964-130">-ResourceGroupName</span></span>
<span data-ttu-id="3d964-131">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3d964-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="3d964-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3d964-132">-ServerName</span></span>
<span data-ttu-id="3d964-133">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3d964-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="3d964-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="3d964-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="3d964-135">ID för SQL Server-databasen som är ansluten av synkroniseringsklienten.</span><span class="sxs-lookup"><span data-stu-id="3d964-135">The id of the SQL server database which is connected by the sync agent.</span></span>

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

### <span data-ttu-id="3d964-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="3d964-136">-SyncAgentName</span></span>
<span data-ttu-id="3d964-137">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="3d964-137">The name of the sync agent.</span></span>

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

### <span data-ttu-id="3d964-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d964-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="3d964-139">Namnet på resurs gruppen där synkroniseringsresursen finns.</span><span class="sxs-lookup"><span data-stu-id="3d964-139">The name of the resource group where the sync agent is under.</span></span>

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

### <span data-ttu-id="3d964-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="3d964-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="3d964-141">Resurs-ID för synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="3d964-141">The resource ID of the sync agent.</span></span>

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

### <span data-ttu-id="3d964-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="3d964-142">-SyncAgentServerName</span></span>
<span data-ttu-id="3d964-143">Namnet på den Azure SQL-Server där synkroniseringsresursen finns.</span><span class="sxs-lookup"><span data-stu-id="3d964-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

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

### <span data-ttu-id="3d964-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="3d964-144">-SyncDirection</span></span>
<span data-ttu-id="3d964-145">Synkroniseringens synkroniseringsstatus.</span><span class="sxs-lookup"><span data-stu-id="3d964-145">The sync direction of this sync member.</span></span>

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

### <span data-ttu-id="3d964-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="3d964-146">-SyncGroupName</span></span>
<span data-ttu-id="3d964-147">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="3d964-147">The sync group name.</span></span>

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

### <span data-ttu-id="3d964-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3d964-148">-Confirm</span></span>
<span data-ttu-id="3d964-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d964-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d964-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d964-150">-WhatIf</span></span>
<span data-ttu-id="3d964-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3d964-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d964-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3d964-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d964-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d964-153">CommonParameters</span></span>
<span data-ttu-id="3d964-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d964-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d964-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d964-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d964-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d964-156">INPUTS</span></span>

### <span data-ttu-id="3d964-157">System. String</span><span class="sxs-lookup"><span data-stu-id="3d964-157">System.String</span></span>

## <span data-ttu-id="3d964-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d964-158">OUTPUTS</span></span>

### <span data-ttu-id="3d964-159">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="3d964-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="3d964-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d964-160">NOTES</span></span>

## <span data-ttu-id="3d964-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d964-161">RELATED LINKS</span></span>

[<span data-ttu-id="3d964-162">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="3d964-162">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="3d964-163">Set-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="3d964-163">Set-AzureRmSqlSyncMember</span></span>](./Set-AzureRmSqlSyncMember.md)

[<span data-ttu-id="3d964-164">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="3d964-164">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)
