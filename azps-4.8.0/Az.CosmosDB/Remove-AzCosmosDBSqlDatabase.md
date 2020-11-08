---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 8496df5eb29d3f3a552e5b68a5e481d5cb01efd1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262338"
---
# <span data-ttu-id="111f8-101">Remove-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="111f8-101">Remove-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="111f8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="111f8-102">SYNOPSIS</span></span>
<span data-ttu-id="111f8-103">Tar bort CosmosDB SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="111f8-103">Deletes the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="111f8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="111f8-104">SYNTAX</span></span>

### <span data-ttu-id="111f8-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="111f8-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="111f8-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="111f8-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -InputObject <PSSqlDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="111f8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="111f8-107">DESCRIPTION</span></span>
<span data-ttu-id="111f8-108">Cmdleten **Remove-AzCosmosDBSqlDatabase** tar bort den CosmosDB SQL-databas som motsvarar angivet ResourceGroupName, AccountName och databasename.</span><span class="sxs-lookup"><span data-stu-id="111f8-108">The **Remove-AzCosmosDBSqlDatabase** cmdlet deletes the CosmosDB Sql Database corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="111f8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="111f8-109">EXAMPLES</span></span>

### <span data-ttu-id="111f8-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="111f8-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {databaseName}
```

## <span data-ttu-id="111f8-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="111f8-111">PARAMETERS</span></span>

### <span data-ttu-id="111f8-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="111f8-112">-AccountName</span></span>
<span data-ttu-id="111f8-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="111f8-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="111f8-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="111f8-114">-Confirm</span></span>
<span data-ttu-id="111f8-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="111f8-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="111f8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="111f8-116">-DefaultProfile</span></span>
<span data-ttu-id="111f8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="111f8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="111f8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="111f8-118">-InputObject</span></span>
<span data-ttu-id="111f8-119">SQL-databasnamn.</span><span class="sxs-lookup"><span data-stu-id="111f8-119">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="111f8-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="111f8-120">-Name</span></span>
<span data-ttu-id="111f8-121">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="111f8-121">Database name.</span></span>

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

### <span data-ttu-id="111f8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="111f8-122">-PassThru</span></span>
<span data-ttu-id="111f8-123">Anges till sant om användaren vill få ett resultat.</span><span class="sxs-lookup"><span data-stu-id="111f8-123">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="111f8-124">Resultatet är sant om åtgärden lyckades och ett fel inträffar om det inte är det.</span><span class="sxs-lookup"><span data-stu-id="111f8-124">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="111f8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="111f8-125">-ResourceGroupName</span></span>
<span data-ttu-id="111f8-126">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="111f8-126">Name of resource group.</span></span>

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

### <span data-ttu-id="111f8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="111f8-127">-WhatIf</span></span>
<span data-ttu-id="111f8-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="111f8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="111f8-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="111f8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="111f8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="111f8-130">CommonParameters</span></span>
<span data-ttu-id="111f8-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="111f8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="111f8-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="111f8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="111f8-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="111f8-133">INPUTS</span></span>

### <span data-ttu-id="111f8-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="111f8-134">None</span></span>

## <span data-ttu-id="111f8-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="111f8-135">OUTPUTS</span></span>

### <span data-ttu-id="111f8-136">System. Void</span><span class="sxs-lookup"><span data-stu-id="111f8-136">System.Void</span></span>

### <span data-ttu-id="111f8-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="111f8-137">System.Boolean</span></span>

## <span data-ttu-id="111f8-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="111f8-138">NOTES</span></span>

## <span data-ttu-id="111f8-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="111f8-139">RELATED LINKS</span></span>
