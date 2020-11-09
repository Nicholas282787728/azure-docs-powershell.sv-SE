---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
ms.openlocfilehash: b9e78e4ff9811f5ff52b64369fd546d5f5a8c474
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321727"
---
# <span data-ttu-id="21cc2-101">Get-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="21cc2-101">Get-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="21cc2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="21cc2-102">SYNOPSIS</span></span>
<span data-ttu-id="21cc2-103">Skaffa nycklar {"ConnectionKeys", "PrimaryReadOnly" eller "nycklar"} för angivet CosmosDB-konto.</span><span class="sxs-lookup"><span data-stu-id="21cc2-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span></span> 

## <span data-ttu-id="21cc2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="21cc2-104">SYNTAX</span></span>

### <span data-ttu-id="21cc2-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="21cc2-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21cc2-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21cc2-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="21cc2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21cc2-107">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21cc2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="21cc2-108">DESCRIPTION</span></span>
<span data-ttu-id="21cc2-109">Hämta listan över anslutnings nycklar.</span><span class="sxs-lookup"><span data-stu-id="21cc2-109">Get the list of connection keys.</span></span>

## <span data-ttu-id="21cc2-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="21cc2-110">EXAMPLES</span></span>

### <span data-ttu-id="21cc2-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="21cc2-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzCosmosDBAccountKey -ResourceGroupName rg1 -Name dbname -Type "ReadOnlyKeys"

Name                           Value
----                           -----
PrimaryReadonlyMasterKey       qjw0ISW1WNN0BIVPeaI7Tm3H8uZ1h7ESQjxaUendxHmIUNQowVvcL84fTqeXoC2HFgyu8Zo1mCFEcg0jZJHPjA==
SecondaryReadonlyMasterKey     9YRcTABuOHcKyHAKf0lmCeHsrcXu02aeID1g3wjXjlX8SU4s2WNlEB5htJoy3xqxNDqIyGfnq3dblLbrZDbesg==
```

<span data-ttu-id="21cc2-112">Visar tangenterna för CosmosDB-kontot.</span><span class="sxs-lookup"><span data-stu-id="21cc2-112">Lists the keys for CosmosDB Account.</span></span> <span data-ttu-id="21cc2-113">Nyckel typen kan vara värde från: ConnectionString, Keys och ReadOnlyKeys.</span><span class="sxs-lookup"><span data-stu-id="21cc2-113">The Key Type can be value from : ConnectionStrings, Keys and ReadOnlyKeys.</span></span> <span data-ttu-id="21cc2-114">Standard är tangenter.</span><span class="sxs-lookup"><span data-stu-id="21cc2-114">Default is Keys.</span></span>

## <span data-ttu-id="21cc2-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="21cc2-115">PARAMETERS</span></span>

### <span data-ttu-id="21cc2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21cc2-116">-DefaultProfile</span></span>
<span data-ttu-id="21cc2-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="21cc2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21cc2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21cc2-118">-InputObject</span></span>
<span data-ttu-id="21cc2-119">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="21cc2-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="21cc2-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="21cc2-120">-Name</span></span>
<span data-ttu-id="21cc2-121">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="21cc2-121">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="21cc2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21cc2-122">-ResourceGroupName</span></span>
<span data-ttu-id="21cc2-123">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="21cc2-123">Name of resource group.</span></span>

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

### <span data-ttu-id="21cc2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21cc2-124">-ResourceId</span></span>
<span data-ttu-id="21cc2-125">ResourceId för resursen.</span><span class="sxs-lookup"><span data-stu-id="21cc2-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="21cc2-126">– Skriv</span><span class="sxs-lookup"><span data-stu-id="21cc2-126">-Type</span></span>
<span data-ttu-id="21cc2-127">Värde från: {ConnectionStrings, tangenter, ReadOnlyKeys}.</span><span class="sxs-lookup"><span data-stu-id="21cc2-127">Value from: {ConnectionStrings, Keys, ReadOnlyKeys}.</span></span>
<span data-ttu-id="21cc2-128">Standard är tangenter.</span><span class="sxs-lookup"><span data-stu-id="21cc2-128">Default is Keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21cc2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21cc2-129">CommonParameters</span></span>
<span data-ttu-id="21cc2-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21cc2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21cc2-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21cc2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21cc2-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="21cc2-132">INPUTS</span></span>

### <span data-ttu-id="21cc2-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="21cc2-133">None</span></span>

## <span data-ttu-id="21cc2-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="21cc2-134">OUTPUTS</span></span>

### <span data-ttu-id="21cc2-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="21cc2-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span></span>

### <span data-ttu-id="21cc2-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="21cc2-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span></span>

### <span data-ttu-id="21cc2-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span><span class="sxs-lookup"><span data-stu-id="21cc2-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span></span>

## <span data-ttu-id="21cc2-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="21cc2-138">NOTES</span></span>

## <span data-ttu-id="21cc2-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="21cc2-139">RELATED LINKS</span></span>
