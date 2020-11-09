---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 10faa4b020633fdf46122c4864d50f00ef3ba54c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321659"
---
# <span data-ttu-id="fc24e-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="fc24e-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="fc24e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc24e-102">SYNOPSIS</span></span>
<span data-ttu-id="fc24e-103">Hämtar SQL-utlösaren för CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="fc24e-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="fc24e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc24e-104">SYNTAX</span></span>

### <span data-ttu-id="fc24e-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc24e-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc24e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc24e-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc24e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc24e-107">DESCRIPTION</span></span>
<span data-ttu-id="fc24e-108">Cmdleten **Get-AzCosmosDBSqlTrigger** hämtar listan över alla befintliga CosmosDB-SQL-utlösare för ett givet ResourceGroupName, AccountName, databasename och ContainerName och får en enda CosmosDB SQL-utlösare för ett givet ResourceGroupName, AccountName, databasename, ContainerName och TriggerName.</span><span class="sxs-lookup"><span data-stu-id="fc24e-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="fc24e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc24e-109">EXAMPLES</span></span>

### <span data-ttu-id="fc24e-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fc24e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="fc24e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc24e-111">PARAMETERS</span></span>

### <span data-ttu-id="fc24e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fc24e-112">-AccountName</span></span>
<span data-ttu-id="fc24e-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="fc24e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fc24e-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="fc24e-114">-ContainerName</span></span>
<span data-ttu-id="fc24e-115">Container namn.</span><span class="sxs-lookup"><span data-stu-id="fc24e-115">Container name.</span></span>

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

### <span data-ttu-id="fc24e-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fc24e-116">-DatabaseName</span></span>
<span data-ttu-id="fc24e-117">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="fc24e-117">Database name.</span></span>

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

### <span data-ttu-id="fc24e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc24e-118">-DefaultProfile</span></span>
<span data-ttu-id="fc24e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fc24e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc24e-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="fc24e-120">-Name</span></span>
<span data-ttu-id="fc24e-121">Utlösarnamn.</span><span class="sxs-lookup"><span data-stu-id="fc24e-121">Trigger name.</span></span>

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

### <span data-ttu-id="fc24e-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fc24e-122">-ParentObject</span></span>
<span data-ttu-id="fc24e-123">SQL-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="fc24e-123">Sql Container object.</span></span>

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

### <span data-ttu-id="fc24e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc24e-124">-ResourceGroupName</span></span>
<span data-ttu-id="fc24e-125">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fc24e-125">Name of resource group.</span></span>

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

### <span data-ttu-id="fc24e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc24e-126">CommonParameters</span></span>
<span data-ttu-id="fc24e-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc24e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc24e-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc24e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc24e-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc24e-129">INPUTS</span></span>

### <span data-ttu-id="fc24e-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="fc24e-130">None</span></span>

## <span data-ttu-id="fc24e-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc24e-131">OUTPUTS</span></span>

### <span data-ttu-id="fc24e-132">Microsoft. Azure. commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="fc24e-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="fc24e-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc24e-133">NOTES</span></span>

## <span data-ttu-id="fc24e-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc24e-134">RELATED LINKS</span></span>
