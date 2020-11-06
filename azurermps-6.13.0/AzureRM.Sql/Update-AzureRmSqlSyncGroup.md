---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/update-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 6d5c2671ec80e3234eb1ab7f26ba005c77f5b872
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583412"
---
# <span data-ttu-id="05c51-101">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="05c51-101">Update-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="05c51-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05c51-102">SYNOPSIS</span></span>
<span data-ttu-id="05c51-103">Uppdaterar en synkroniseringsresurs för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="05c51-103">Updates an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05c51-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05c51-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05c51-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05c51-105">DESCRIPTION</span></span>
<span data-ttu-id="05c51-106">Cmdleten **Update-AzureRmSqlSyncGroup** ändrar egenskaperna för en synkroniseringsresurs för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="05c51-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="05c51-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05c51-107">EXAMPLES</span></span>

### <span data-ttu-id="05c51-108">Exempel 1: uppdatera en synkroniseringsresurs för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="05c51-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01"
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

<span data-ttu-id="05c51-109">Det här kommandot uppdaterar en synkroniseringsresurs för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="05c51-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="05c51-110">"schema.jsär en fil på den lokala hård disken.</span><span class="sxs-lookup"><span data-stu-id="05c51-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="05c51-111">Den innehåller Shema-nyttolasten i JSON-format.</span><span class="sxs-lookup"><span data-stu-id="05c51-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="05c51-112">Ett exempel på schema-JSON är: {"tabeller": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"kolumner": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}]; "MasterSyncMemberName": null}</span><span class="sxs-lookup"><span data-stu-id="05c51-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="05c51-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05c51-113">PARAMETERS</span></span>

### <span data-ttu-id="05c51-114">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="05c51-114">-DatabaseCredential</span></span>
<span data-ttu-id="05c51-115">Autentiseringsuppgifter för SQL-autentisering för NAV databasen.</span><span class="sxs-lookup"><span data-stu-id="05c51-115">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="05c51-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="05c51-116">-DatabaseName</span></span>
<span data-ttu-id="05c51-117">Namn på SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="05c51-117">SQL Database name.</span></span>

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

### <span data-ttu-id="05c51-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05c51-118">-DefaultProfile</span></span>
<span data-ttu-id="05c51-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="05c51-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05c51-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="05c51-120">-IntervalInSeconds</span></span>
<span data-ttu-id="05c51-121">Frekvens (i sekunder) vid synkronisering av data.</span><span class="sxs-lookup"><span data-stu-id="05c51-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="05c51-122">Standard är-1, vilket innebär att den automatiska synkroniseringen inte är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="05c51-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="05c51-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="05c51-123">-Name</span></span>
<span data-ttu-id="05c51-124">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="05c51-124">The sync group name.</span></span>

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

### <span data-ttu-id="05c51-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05c51-125">-ResourceGroupName</span></span>
<span data-ttu-id="05c51-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="05c51-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="05c51-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="05c51-127">-SchemaFile</span></span>
<span data-ttu-id="05c51-128">Sökvägen till schema filen.</span><span class="sxs-lookup"><span data-stu-id="05c51-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="05c51-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="05c51-129">-ServerName</span></span>
<span data-ttu-id="05c51-130">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="05c51-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="05c51-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="05c51-131">-Confirm</span></span>
<span data-ttu-id="05c51-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="05c51-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05c51-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05c51-133">-WhatIf</span></span>
<span data-ttu-id="05c51-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="05c51-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05c51-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="05c51-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05c51-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05c51-136">CommonParameters</span></span>
<span data-ttu-id="05c51-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05c51-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05c51-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05c51-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05c51-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05c51-139">INPUTS</span></span>

### <span data-ttu-id="05c51-140">System. String</span><span class="sxs-lookup"><span data-stu-id="05c51-140">System.String</span></span>

## <span data-ttu-id="05c51-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05c51-141">OUTPUTS</span></span>

### <span data-ttu-id="05c51-142">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="05c51-142">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="05c51-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05c51-143">NOTES</span></span>

## <span data-ttu-id="05c51-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05c51-144">RELATED LINKS</span></span>

[<span data-ttu-id="05c51-145">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="05c51-145">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="05c51-146">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="05c51-146">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="05c51-147">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="05c51-147">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

