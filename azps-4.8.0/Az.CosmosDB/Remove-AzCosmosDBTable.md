---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
ms.openlocfilehash: ab8f0367f932a96d6296b5e6174bc3b6bbb651f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260102"
---
# <span data-ttu-id="5db1f-101">Remove-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="5db1f-101">Remove-AzCosmosDBTable</span></span>

## <span data-ttu-id="5db1f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5db1f-102">SYNOPSIS</span></span>
<span data-ttu-id="5db1f-103">Tar bort tabellen CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="5db1f-103">Deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="5db1f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5db1f-104">SYNTAX</span></span>

### <span data-ttu-id="5db1f-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5db1f-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBTable -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5db1f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5db1f-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBTable -InputObject <PSTableGetResults> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5db1f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5db1f-107">DESCRIPTION</span></span>
<span data-ttu-id="5db1f-108">Cmdleten **Remove-AzCosmosDBTable** tar bort CosmosDB-tabellen.</span><span class="sxs-lookup"><span data-stu-id="5db1f-108">The **Remove-AzCosmosDBTable** cmdlet deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="5db1f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5db1f-109">EXAMPLES</span></span>

### <span data-ttu-id="5db1f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5db1f-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}
```

<span data-ttu-id="5db1f-111">Cmdleten returnerar ett objekt av typen bool (när-PassThru skickas), vilket är sant, om borttagningen lyckades.</span><span class="sxs-lookup"><span data-stu-id="5db1f-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="5db1f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5db1f-112">PARAMETERS</span></span>

### <span data-ttu-id="5db1f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5db1f-113">-AccountName</span></span>
<span data-ttu-id="5db1f-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="5db1f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5db1f-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5db1f-115">-Confirm</span></span>
<span data-ttu-id="5db1f-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5db1f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5db1f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5db1f-117">-DefaultProfile</span></span>
<span data-ttu-id="5db1f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5db1f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5db1f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5db1f-119">-InputObject</span></span>
<span data-ttu-id="5db1f-120">SQL-databasnamn.</span><span class="sxs-lookup"><span data-stu-id="5db1f-120">Sql Database object.</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5db1f-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="5db1f-121">-Name</span></span>
<span data-ttu-id="5db1f-122">Namnet på tabellen.</span><span class="sxs-lookup"><span data-stu-id="5db1f-122">Name of the Table.</span></span>

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

### <span data-ttu-id="5db1f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5db1f-123">-PassThru</span></span>
<span data-ttu-id="5db1f-124">Anges till sant om användaren vill få ett resultat.</span><span class="sxs-lookup"><span data-stu-id="5db1f-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="5db1f-125">Resultatet är sant om åtgärden lyckades och ett fel inträffar om det inte är det.</span><span class="sxs-lookup"><span data-stu-id="5db1f-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="5db1f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5db1f-126">-ResourceGroupName</span></span>
<span data-ttu-id="5db1f-127">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5db1f-127">Name of resource group.</span></span>

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

### <span data-ttu-id="5db1f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5db1f-128">-WhatIf</span></span>
<span data-ttu-id="5db1f-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5db1f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5db1f-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5db1f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5db1f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5db1f-131">CommonParameters</span></span>
<span data-ttu-id="5db1f-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5db1f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5db1f-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5db1f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5db1f-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5db1f-134">INPUTS</span></span>

### <span data-ttu-id="5db1f-135">Microsoft. Azure. commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="5db1f-135">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="5db1f-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5db1f-136">OUTPUTS</span></span>

### <span data-ttu-id="5db1f-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="5db1f-137">System.Void</span></span>

### <span data-ttu-id="5db1f-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5db1f-138">System.Boolean</span></span>

## <span data-ttu-id="5db1f-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5db1f-139">NOTES</span></span>

## <span data-ttu-id="5db1f-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5db1f-140">RELATED LINKS</span></span>
