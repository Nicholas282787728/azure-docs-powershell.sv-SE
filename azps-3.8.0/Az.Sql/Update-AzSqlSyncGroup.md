---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
ms.openlocfilehash: cef62c85f42c2c9f0e6fbda776c58d6818659474
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927021"
---
# <span data-ttu-id="918ec-101">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="918ec-101">Update-AzSqlSyncGroup</span></span>

## <span data-ttu-id="918ec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="918ec-102">SYNOPSIS</span></span>
<span data-ttu-id="918ec-103">Uppdaterar en synkroniseringsresurs för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="918ec-103">Updates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="918ec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="918ec-104">SYNTAX</span></span>

```
Update-AzSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="918ec-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="918ec-105">DESCRIPTION</span></span>
<span data-ttu-id="918ec-106">Cmdleten **Update-AzSqlSyncGroup** ändrar egenskaperna för en synkroniseringsresurs för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="918ec-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="918ec-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="918ec-107">EXAMPLES</span></span>

### <span data-ttu-id="918ec-108">Exempel 1: uppdatera en synkroniseringsresurs för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="918ec-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
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

<span data-ttu-id="918ec-109">Det här kommandot uppdaterar en synkroniseringsresurs för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="918ec-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="918ec-110">"schema.jsär en fil på den lokala hård disken.</span><span class="sxs-lookup"><span data-stu-id="918ec-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="918ec-111">Den innehåller schemats nytto Last i JSON-format.</span><span class="sxs-lookup"><span data-stu-id="918ec-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="918ec-112">Ett exempel på schema-JSON är: {"tabeller": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"kolumner": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}]; "MasterSyncMemberName": null}</span><span class="sxs-lookup"><span data-stu-id="918ec-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="918ec-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="918ec-113">PARAMETERS</span></span>

### <span data-ttu-id="918ec-114">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="918ec-114">-DatabaseCredential</span></span>
<span data-ttu-id="918ec-115">Autentiseringsuppgifter för SQL-autentisering för NAV databasen.</span><span class="sxs-lookup"><span data-stu-id="918ec-115">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="918ec-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="918ec-116">-DatabaseName</span></span>
<span data-ttu-id="918ec-117">Namn på SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="918ec-117">SQL Database name.</span></span>

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

### <span data-ttu-id="918ec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="918ec-118">-DefaultProfile</span></span>
<span data-ttu-id="918ec-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="918ec-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="918ec-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="918ec-120">-IntervalInSeconds</span></span>
<span data-ttu-id="918ec-121">Frekvens (i sekunder) vid synkronisering av data.</span><span class="sxs-lookup"><span data-stu-id="918ec-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="918ec-122">Standard är-1, vilket innebär att den automatiska synkroniseringen inte är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="918ec-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="918ec-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="918ec-123">-Name</span></span>
<span data-ttu-id="918ec-124">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="918ec-124">The sync group name.</span></span>

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

### <span data-ttu-id="918ec-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="918ec-125">-ResourceGroupName</span></span>
<span data-ttu-id="918ec-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="918ec-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="918ec-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="918ec-127">-SchemaFile</span></span>
<span data-ttu-id="918ec-128">Sökvägen till schema filen.</span><span class="sxs-lookup"><span data-stu-id="918ec-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="918ec-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="918ec-129">-ServerName</span></span>
<span data-ttu-id="918ec-130">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="918ec-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="918ec-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="918ec-131">-Confirm</span></span>
<span data-ttu-id="918ec-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="918ec-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="918ec-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="918ec-133">-WhatIf</span></span>
<span data-ttu-id="918ec-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="918ec-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="918ec-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="918ec-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="918ec-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="918ec-136">CommonParameters</span></span>
<span data-ttu-id="918ec-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="918ec-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="918ec-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="918ec-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="918ec-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="918ec-139">INPUTS</span></span>

### <span data-ttu-id="918ec-140">System. String</span><span class="sxs-lookup"><span data-stu-id="918ec-140">System.String</span></span>

## <span data-ttu-id="918ec-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="918ec-141">OUTPUTS</span></span>

### <span data-ttu-id="918ec-142">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="918ec-142">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="918ec-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="918ec-143">NOTES</span></span>

## <span data-ttu-id="918ec-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="918ec-144">RELATED LINKS</span></span>

[<span data-ttu-id="918ec-145">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="918ec-145">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="918ec-146">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="918ec-146">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="918ec-147">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="918ec-147">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

