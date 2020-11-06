---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 6e1d647c390d8d0f92192a63c3a395005074cfa6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579296"
---
# <span data-ttu-id="30d51-101">New-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="30d51-101">New-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="30d51-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30d51-102">SYNOPSIS</span></span>
<span data-ttu-id="30d51-103">Skapar en agent för Azure SQL-synkronisering.</span><span class="sxs-lookup"><span data-stu-id="30d51-103">Creates an Azure SQL Sync Agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30d51-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30d51-104">SYNTAX</span></span>

### <span data-ttu-id="30d51-105">SyncDatabaseComponent (standard)</span><span class="sxs-lookup"><span data-stu-id="30d51-105">SyncDatabaseComponent (Default)</span></span>
```
New-AzureRmSqlSyncAgent [-Name] <String> -SyncDatabaseName <String> [-SyncDatabaseServerName <String>]
 [-SyncDatabaseResourceGroupName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30d51-106">SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="30d51-106">SyncDatabaseResourceID</span></span>
```
New-AzureRmSqlSyncAgent [-Name] <String> -SyncDatabaseResourceID <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30d51-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30d51-107">DESCRIPTION</span></span>
<span data-ttu-id="30d51-108">Cmdleten **New-AzureRmSqlSyncAgent** skapar en agent för Azure SQL-synkronisering.</span><span class="sxs-lookup"><span data-stu-id="30d51-108">The **New-AzureRmSqlSyncAgent** cmdlet creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="30d51-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30d51-109">EXAMPLES</span></span>

### <span data-ttu-id="30d51-110">Exempel 1: skapa en synkroniseringsresurs för en Azure SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="30d51-110">Example 1: Create a sync agent for an Azure SQL server.</span></span>
```
PS C:\> New-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" -SyncDatabaseServerName "syncDatabaseServer01" 
-SyncDatabaseName "syncDatabaseName01" -SyncDatabaseResourceGroupName "syncDatabaseResourceGroup01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 
Version                     : 4.2.0.0
IsUpToDate                  : True
ExpiryTime                  : 12/31/9999 11:59:59 PM
State                       : NeverConnected
```

<span data-ttu-id="30d51-111">Det här kommandot skapar en synkroniseringsresurs för en Azure SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="30d51-111">This command creates a sync agent for an Azure SQL server.</span></span>

## <span data-ttu-id="30d51-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30d51-112">PARAMETERS</span></span>

### <span data-ttu-id="30d51-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30d51-113">-DefaultProfile</span></span>
<span data-ttu-id="30d51-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="30d51-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30d51-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="30d51-115">-Name</span></span>
<span data-ttu-id="30d51-116">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="30d51-116">The sync agent name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30d51-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30d51-117">-ResourceGroupName</span></span>
<span data-ttu-id="30d51-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="30d51-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="30d51-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="30d51-119">-ServerName</span></span>
<span data-ttu-id="30d51-120">Namnet på den Azure SQL-Server som synkroniseringsresursen finns i.</span><span class="sxs-lookup"><span data-stu-id="30d51-120">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="30d51-121">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="30d51-121">-SyncDatabaseName</span></span>
<span data-ttu-id="30d51-122">Databasen som används för att lagra synkroniserade metadata.</span><span class="sxs-lookup"><span data-stu-id="30d51-122">The database used to store sync related metadata.</span></span>

```yaml
Type: String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d51-123">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30d51-123">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="30d51-124">Den resurs grupp som databasen för synkade metadata tillhör.</span><span class="sxs-lookup"><span data-stu-id="30d51-124">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d51-125">-SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="30d51-125">-SyncDatabaseResourceID</span></span>
<span data-ttu-id="30d51-126">Resurs-ID för databasen med synkronisering.</span><span class="sxs-lookup"><span data-stu-id="30d51-126">The resource ID of  the sync metadata database.</span></span>

```yaml
Type: String
Parameter Sets: SyncDatabaseResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d51-127">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="30d51-127">-SyncDatabaseServerName</span></span>
<span data-ttu-id="30d51-128">Den server där databasen med synkrona data hanteras.</span><span class="sxs-lookup"><span data-stu-id="30d51-128">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d51-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="30d51-129">-Confirm</span></span>
<span data-ttu-id="30d51-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="30d51-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30d51-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30d51-131">-WhatIf</span></span>
<span data-ttu-id="30d51-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="30d51-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30d51-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="30d51-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30d51-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30d51-134">CommonParameters</span></span>
<span data-ttu-id="30d51-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30d51-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30d51-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30d51-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30d51-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30d51-137">INPUTS</span></span>

### <span data-ttu-id="30d51-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="30d51-138">None</span></span>
<span data-ttu-id="30d51-139">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="30d51-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30d51-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30d51-140">OUTPUTS</span></span>

### <span data-ttu-id="30d51-141">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="30d51-141">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="30d51-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30d51-142">NOTES</span></span>

## <span data-ttu-id="30d51-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30d51-143">RELATED LINKS</span></span>

[<span data-ttu-id="30d51-144">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="30d51-144">Remove-AzureRmSqlSyncAgent</span></span>](./Remove-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="30d51-145">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="30d51-145">Get-AzureRmSqlSyncAgent</span></span>](./Get-AzureRmSqlSyncAgent.md)

