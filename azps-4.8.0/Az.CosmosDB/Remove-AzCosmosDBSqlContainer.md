---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 2d8d136385470267ee88b139cc3dc23e134b5b88
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262341"
---
# <span data-ttu-id="e83aa-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="e83aa-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="e83aa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e83aa-102">SYNOPSIS</span></span>
<span data-ttu-id="e83aa-103">Tar bort CosmosDB SQL-behållare.</span><span class="sxs-lookup"><span data-stu-id="e83aa-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="e83aa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e83aa-104">SYNTAX</span></span>

### <span data-ttu-id="e83aa-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e83aa-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e83aa-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e83aa-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e83aa-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e83aa-107">DESCRIPTION</span></span>
<span data-ttu-id="e83aa-108">Cmdleten **Remove-AzCosmosDBSqlContainer** tar bort den CosmosDB SQL-container som motsvarar angivet ResourceGroupName, AccountName, databasename och ContainerName.</span><span class="sxs-lookup"><span data-stu-id="e83aa-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="e83aa-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e83aa-109">EXAMPLES</span></span>

### <span data-ttu-id="e83aa-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e83aa-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="e83aa-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e83aa-111">PARAMETERS</span></span>

### <span data-ttu-id="e83aa-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e83aa-112">-AccountName</span></span>
<span data-ttu-id="e83aa-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="e83aa-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e83aa-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e83aa-114">-Confirm</span></span>
<span data-ttu-id="e83aa-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e83aa-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e83aa-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e83aa-116">-DatabaseName</span></span>
<span data-ttu-id="e83aa-117">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="e83aa-117">Database name.</span></span>

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

### <span data-ttu-id="e83aa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e83aa-118">-DefaultProfile</span></span>
<span data-ttu-id="e83aa-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e83aa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e83aa-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e83aa-120">-InputObject</span></span>
<span data-ttu-id="e83aa-121">SQL-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="e83aa-121">Sql Container object.</span></span>

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

### <span data-ttu-id="e83aa-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="e83aa-122">-Name</span></span>
<span data-ttu-id="e83aa-123">Container namn.</span><span class="sxs-lookup"><span data-stu-id="e83aa-123">Container name.</span></span>

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

### <span data-ttu-id="e83aa-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e83aa-124">-PassThru</span></span>
<span data-ttu-id="e83aa-125">Anges till sant om användaren vill få ett resultat.</span><span class="sxs-lookup"><span data-stu-id="e83aa-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="e83aa-126">Resultatet är sant om åtgärden lyckades och ett fel inträffar om det inte är det.</span><span class="sxs-lookup"><span data-stu-id="e83aa-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e83aa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e83aa-127">-ResourceGroupName</span></span>
<span data-ttu-id="e83aa-128">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e83aa-128">Name of resource group.</span></span>

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

### <span data-ttu-id="e83aa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e83aa-129">-WhatIf</span></span>
<span data-ttu-id="e83aa-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e83aa-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e83aa-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e83aa-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e83aa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e83aa-132">CommonParameters</span></span>
<span data-ttu-id="e83aa-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e83aa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e83aa-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e83aa-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e83aa-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e83aa-135">INPUTS</span></span>

### <span data-ttu-id="e83aa-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="e83aa-136">None</span></span>

## <span data-ttu-id="e83aa-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e83aa-137">OUTPUTS</span></span>

### <span data-ttu-id="e83aa-138">System. Void</span><span class="sxs-lookup"><span data-stu-id="e83aa-138">System.Void</span></span>

### <span data-ttu-id="e83aa-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e83aa-139">System.Boolean</span></span>

## <span data-ttu-id="e83aa-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e83aa-140">NOTES</span></span>

## <span data-ttu-id="e83aa-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e83aa-141">RELATED LINKS</span></span>
