---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
ms.openlocfilehash: 9c4a6572a5a2025bba23758160378519524b8ce7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393040"
---
# <span data-ttu-id="e02a8-101">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e02a8-101">Update-AzSqlSyncGroup</span></span>

## <span data-ttu-id="e02a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e02a8-102">SYNOPSIS</span></span>
<span data-ttu-id="e02a8-103">Uppdaterar en synkroniseringsresurs för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="e02a8-103">Updates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="e02a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e02a8-104">SYNTAX</span></span>

```
Update-AzSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-UsePrivateLinkConnection <Boolean>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e02a8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e02a8-105">DESCRIPTION</span></span>
<span data-ttu-id="e02a8-106">Cmdleten **Update-AzSqlSyncGroup** ändrar egenskaperna för en synkroniseringsresurs för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="e02a8-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="e02a8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e02a8-107">EXAMPLES</span></span>

### <span data-ttu-id="e02a8-108">Exempel 1: uppdatera en synkroniseringsresurs för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="e02a8-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01"
-DatabaseCredential $credential -IntervalInSeconds 100 -Schema ".\schema.json" | Format-List
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

<span data-ttu-id="e02a8-109">Det här kommandot uppdaterar en synkroniseringsresurs för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="e02a8-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="e02a8-110">"schema.jsär en fil på den lokala hård disken.</span><span class="sxs-lookup"><span data-stu-id="e02a8-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="e02a8-111">Den innehåller schemats nytto Last i JSON-format.</span><span class="sxs-lookup"><span data-stu-id="e02a8-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="e02a8-112">Ett exempel på schema-JSON är: {"tabeller": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"kolumner": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}]; "MasterSyncMemberName": null}</span><span class="sxs-lookup"><span data-stu-id="e02a8-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="e02a8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e02a8-113">PARAMETERS</span></span>

### <span data-ttu-id="e02a8-114">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="e02a8-114">-DatabaseCredential</span></span>
<span data-ttu-id="e02a8-115">Autentiseringsuppgifter för SQL-autentisering för NAV databasen.</span><span class="sxs-lookup"><span data-stu-id="e02a8-115">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="e02a8-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e02a8-116">-DatabaseName</span></span>
<span data-ttu-id="e02a8-117">Namn på SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="e02a8-117">SQL Database name.</span></span>

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

### <span data-ttu-id="e02a8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e02a8-118">-DefaultProfile</span></span>
<span data-ttu-id="e02a8-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e02a8-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e02a8-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e02a8-120">-IntervalInSeconds</span></span>
<span data-ttu-id="e02a8-121">Frekvens (i sekunder) vid synkronisering av data.</span><span class="sxs-lookup"><span data-stu-id="e02a8-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="e02a8-122">Standard är-1, vilket innebär att den automatiska synkroniseringen inte är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="e02a8-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="e02a8-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="e02a8-123">-Name</span></span>
<span data-ttu-id="e02a8-124">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="e02a8-124">The sync group name.</span></span>

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

### <span data-ttu-id="e02a8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e02a8-125">-ResourceGroupName</span></span>
<span data-ttu-id="e02a8-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e02a8-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="e02a8-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="e02a8-127">-SchemaFile</span></span>
<span data-ttu-id="e02a8-128">Sökvägen till schema filen.</span><span class="sxs-lookup"><span data-stu-id="e02a8-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="e02a8-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e02a8-129">-ServerName</span></span>
<span data-ttu-id="e02a8-130">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e02a8-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="e02a8-131">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="e02a8-131">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="e02a8-132">Om en privat länk anslutning ska användas vid anslutning till navet i den här synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="e02a8-132">Whether to use a private link connection when connecting to the hub of this sync group.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e02a8-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e02a8-133">-Confirm</span></span>
<span data-ttu-id="e02a8-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e02a8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e02a8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e02a8-135">-WhatIf</span></span>
<span data-ttu-id="e02a8-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e02a8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e02a8-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e02a8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e02a8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e02a8-138">CommonParameters</span></span>
<span data-ttu-id="e02a8-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e02a8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e02a8-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e02a8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e02a8-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e02a8-141">INPUTS</span></span>

### <span data-ttu-id="e02a8-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e02a8-142">System.String</span></span>

## <span data-ttu-id="e02a8-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e02a8-143">OUTPUTS</span></span>

### <span data-ttu-id="e02a8-144">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="e02a8-144">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="e02a8-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e02a8-145">NOTES</span></span>

## <span data-ttu-id="e02a8-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e02a8-146">RELATED LINKS</span></span>

[<span data-ttu-id="e02a8-147">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e02a8-147">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="e02a8-148">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e02a8-148">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="e02a8-149">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e02a8-149">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

