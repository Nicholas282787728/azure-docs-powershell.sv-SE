---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: cc7c443ad4447abfa1c31ebb335d3d1ae602f1b3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524324"
---
# <span data-ttu-id="40d50-101">New-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="40d50-101">New-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="40d50-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40d50-102">SYNOPSIS</span></span>
<span data-ttu-id="40d50-103">Skapar en ny CosmosDB SQL-UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="40d50-103">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="40d50-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40d50-104">SYNTAX</span></span>

### <span data-ttu-id="40d50-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="40d50-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40d50-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40d50-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40d50-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40d50-107">DESCRIPTION</span></span>
<span data-ttu-id="40d50-108">Skapar en ny CosmosDB SQL-UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="40d50-108">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="40d50-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40d50-109">EXAMPLES</span></span>

### <span data-ttu-id="40d50-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="40d50-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="40d50-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40d50-111">PARAMETERS</span></span>

### <span data-ttu-id="40d50-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="40d50-112">-AccountName</span></span>
<span data-ttu-id="40d50-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="40d50-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="40d50-114">-Body</span><span class="sxs-lookup"><span data-stu-id="40d50-114">-Body</span></span>
<span data-ttu-id="40d50-115">Bröd texten i den användardefinierade funktionen.</span><span class="sxs-lookup"><span data-stu-id="40d50-115">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="40d50-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="40d50-116">-Confirm</span></span>
<span data-ttu-id="40d50-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="40d50-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40d50-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="40d50-118">-ContainerName</span></span>
<span data-ttu-id="40d50-119">Container namn.</span><span class="sxs-lookup"><span data-stu-id="40d50-119">Container name.</span></span>

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

### <span data-ttu-id="40d50-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="40d50-120">-DatabaseName</span></span>
<span data-ttu-id="40d50-121">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="40d50-121">Database name.</span></span>

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

### <span data-ttu-id="40d50-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d50-122">-DefaultProfile</span></span>
<span data-ttu-id="40d50-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="40d50-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40d50-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="40d50-124">-Name</span></span>
<span data-ttu-id="40d50-125">Användardefinierat funktions namn.</span><span class="sxs-lookup"><span data-stu-id="40d50-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="40d50-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="40d50-126">-ParentObject</span></span>
<span data-ttu-id="40d50-127">SQL-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="40d50-127">Sql Container object.</span></span>

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

### <span data-ttu-id="40d50-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40d50-128">-ResourceGroupName</span></span>
<span data-ttu-id="40d50-129">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="40d50-129">Name of resource group.</span></span>

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

### <span data-ttu-id="40d50-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40d50-130">-WhatIf</span></span>
<span data-ttu-id="40d50-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="40d50-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40d50-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="40d50-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40d50-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d50-133">CommonParameters</span></span>
<span data-ttu-id="40d50-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40d50-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d50-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40d50-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d50-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40d50-136">INPUTS</span></span>

### <span data-ttu-id="40d50-137">Microsoft. Azure. commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="40d50-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="40d50-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40d50-138">OUTPUTS</span></span>

### <span data-ttu-id="40d50-139">Microsoft. Azure. commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="40d50-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="40d50-140">Microsoft. Azure. commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="40d50-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="40d50-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40d50-141">NOTES</span></span>

## <span data-ttu-id="40d50-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40d50-142">RELATED LINKS</span></span>
