---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 65ac7bb4a63fa8519bd8f0b0c006209d5f171833
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579295"
---
# <span data-ttu-id="ef814-101">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ef814-101">New-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="ef814-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef814-102">SYNOPSIS</span></span>
<span data-ttu-id="ef814-103">Skapar en synkroniseringsresurs för Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="ef814-103">Creates an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef814-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef814-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef814-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef814-105">DESCRIPTION</span></span>
<span data-ttu-id="ef814-106">Cmdleten **New-AzureRmSqlSyncGroup** skapar en synkroniseringsresurs för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="ef814-106">The **New-AzureRmSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="ef814-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef814-107">EXAMPLES</span></span>

### <span data-ttu-id="ef814-108">Exempel 1: skapa en synkroniseringsresurs för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="ef814-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" -ConflictResolutionPolicy "HubWin"
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

<span data-ttu-id="ef814-109">Det här kommandot skapar en synkroniseringsresurs för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="ef814-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="ef814-110">"schema.jsär en fil på den lokala hård disken.</span><span class="sxs-lookup"><span data-stu-id="ef814-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="ef814-111">Den innehåller Shema-nyttolasten i JSON-format.</span><span class="sxs-lookup"><span data-stu-id="ef814-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="ef814-112">Ett exempel på schema-JSON är: {"tabeller": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"kolumner": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}]; "MasterSyncMemberName": null}</span><span class="sxs-lookup"><span data-stu-id="ef814-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="ef814-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef814-113">PARAMETERS</span></span>

### <span data-ttu-id="ef814-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="ef814-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="ef814-115">Principen för att lösa konflikter mellan hubb och medlems databas i synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="ef814-115">The policy of resolving confliction between hub and member database in the sync group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: HubWin, MemberWin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef814-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="ef814-116">-DatabaseCredential</span></span>
<span data-ttu-id="ef814-117">Autentiseringsuppgifter för SQL-autentisering för NAV databasen.</span><span class="sxs-lookup"><span data-stu-id="ef814-117">The SQL authentication credential of the hub database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef814-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ef814-118">-DatabaseName</span></span>
<span data-ttu-id="ef814-119">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="ef814-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="ef814-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef814-120">-DefaultProfile</span></span>
<span data-ttu-id="ef814-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ef814-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef814-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="ef814-122">-IntervalInSeconds</span></span>
<span data-ttu-id="ef814-123">Frekvens (i sekunder) vid synkronisering av data.</span><span class="sxs-lookup"><span data-stu-id="ef814-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="ef814-124">Standard är-1, vilket innebär att den automatiska synkroniseringen inte är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="ef814-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef814-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="ef814-125">-Name</span></span>
<span data-ttu-id="ef814-126">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="ef814-126">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef814-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef814-127">-ResourceGroupName</span></span>
<span data-ttu-id="ef814-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ef814-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="ef814-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="ef814-129">-SchemaFile</span></span>
<span data-ttu-id="ef814-130">Sökvägen till schema filen.</span><span class="sxs-lookup"><span data-stu-id="ef814-130">The path of the schema file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef814-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ef814-131">-ServerName</span></span>
<span data-ttu-id="ef814-132">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ef814-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="ef814-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="ef814-133">-SyncDatabaseName</span></span>
<span data-ttu-id="ef814-134">Databasen som används för att lagra synkroniserade metadata.</span><span class="sxs-lookup"><span data-stu-id="ef814-134">The database used to store sync related metadata.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef814-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef814-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="ef814-136">Den resurs grupp som databasen för synkade metadata tillhör.</span><span class="sxs-lookup"><span data-stu-id="ef814-136">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef814-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="ef814-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="ef814-138">Den server där databasen med synkrona data hanteras.</span><span class="sxs-lookup"><span data-stu-id="ef814-138">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef814-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ef814-139">-Confirm</span></span>
<span data-ttu-id="ef814-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ef814-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef814-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef814-141">-WhatIf</span></span>
<span data-ttu-id="ef814-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ef814-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef814-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ef814-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef814-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef814-144">CommonParameters</span></span>
<span data-ttu-id="ef814-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef814-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef814-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef814-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef814-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef814-147">INPUTS</span></span>

### <span data-ttu-id="ef814-148">Ingen</span><span class="sxs-lookup"><span data-stu-id="ef814-148">None</span></span>
<span data-ttu-id="ef814-149">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ef814-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ef814-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef814-150">OUTPUTS</span></span>

### <span data-ttu-id="ef814-151">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="ef814-151">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="ef814-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef814-152">NOTES</span></span>

## <span data-ttu-id="ef814-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef814-153">RELATED LINKS</span></span>

[<span data-ttu-id="ef814-154">Set-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ef814-154">Set-AzureRmSqlSyncGroup</span></span>](./Set-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="ef814-155">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ef814-155">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="ef814-156">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ef814-156">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

