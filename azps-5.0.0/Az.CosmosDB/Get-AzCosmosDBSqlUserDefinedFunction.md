---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: b2f6e203b1ef8f14623df2910b853ea6f3841f72
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321648"
---
# <span data-ttu-id="c6581-101">Get-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="c6581-101">Get-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="c6581-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c6581-102">SYNOPSIS</span></span>
<span data-ttu-id="c6581-103">Hämtar den CosmosDB SQL-funktionen.</span><span class="sxs-lookup"><span data-stu-id="c6581-103">Gets the CosmosDB Sql User Defined Function.</span></span>

## <span data-ttu-id="c6581-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c6581-104">SYNTAX</span></span>

### <span data-ttu-id="c6581-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6581-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6581-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6581-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6581-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c6581-107">DESCRIPTION</span></span>
<span data-ttu-id="c6581-108">Cmdleten **Get-AzCosmosDBSqlUserDefinedFunction** hämtar listan över alla befintliga CosmosDB SQL-UserDefinedFunctions för ett givet ResourceGroupName, AccountName, databasename och ContainerName och hämtar en enda CosmosDB SQL-UserDefinedFunction för en given ResourceGroupName, AccountName, databasename, ContainerName och UserDefinedFunctionName.</span><span class="sxs-lookup"><span data-stu-id="c6581-108">The **Get-AzCosmosDBSqlUserDefinedFunction** cmdlet gets the list of all existing CosmosDB Sql UserDefinedFunctions for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql UserDefinedFunction for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and UserDefinedFunctionName.</span></span>

## <span data-ttu-id="c6581-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c6581-109">EXAMPLES</span></span>

### <span data-ttu-id="c6581-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c6581-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## <span data-ttu-id="c6581-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c6581-111">PARAMETERS</span></span>

### <span data-ttu-id="c6581-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c6581-112">-AccountName</span></span>
<span data-ttu-id="c6581-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="c6581-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c6581-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="c6581-114">-ContainerName</span></span>
<span data-ttu-id="c6581-115">Container namn.</span><span class="sxs-lookup"><span data-stu-id="c6581-115">Container name.</span></span>

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

### <span data-ttu-id="c6581-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c6581-116">-DatabaseName</span></span>
<span data-ttu-id="c6581-117">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="c6581-117">Database name.</span></span>

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

### <span data-ttu-id="c6581-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6581-118">-DefaultProfile</span></span>
<span data-ttu-id="c6581-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c6581-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6581-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="c6581-120">-Name</span></span>
<span data-ttu-id="c6581-121">Användardefinierat funktions namn.</span><span class="sxs-lookup"><span data-stu-id="c6581-121">User Defined Function Name.</span></span>

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

### <span data-ttu-id="c6581-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c6581-122">-ParentObject</span></span>
<span data-ttu-id="c6581-123">SQL-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="c6581-123">Sql Container object.</span></span>

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

### <span data-ttu-id="c6581-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6581-124">-ResourceGroupName</span></span>
<span data-ttu-id="c6581-125">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c6581-125">Name of resource group.</span></span>

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

### <span data-ttu-id="c6581-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6581-126">CommonParameters</span></span>
<span data-ttu-id="c6581-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6581-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6581-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6581-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6581-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c6581-129">INPUTS</span></span>

### <span data-ttu-id="c6581-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="c6581-130">None</span></span>

## <span data-ttu-id="c6581-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c6581-131">OUTPUTS</span></span>

### <span data-ttu-id="c6581-132">Microsoft. Azure. commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="c6581-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="c6581-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c6581-133">NOTES</span></span>

## <span data-ttu-id="c6581-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c6581-134">RELATED LINKS</span></span>
