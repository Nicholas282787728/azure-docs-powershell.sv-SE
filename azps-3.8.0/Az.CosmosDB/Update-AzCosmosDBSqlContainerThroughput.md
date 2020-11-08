---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: e38e10765bc9a9768efaf1598a1865ec985b376c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089911"
---
# <span data-ttu-id="157f6-101">Update-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="157f6-101">Update-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="157f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="157f6-102">SYNOPSIS</span></span>
<span data-ttu-id="157f6-103">Uppdaterar genomflödet för en CosmosDB SQL-behållare.</span><span class="sxs-lookup"><span data-stu-id="157f6-103">Updates the throughput value of a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="157f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="157f6-104">SYNTAX</span></span>

### <span data-ttu-id="157f6-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="157f6-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="157f6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="157f6-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainerThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="157f6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="157f6-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainerThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="157f6-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="157f6-108">EXAMPLES</span></span>

### <span data-ttu-id="157f6-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="157f6-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlContainerThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {myDatabaseName} -Name {myContainerName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/sqlDatabases/{myDatabaseName}/conatiners/{myContainerName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="157f6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="157f6-110">PARAMETERS</span></span>

### <span data-ttu-id="157f6-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="157f6-111">-AccountName</span></span>
<span data-ttu-id="157f6-112">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="157f6-112">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="157f6-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="157f6-113">-Confirm</span></span>
<span data-ttu-id="157f6-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="157f6-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="157f6-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="157f6-115">-DatabaseName</span></span>
<span data-ttu-id="157f6-116">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="157f6-116">Database name.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="157f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="157f6-117">-DefaultProfile</span></span>
<span data-ttu-id="157f6-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="157f6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="157f6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="157f6-119">-InputObject</span></span>
<span data-ttu-id="157f6-120">SQL-databasnamn.</span><span class="sxs-lookup"><span data-stu-id="157f6-120">Sql Database object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="157f6-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="157f6-121">-Name</span></span>
<span data-ttu-id="157f6-122">Container namn.</span><span class="sxs-lookup"><span data-stu-id="157f6-122">Container name.</span></span>

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

### <span data-ttu-id="157f6-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="157f6-123">-ParentObject</span></span>
<span data-ttu-id="157f6-124">SQL-databasnamn.</span><span class="sxs-lookup"><span data-stu-id="157f6-124">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="157f6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="157f6-125">-ResourceGroupName</span></span>
<span data-ttu-id="157f6-126">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="157f6-126">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="157f6-127">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="157f6-127">-Throughput</span></span>
<span data-ttu-id="157f6-128">Genomflödet i SQL-behållare (RU/s).</span><span class="sxs-lookup"><span data-stu-id="157f6-128">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="157f6-129">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="157f6-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="157f6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="157f6-130">-WhatIf</span></span>
<span data-ttu-id="157f6-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="157f6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="157f6-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="157f6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="157f6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="157f6-133">CommonParameters</span></span>
<span data-ttu-id="157f6-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="157f6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="157f6-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="157f6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="157f6-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="157f6-136">INPUTS</span></span>

### <span data-ttu-id="157f6-137">Microsoft. Azure. commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="157f6-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="157f6-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="157f6-138">OUTPUTS</span></span>

### <span data-ttu-id="157f6-139">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="157f6-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="157f6-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="157f6-140">NOTES</span></span>

## <span data-ttu-id="157f6-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="157f6-141">RELATED LINKS</span></span>
