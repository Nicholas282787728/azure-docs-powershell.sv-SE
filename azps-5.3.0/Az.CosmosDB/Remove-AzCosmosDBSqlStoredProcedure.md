---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 6abad7d11da1ba73f1f34804c32bddeb779b0b1d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524311"
---
# <span data-ttu-id="1d704-101">Remove-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="1d704-101">Remove-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="1d704-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1d704-102">SYNOPSIS</span></span>
<span data-ttu-id="1d704-103">Tar bort CosmosDB SQL-StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="1d704-103">Deletes the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="1d704-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1d704-104">SYNTAX</span></span>

### <span data-ttu-id="1d704-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d704-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d704-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d704-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -InputObject <PSSqlStoredProcedureGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d704-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1d704-107">DESCRIPTION</span></span>
<span data-ttu-id="1d704-108">Cmdleten **Remove-AzCosmosDBSqlStoredProcedure** tar bort den CosmosDB SQL-StoredProcedure som motsvarar angivet ResourceGroupName, AccountName och databasename.</span><span class="sxs-lookup"><span data-stu-id="1d704-108">The **Remove-AzCosmosDBSqlStoredProcedure** cmdlet deletes the CosmosDB Sql StoredProcedure corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="1d704-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1d704-109">EXAMPLES</span></span>

### <span data-ttu-id="1d704-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1d704-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {storedProcedureName}
```

## <span data-ttu-id="1d704-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1d704-111">PARAMETERS</span></span>

### <span data-ttu-id="1d704-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1d704-112">-AccountName</span></span>
<span data-ttu-id="1d704-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="1d704-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1d704-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1d704-114">-Confirm</span></span>
<span data-ttu-id="1d704-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1d704-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d704-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="1d704-116">-ContainerName</span></span>
<span data-ttu-id="1d704-117">Container namn.</span><span class="sxs-lookup"><span data-stu-id="1d704-117">Container name.</span></span>

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

### <span data-ttu-id="1d704-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1d704-118">-DatabaseName</span></span>
<span data-ttu-id="1d704-119">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="1d704-119">Database name.</span></span>

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

### <span data-ttu-id="1d704-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d704-120">-DefaultProfile</span></span>
<span data-ttu-id="1d704-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1d704-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d704-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d704-122">-InputObject</span></span>
<span data-ttu-id="1d704-123">SQL-databasnamn.</span><span class="sxs-lookup"><span data-stu-id="1d704-123">Sql Database object.</span></span>

```yaml
Type: PSSqlStoredProcedureGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d704-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="1d704-124">-Name</span></span>
<span data-ttu-id="1d704-125">Lagrat Prcodecure-namn.</span><span class="sxs-lookup"><span data-stu-id="1d704-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="1d704-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d704-126">-PassThru</span></span>
<span data-ttu-id="1d704-127">Anges till sant om användaren vill få ett resultat.</span><span class="sxs-lookup"><span data-stu-id="1d704-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="1d704-128">Resultatet är sant om åtgärden lyckades och ett fel inträffar om det inte är det.</span><span class="sxs-lookup"><span data-stu-id="1d704-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="1d704-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d704-129">-ResourceGroupName</span></span>
<span data-ttu-id="1d704-130">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1d704-130">Name of resource group.</span></span>

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

### <span data-ttu-id="1d704-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d704-131">-WhatIf</span></span>
<span data-ttu-id="1d704-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1d704-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d704-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1d704-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d704-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d704-134">CommonParameters</span></span>
<span data-ttu-id="1d704-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d704-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d704-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d704-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d704-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1d704-137">INPUTS</span></span>

### <span data-ttu-id="1d704-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="1d704-138">None</span></span>

## <span data-ttu-id="1d704-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1d704-139">OUTPUTS</span></span>

### <span data-ttu-id="1d704-140">System. Void</span><span class="sxs-lookup"><span data-stu-id="1d704-140">System.Void</span></span>

### <span data-ttu-id="1d704-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1d704-141">System.Boolean</span></span>

## <span data-ttu-id="1d704-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1d704-142">NOTES</span></span>

## <span data-ttu-id="1d704-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1d704-143">RELATED LINKS</span></span>
