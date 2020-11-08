---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 69d3fa5be2b5650a3d4093c63a20d43e098062b6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091346"
---
# <span data-ttu-id="2bb66-101">Remove-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="2bb66-101">Remove-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="2bb66-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2bb66-102">SYNOPSIS</span></span>
<span data-ttu-id="2bb66-103">Tar bort en CosmosDB MongoDB-samling.</span><span class="sxs-lookup"><span data-stu-id="2bb66-103">Deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="2bb66-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2bb66-104">SYNTAX</span></span>

### <span data-ttu-id="2bb66-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2bb66-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2bb66-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bb66-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBCollection -InputObject <PSMongoDBCollectionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bb66-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2bb66-107">DESCRIPTION</span></span>
<span data-ttu-id="2bb66-108">Cmdleten **Remove-AzCosmosDBMongoDBCollection** tar bort en CosmosDB MongoDB-samling.</span><span class="sxs-lookup"><span data-stu-id="2bb66-108">The **Remove-AzCosmosDBMongoDBCollection** cmdlet deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="2bb66-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2bb66-109">EXAMPLES</span></span>

### <span data-ttu-id="2bb66-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2bb66-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {collectionName}
```

<span data-ttu-id="2bb66-111">Cmdleten returnerar ett objekt av typen bool (när-PassThru skickas), vilket är sant, om borttagningen lyckades.</span><span class="sxs-lookup"><span data-stu-id="2bb66-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="2bb66-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2bb66-112">PARAMETERS</span></span>

### <span data-ttu-id="2bb66-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2bb66-113">-AccountName</span></span>
<span data-ttu-id="2bb66-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="2bb66-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2bb66-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2bb66-115">-Confirm</span></span>
<span data-ttu-id="2bb66-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2bb66-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bb66-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2bb66-117">-DatabaseName</span></span>
<span data-ttu-id="2bb66-118">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="2bb66-118">Database name.</span></span>

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

### <span data-ttu-id="2bb66-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bb66-119">-DefaultProfile</span></span>
<span data-ttu-id="2bb66-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2bb66-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bb66-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2bb66-121">-InputObject</span></span>
<span data-ttu-id="2bb66-122">SQL-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="2bb66-122">Sql Container object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bb66-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="2bb66-123">-Name</span></span>
<span data-ttu-id="2bb66-124">Samlingens namn.</span><span class="sxs-lookup"><span data-stu-id="2bb66-124">Collection name.</span></span>

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

### <span data-ttu-id="2bb66-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2bb66-125">-PassThru</span></span>
<span data-ttu-id="2bb66-126">Anges till sant om användaren vill få ett resultat.</span><span class="sxs-lookup"><span data-stu-id="2bb66-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="2bb66-127">Resultatet är sant om åtgärden lyckades och ett fel inträffar om det inte är det.</span><span class="sxs-lookup"><span data-stu-id="2bb66-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="2bb66-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bb66-128">-ResourceGroupName</span></span>
<span data-ttu-id="2bb66-129">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2bb66-129">Name of resource group.</span></span>

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

### <span data-ttu-id="2bb66-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bb66-130">-WhatIf</span></span>
<span data-ttu-id="2bb66-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2bb66-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bb66-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2bb66-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bb66-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bb66-133">CommonParameters</span></span>
<span data-ttu-id="2bb66-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bb66-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bb66-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2bb66-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bb66-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2bb66-136">INPUTS</span></span>

### <span data-ttu-id="2bb66-137">Microsoft. Azure. commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="2bb66-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="2bb66-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2bb66-138">OUTPUTS</span></span>

### <span data-ttu-id="2bb66-139">System. Void</span><span class="sxs-lookup"><span data-stu-id="2bb66-139">System.Void</span></span>

### <span data-ttu-id="2bb66-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2bb66-140">System.Boolean</span></span>

## <span data-ttu-id="2bb66-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2bb66-141">NOTES</span></span>

## <span data-ttu-id="2bb66-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2bb66-142">RELATED LINKS</span></span>
