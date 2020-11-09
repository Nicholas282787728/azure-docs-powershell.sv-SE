---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 37da28136e8c0a794e263cff4c2b9f9c0d6ce69f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321411"
---
# <span data-ttu-id="88bc9-101">Remove-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="88bc9-101">Remove-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="88bc9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="88bc9-102">SYNOPSIS</span></span>
<span data-ttu-id="88bc9-103">Tar bort CosmosDB SQL-UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="88bc9-103">Deletes the CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="88bc9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="88bc9-104">SYNTAX</span></span>

### <span data-ttu-id="88bc9-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="88bc9-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88bc9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88bc9-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -InputObject <PSSqlUserDefinedFunctionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88bc9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="88bc9-107">DESCRIPTION</span></span>
<span data-ttu-id="88bc9-108">Cmdleten **Remove-AzCosmosDBSqlUserDefinedFunction** tar bort den CosmosDB SQL-UserDefinedFunction som motsvarar angivet ResourceGroupName, AccountName och databasename.</span><span class="sxs-lookup"><span data-stu-id="88bc9-108">The **Remove-AzCosmosDBSqlUserDefinedFunction** cmdlet deletes the CosmosDB Sql UserDefinedFunction corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="88bc9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="88bc9-109">EXAMPLES</span></span>

### <span data-ttu-id="88bc9-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="88bc9-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {userDefinedFunctionName}
```

## <span data-ttu-id="88bc9-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="88bc9-111">PARAMETERS</span></span>

### <span data-ttu-id="88bc9-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="88bc9-112">-AccountName</span></span>
<span data-ttu-id="88bc9-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="88bc9-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="88bc9-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="88bc9-114">-Confirm</span></span>
<span data-ttu-id="88bc9-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="88bc9-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88bc9-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="88bc9-116">-ContainerName</span></span>
<span data-ttu-id="88bc9-117">Container namn.</span><span class="sxs-lookup"><span data-stu-id="88bc9-117">Container name.</span></span>

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

### <span data-ttu-id="88bc9-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="88bc9-118">-DatabaseName</span></span>
<span data-ttu-id="88bc9-119">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="88bc9-119">Database name.</span></span>

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

### <span data-ttu-id="88bc9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88bc9-120">-DefaultProfile</span></span>
<span data-ttu-id="88bc9-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="88bc9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88bc9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88bc9-122">-InputObject</span></span>
<span data-ttu-id="88bc9-123">SQL-användardefinierat funktions objekt</span><span class="sxs-lookup"><span data-stu-id="88bc9-123">Sql User Defined Function Object</span></span>

```yaml
Type: PSSqlUserDefinedFunctionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88bc9-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="88bc9-124">-Name</span></span>
<span data-ttu-id="88bc9-125">Användardefinierat funktions namn.</span><span class="sxs-lookup"><span data-stu-id="88bc9-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="88bc9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88bc9-126">-PassThru</span></span>
<span data-ttu-id="88bc9-127">Anges till sant om användaren vill få ett resultat.</span><span class="sxs-lookup"><span data-stu-id="88bc9-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="88bc9-128">Resultatet är sant om åtgärden lyckades och ett fel inträffar om det inte är det.</span><span class="sxs-lookup"><span data-stu-id="88bc9-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="88bc9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88bc9-129">-ResourceGroupName</span></span>
<span data-ttu-id="88bc9-130">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="88bc9-130">Name of resource group.</span></span>

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

### <span data-ttu-id="88bc9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88bc9-131">-WhatIf</span></span>
<span data-ttu-id="88bc9-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="88bc9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88bc9-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="88bc9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88bc9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88bc9-134">CommonParameters</span></span>
<span data-ttu-id="88bc9-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88bc9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88bc9-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88bc9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88bc9-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="88bc9-137">INPUTS</span></span>

### <span data-ttu-id="88bc9-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="88bc9-138">None</span></span>

## <span data-ttu-id="88bc9-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="88bc9-139">OUTPUTS</span></span>

### <span data-ttu-id="88bc9-140">System. Void</span><span class="sxs-lookup"><span data-stu-id="88bc9-140">System.Void</span></span>

### <span data-ttu-id="88bc9-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="88bc9-141">System.Boolean</span></span>

## <span data-ttu-id="88bc9-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="88bc9-142">NOTES</span></span>

## <span data-ttu-id="88bc9-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="88bc9-143">RELATED LINKS</span></span>
