---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 6631cad83260a935f2849391941ec0cf6514b188
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088286"
---
# <span data-ttu-id="0a7c9-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="0a7c9-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="0a7c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0a7c9-102">SYNOPSIS</span></span>
<span data-ttu-id="0a7c9-103">Hämtar SQL-utlösaren för CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="0a7c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0a7c9-104">SYNTAX</span></span>

### <span data-ttu-id="0a7c9-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a7c9-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a7c9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a7c9-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a7c9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0a7c9-107">DESCRIPTION</span></span>
<span data-ttu-id="0a7c9-108">Cmdleten **Get-AzCosmosDBSqlTrigger** hämtar listan över alla befintliga CosmosDB-SQL-utlösare för ett givet ResourceGroupName, AccountName, databasename och ContainerName och får en enda CosmosDB SQL-utlösare för ett givet ResourceGroupName, AccountName, databasename, ContainerName och TriggerName.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="0a7c9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0a7c9-109">EXAMPLES</span></span>

### <span data-ttu-id="0a7c9-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0a7c9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="0a7c9-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0a7c9-111">PARAMETERS</span></span>

### <span data-ttu-id="0a7c9-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0a7c9-112">-AccountName</span></span>
<span data-ttu-id="0a7c9-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0a7c9-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="0a7c9-114">-ContainerName</span></span>
<span data-ttu-id="0a7c9-115">Container namn.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-115">Container name.</span></span>

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

### <span data-ttu-id="0a7c9-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0a7c9-116">-DatabaseName</span></span>
<span data-ttu-id="0a7c9-117">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-117">Database name.</span></span>

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

### <span data-ttu-id="0a7c9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a7c9-118">-DefaultProfile</span></span>
<span data-ttu-id="0a7c9-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a7c9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a7c9-120">-InputObject</span></span>
<span data-ttu-id="0a7c9-121">SQL-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-121">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a7c9-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="0a7c9-122">-Name</span></span>
<span data-ttu-id="0a7c9-123">Utlösarnamn.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-123">Trigger name.</span></span>

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

### <span data-ttu-id="0a7c9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a7c9-124">-ResourceGroupName</span></span>
<span data-ttu-id="0a7c9-125">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-125">Name of resource group.</span></span>

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

### <span data-ttu-id="0a7c9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a7c9-126">CommonParameters</span></span>
<span data-ttu-id="0a7c9-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a7c9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a7c9-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a7c9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a7c9-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0a7c9-129">INPUTS</span></span>

### <span data-ttu-id="0a7c9-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="0a7c9-130">None</span></span>

## <span data-ttu-id="0a7c9-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0a7c9-131">OUTPUTS</span></span>

### <span data-ttu-id="0a7c9-132">Microsoft. Azure. commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="0a7c9-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="0a7c9-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0a7c9-133">NOTES</span></span>

## <span data-ttu-id="0a7c9-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0a7c9-134">RELATED LINKS</span></span>
