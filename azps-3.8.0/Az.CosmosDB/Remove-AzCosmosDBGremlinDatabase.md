---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 5c3150e2bdb81c8864116bc521b9f07f2ea43e1b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091347"
---
# <span data-ttu-id="79822-101">Remove-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="79822-101">Remove-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="79822-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79822-102">SYNOPSIS</span></span>
<span data-ttu-id="79822-103">Tar bort en CosmosDB Gremlin-databas.</span><span class="sxs-lookup"><span data-stu-id="79822-103">Deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="79822-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79822-104">SYNTAX</span></span>

### <span data-ttu-id="79822-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="79822-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79822-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79822-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -InputObject <PSGremlinDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79822-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79822-107">DESCRIPTION</span></span>
<span data-ttu-id="79822-108">Cmdleten **Remove-AzCosmosDBGremlinDatabase** tar bort en CosmosDB Gremlin-databas.</span><span class="sxs-lookup"><span data-stu-id="79822-108">The **Remove-AzCosmosDBGremlinDatabase** cmdlet deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="79822-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79822-109">EXAMPLES</span></span>

### <span data-ttu-id="79822-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="79822-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="79822-111">Cmdleten returnerar ett objekt av typen bool (när-PassThru skickas), vilket är sant, om borttagningen lyckades.</span><span class="sxs-lookup"><span data-stu-id="79822-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="79822-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79822-112">PARAMETERS</span></span>

### <span data-ttu-id="79822-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="79822-113">-AccountName</span></span>
<span data-ttu-id="79822-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="79822-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="79822-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="79822-115">-Confirm</span></span>
<span data-ttu-id="79822-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="79822-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79822-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79822-117">-DefaultProfile</span></span>
<span data-ttu-id="79822-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="79822-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79822-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79822-119">-InputObject</span></span>
<span data-ttu-id="79822-120">Gremlin.</span><span class="sxs-lookup"><span data-stu-id="79822-120">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79822-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="79822-121">-Name</span></span>
<span data-ttu-id="79822-122">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="79822-122">Database name.</span></span>

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

### <span data-ttu-id="79822-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79822-123">-PassThru</span></span>
<span data-ttu-id="79822-124">Anges till sant om användaren vill få ett resultat.</span><span class="sxs-lookup"><span data-stu-id="79822-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="79822-125">Resultatet är sant om åtgärden lyckades och ett fel inträffar om det inte är det.</span><span class="sxs-lookup"><span data-stu-id="79822-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="79822-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79822-126">-ResourceGroupName</span></span>
<span data-ttu-id="79822-127">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="79822-127">Name of resource group.</span></span>

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

### <span data-ttu-id="79822-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79822-128">-WhatIf</span></span>
<span data-ttu-id="79822-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="79822-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79822-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="79822-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79822-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79822-131">CommonParameters</span></span>
<span data-ttu-id="79822-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79822-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79822-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79822-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79822-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79822-134">INPUTS</span></span>

### <span data-ttu-id="79822-135">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="79822-135">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="79822-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79822-136">OUTPUTS</span></span>

### <span data-ttu-id="79822-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="79822-137">System.Void</span></span>

### <span data-ttu-id="79822-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="79822-138">System.Boolean</span></span>

## <span data-ttu-id="79822-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79822-139">NOTES</span></span>

## <span data-ttu-id="79822-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79822-140">RELATED LINKS</span></span>
