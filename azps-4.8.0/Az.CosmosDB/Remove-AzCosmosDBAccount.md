---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
ms.openlocfilehash: d10ed161ddab638e32126374d106eeffe3969a8e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260585"
---
# <span data-ttu-id="4d044-101">Remove-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="4d044-101">Remove-AzCosmosDBAccount</span></span>

## <span data-ttu-id="4d044-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d044-102">SYNOPSIS</span></span>
<span data-ttu-id="4d044-103">Ta bort ett CosmosDB-konto.</span><span class="sxs-lookup"><span data-stu-id="4d044-103">Remove a CosmosDB Account.</span></span>

## <span data-ttu-id="4d044-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d044-104">SYNTAX</span></span>

### <span data-ttu-id="4d044-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4d044-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d044-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d044-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCosmosDBAccount -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d044-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d044-107">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d044-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d044-108">DESCRIPTION</span></span>
<span data-ttu-id="4d044-109">Ta bort ett CosmosDB-konto med ett angivet namn i angiven ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4d044-109">Remove a CosmosDB Account with a given Name in the given ResourceGroup.</span></span>

## <span data-ttu-id="4d044-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d044-110">EXAMPLES</span></span>

### <span data-ttu-id="4d044-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4d044-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBAccount -ResourceGroupName rg -Name dbname  -PassThru

True
```

<span data-ttu-id="4d044-112">Kontot med konto namn dbname i ResourceGroup RG tas bort.</span><span class="sxs-lookup"><span data-stu-id="4d044-112">The Account with account name dbname in ResourceGroup rg is deleted.</span></span> 

## <span data-ttu-id="4d044-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d044-113">PARAMETERS</span></span>

### <span data-ttu-id="4d044-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d044-114">-AsJob</span></span>
<span data-ttu-id="4d044-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4d044-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d044-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4d044-116">-Confirm</span></span>
<span data-ttu-id="4d044-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4d044-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d044-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d044-118">-DefaultProfile</span></span>
<span data-ttu-id="4d044-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4d044-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d044-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d044-120">-InputObject</span></span>
<span data-ttu-id="4d044-121">Databas konto objekt</span><span class="sxs-lookup"><span data-stu-id="4d044-121">The Database Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d044-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="4d044-122">-Name</span></span>
<span data-ttu-id="4d044-123">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="4d044-123">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4d044-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d044-124">-PassThru</span></span>
<span data-ttu-id="4d044-125">Anges till sant om användaren vill få ett resultat.</span><span class="sxs-lookup"><span data-stu-id="4d044-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="4d044-126">Resultatet är sant om åtgärden lyckades och ett fel inträffar om det inte är det.</span><span class="sxs-lookup"><span data-stu-id="4d044-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="4d044-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d044-127">-ResourceGroupName</span></span>
<span data-ttu-id="4d044-128">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4d044-128">Name of resource group.</span></span>

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

### <span data-ttu-id="4d044-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d044-129">-ResourceId</span></span>
<span data-ttu-id="4d044-130">ResourceId för resursen.</span><span class="sxs-lookup"><span data-stu-id="4d044-130">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d044-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d044-131">-WhatIf</span></span>
<span data-ttu-id="4d044-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4d044-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d044-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4d044-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d044-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d044-134">CommonParameters</span></span>
<span data-ttu-id="4d044-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d044-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d044-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d044-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d044-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d044-137">INPUTS</span></span>

### <span data-ttu-id="4d044-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="4d044-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="4d044-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d044-139">OUTPUTS</span></span>

### <span data-ttu-id="4d044-140">System. Void</span><span class="sxs-lookup"><span data-stu-id="4d044-140">System.Void</span></span>

## <span data-ttu-id="4d044-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d044-141">NOTES</span></span>

## <span data-ttu-id="4d044-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d044-142">RELATED LINKS</span></span>
