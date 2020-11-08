---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
ms.openlocfilehash: d6964f076dd1e6882a8031f19101f55d19b9e4d4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103465"
---
# <span data-ttu-id="ab2a0-101">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ab2a0-101">New-AzSqlSyncGroup</span></span>

## <span data-ttu-id="ab2a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab2a0-102">SYNOPSIS</span></span>
<span data-ttu-id="ab2a0-103">Skapar en synkroniseringsresurs för Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="ab2a0-103">Creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="ab2a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab2a0-104">SYNTAX</span></span>

```
New-AzSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-UsePrivateLinkConnection] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab2a0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab2a0-105">DESCRIPTION</span></span>
<span data-ttu-id="ab2a0-106">Cmdleten **New-AzSqlSyncGroup** skapar en synkroniseringsresurs för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="ab2a0-106">The **New-AzSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="ab2a0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab2a0-107">EXAMPLES</span></span>

### <span data-ttu-id="ab2a0-108">Exempel 1: skapa en synkroniseringsresurs för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="ab2a0-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" -ConflictResolutionPolicy "HubWin"
-DatabaseCredential $credential -IntervalInSeconds 100 -SyncDatabaseServerName "syncDatabaseServer01" -SyncDatabaseName "syncDatabaseName01"
-SyncDatabaseResourceGroupName "syncDatabaseResourceGroup01" -Schema ".\schema.json" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="ab2a0-109">Det här kommandot skapar en synkroniseringsresurs för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="ab2a0-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="ab2a0-110">"schema.jsär en fil på den lokala hård disken.</span><span class="sxs-lookup"><span data-stu-id="ab2a0-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="ab2a0-111">Den innehåller schemats nytto Last i JSON-format.</span><span class="sxs-lookup"><span data-stu-id="ab2a0-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="ab2a0-112">Ett exempel på schema-JSON är: {"tabeller": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"kolumner": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}]; "MasterSyncMemberName": null}</span><span class="sxs-lookup"><span data-stu-id="ab2a0-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="ab2a0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab2a0-113">PARAMETERS</span></span>

### <span data-ttu-id="ab2a0-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="ab2a0-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="ab2a0-115">Principen för att lösa konflikter mellan nav och medlems databas i synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="ab2a0-115">The policy of resolving conflicts between hub and member database in the sync group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: HubWin, MemberWin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab2a0-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="ab2a0-116">-DatabaseCredential</span></span>
<span data-ttu-id="ab2a0-117">Autentiseringsuppgifter för SQL-autentisering för NAV databasen.</span><span class="sxs-lookup"><span data-stu-id="ab2a0-117">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="ab2a0-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ab2a0-118">-DatabaseName</span></span>
<span data-ttu-id="ab2a0-119">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="ab2a0-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="ab2a0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab2a0-120">-DefaultProfile</span></span>
<span data-ttu-id="ab2a0-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ab2a0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab2a0-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="ab2a0-122">-IntervalInSeconds</span></span>
<span data-ttu-id="ab2a0-123">Frekvens (i sekunder) vid synkronisering av data.</span><span class="sxs-lookup"><span data-stu-id="ab2a0-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="ab2a0-124">Standard är-1, vilket innebär att den automatiska synkroniseringen inte är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="ab2a0-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab2a0-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="ab2a0-125">-Name</span></span>
<span data-ttu-id="ab2a0-126">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="ab2a0-126">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab2a0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab2a0-127">-ResourceGroupName</span></span>
<span data-ttu-id="ab2a0-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ab2a0-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="ab2a0-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="ab2a0-129">-SchemaFile</span></span>
<span data-ttu-id="ab2a0-130">Sökvägen till schema filen.</span><span class="sxs-lookup"><span data-stu-id="ab2a0-130">The path of the schema file.</span></span>

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

### <span data-ttu-id="ab2a0-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ab2a0-131">-ServerName</span></span>
<span data-ttu-id="ab2a0-132">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ab2a0-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="ab2a0-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="ab2a0-133">-SyncDatabaseName</span></span>
<span data-ttu-id="ab2a0-134">Databasen som används för att lagra synkroniserade metadata.</span><span class="sxs-lookup"><span data-stu-id="ab2a0-134">The database used to store sync related metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab2a0-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab2a0-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="ab2a0-136">Den resurs grupp som databasen för synkade metadata tillhör.</span><span class="sxs-lookup"><span data-stu-id="ab2a0-136">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab2a0-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="ab2a0-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="ab2a0-138">Den server där databasen med synkrona data hanteras.</span><span class="sxs-lookup"><span data-stu-id="ab2a0-138">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab2a0-139">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="ab2a0-139">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="ab2a0-140">Använd en privat länk anslutning när du ansluter till navets grupp.</span><span class="sxs-lookup"><span data-stu-id="ab2a0-140">Use a private link connection when connecting to the hub of this sync group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab2a0-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ab2a0-141">-Confirm</span></span>
<span data-ttu-id="ab2a0-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ab2a0-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab2a0-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab2a0-143">-WhatIf</span></span>
<span data-ttu-id="ab2a0-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ab2a0-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab2a0-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ab2a0-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab2a0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab2a0-146">CommonParameters</span></span>
<span data-ttu-id="ab2a0-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab2a0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab2a0-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab2a0-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab2a0-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab2a0-149">INPUTS</span></span>

### <span data-ttu-id="ab2a0-150">System. String</span><span class="sxs-lookup"><span data-stu-id="ab2a0-150">System.String</span></span>

## <span data-ttu-id="ab2a0-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab2a0-151">OUTPUTS</span></span>

### <span data-ttu-id="ab2a0-152">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="ab2a0-152">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="ab2a0-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab2a0-153">NOTES</span></span>

## <span data-ttu-id="ab2a0-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab2a0-154">RELATED LINKS</span></span>

[<span data-ttu-id="ab2a0-155">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ab2a0-155">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="ab2a0-156">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ab2a0-156">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="ab2a0-157">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ab2a0-157">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

