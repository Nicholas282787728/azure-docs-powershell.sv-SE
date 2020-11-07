---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgent.md
ms.openlocfilehash: e296e338d519537f688085fc5c142e3c12804b0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755281"
---
# <span data-ttu-id="be595-101">New-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="be595-101">New-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="be595-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="be595-102">SYNOPSIS</span></span>
<span data-ttu-id="be595-103">Skapar en agent för Azure SQL-synkronisering.</span><span class="sxs-lookup"><span data-stu-id="be595-103">Creates an Azure SQL Sync Agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be595-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="be595-104">SYNTAX</span></span>

### <span data-ttu-id="be595-105">SyncDatabaseComponent (standard)</span><span class="sxs-lookup"><span data-stu-id="be595-105">SyncDatabaseComponent (Default)</span></span>
```
New-AzureRmSqlSyncAgent [-Name] <String> -SyncDatabaseName <String> [-SyncDatabaseServerName <String>]
 [-SyncDatabaseResourceGroupName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be595-106">SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="be595-106">SyncDatabaseResourceID</span></span>
```
New-AzureRmSqlSyncAgent [-Name] <String> -SyncDatabaseResourceID <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be595-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="be595-107">DESCRIPTION</span></span>
<span data-ttu-id="be595-108">Cmdleten **New-AzureRmSqlSyncAgent** skapar en agent för Azure SQL-synkronisering.</span><span class="sxs-lookup"><span data-stu-id="be595-108">The **New-AzureRmSqlSyncAgent** cmdlet creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="be595-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="be595-109">EXAMPLES</span></span>

### <span data-ttu-id="be595-110">Exempel 1: skapa en synkroniseringsresurs för en Azure SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="be595-110">Example 1: Create a sync agent for an Azure SQL server.</span></span>
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

<span data-ttu-id="be595-111">Det här kommandot skapar en synkroniseringsresurs för en Azure SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="be595-111">This command creates a sync agent for an Azure SQL server.</span></span>

## <span data-ttu-id="be595-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="be595-112">PARAMETERS</span></span>

### <span data-ttu-id="be595-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="be595-113">-Confirm</span></span>
<span data-ttu-id="be595-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="be595-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be595-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="be595-115">-Name</span></span>
<span data-ttu-id="be595-116">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="be595-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be595-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be595-117">-ResourceGroupName</span></span>
<span data-ttu-id="be595-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="be595-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="be595-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="be595-119">-ServerName</span></span>
<span data-ttu-id="be595-120">Namnet på den Azure SQL-Server som synkroniseringsresursen finns i.</span><span class="sxs-lookup"><span data-stu-id="be595-120">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="be595-121">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="be595-121">-SyncDatabaseName</span></span>
<span data-ttu-id="be595-122">Databasen som används för att lagra synkroniserade metadata.</span><span class="sxs-lookup"><span data-stu-id="be595-122">The database used to store sync related metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be595-123">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be595-123">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="be595-124">Den resurs grupp som databasen för synkade metadata tillhör.</span><span class="sxs-lookup"><span data-stu-id="be595-124">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be595-125">-SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="be595-125">-SyncDatabaseResourceID</span></span>
<span data-ttu-id="be595-126">Resurs-ID för databasen med synkronisering.</span><span class="sxs-lookup"><span data-stu-id="be595-126">The resource ID of  the sync metadata database.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseResourceID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be595-127">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="be595-127">-SyncDatabaseServerName</span></span>
<span data-ttu-id="be595-128">Den server där databasen med synkrona data hanteras.</span><span class="sxs-lookup"><span data-stu-id="be595-128">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be595-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be595-129">-WhatIf</span></span>
<span data-ttu-id="be595-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="be595-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be595-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="be595-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be595-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be595-132">-DefaultProfile</span></span>
<span data-ttu-id="be595-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="be595-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be595-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be595-134">CommonParameters</span></span>
<span data-ttu-id="be595-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be595-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be595-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be595-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be595-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="be595-137">INPUTS</span></span>

## <span data-ttu-id="be595-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="be595-138">OUTPUTS</span></span>

### <span data-ttu-id="be595-139">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="be595-139">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="be595-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="be595-140">NOTES</span></span>

## <span data-ttu-id="be595-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="be595-141">RELATED LINKS</span></span>

[<span data-ttu-id="be595-142">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="be595-142">Remove-AzureRmSqlSyncAgent</span></span>](./Remove-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="be595-143">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="be595-143">Get-AzureRmSqlSyncAgent</span></span>](./Get-AzureRmSqlSyncAgent.md)

