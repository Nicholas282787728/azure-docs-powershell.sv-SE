---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 2d8d136385470267ee88b139cc3dc23e134b5b88
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524312"
---
# <span data-ttu-id="43194-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="43194-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="43194-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="43194-102">SYNOPSIS</span></span>
<span data-ttu-id="43194-103">Tar bort CosmosDB SQL-behållare.</span><span class="sxs-lookup"><span data-stu-id="43194-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="43194-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="43194-104">SYNTAX</span></span>

### <span data-ttu-id="43194-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="43194-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43194-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43194-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43194-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="43194-107">DESCRIPTION</span></span>
<span data-ttu-id="43194-108">Cmdleten **Remove-AzCosmosDBSqlContainer** tar bort den CosmosDB SQL-container som motsvarar angivet ResourceGroupName, AccountName, databasename och ContainerName.</span><span class="sxs-lookup"><span data-stu-id="43194-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="43194-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="43194-109">EXAMPLES</span></span>

### <span data-ttu-id="43194-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="43194-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="43194-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="43194-111">PARAMETERS</span></span>

### <span data-ttu-id="43194-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="43194-112">-AccountName</span></span>
<span data-ttu-id="43194-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="43194-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="43194-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="43194-114">-Confirm</span></span>
<span data-ttu-id="43194-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="43194-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43194-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="43194-116">-DatabaseName</span></span>
<span data-ttu-id="43194-117">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="43194-117">Database name.</span></span>

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

### <span data-ttu-id="43194-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43194-118">-DefaultProfile</span></span>
<span data-ttu-id="43194-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="43194-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43194-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43194-120">-InputObject</span></span>
<span data-ttu-id="43194-121">SQL-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="43194-121">Sql Container object.</span></span>

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

### <span data-ttu-id="43194-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="43194-122">-Name</span></span>
<span data-ttu-id="43194-123">Container namn.</span><span class="sxs-lookup"><span data-stu-id="43194-123">Container name.</span></span>

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

### <span data-ttu-id="43194-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43194-124">-PassThru</span></span>
<span data-ttu-id="43194-125">Anges till sant om användaren vill få ett resultat.</span><span class="sxs-lookup"><span data-stu-id="43194-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="43194-126">Resultatet är sant om åtgärden lyckades och ett fel inträffar om det inte är det.</span><span class="sxs-lookup"><span data-stu-id="43194-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="43194-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43194-127">-ResourceGroupName</span></span>
<span data-ttu-id="43194-128">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="43194-128">Name of resource group.</span></span>

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

### <span data-ttu-id="43194-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43194-129">-WhatIf</span></span>
<span data-ttu-id="43194-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="43194-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43194-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="43194-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43194-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43194-132">CommonParameters</span></span>
<span data-ttu-id="43194-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43194-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43194-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43194-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43194-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="43194-135">INPUTS</span></span>

### <span data-ttu-id="43194-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="43194-136">None</span></span>

## <span data-ttu-id="43194-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="43194-137">OUTPUTS</span></span>

### <span data-ttu-id="43194-138">System. Void</span><span class="sxs-lookup"><span data-stu-id="43194-138">System.Void</span></span>

### <span data-ttu-id="43194-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43194-139">System.Boolean</span></span>

## <span data-ttu-id="43194-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="43194-140">NOTES</span></span>

## <span data-ttu-id="43194-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="43194-141">RELATED LINKS</span></span>
