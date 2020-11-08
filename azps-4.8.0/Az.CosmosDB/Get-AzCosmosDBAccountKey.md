---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
ms.openlocfilehash: b9e78e4ff9811f5ff52b64369fd546d5f5a8c474
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260604"
---
# <span data-ttu-id="fff04-101">Get-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="fff04-101">Get-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="fff04-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fff04-102">SYNOPSIS</span></span>
<span data-ttu-id="fff04-103">Skaffa nycklar {"ConnectionKeys", "PrimaryReadOnly" eller "nycklar"} för angivet CosmosDB-konto.</span><span class="sxs-lookup"><span data-stu-id="fff04-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span></span> 

## <span data-ttu-id="fff04-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fff04-104">SYNTAX</span></span>

### <span data-ttu-id="fff04-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fff04-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fff04-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fff04-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fff04-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fff04-107">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fff04-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fff04-108">DESCRIPTION</span></span>
<span data-ttu-id="fff04-109">Hämta listan över anslutnings nycklar.</span><span class="sxs-lookup"><span data-stu-id="fff04-109">Get the list of connection keys.</span></span>

## <span data-ttu-id="fff04-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fff04-110">EXAMPLES</span></span>

### <span data-ttu-id="fff04-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fff04-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzCosmosDBAccountKey -ResourceGroupName rg1 -Name dbname -Type "ReadOnlyKeys"

Name                           Value
----                           -----
PrimaryReadonlyMasterKey       qjw0ISW1WNN0BIVPeaI7Tm3H8uZ1h7ESQjxaUendxHmIUNQowVvcL84fTqeXoC2HFgyu8Zo1mCFEcg0jZJHPjA==
SecondaryReadonlyMasterKey     9YRcTABuOHcKyHAKf0lmCeHsrcXu02aeID1g3wjXjlX8SU4s2WNlEB5htJoy3xqxNDqIyGfnq3dblLbrZDbesg==
```

<span data-ttu-id="fff04-112">Visar tangenterna för CosmosDB-kontot.</span><span class="sxs-lookup"><span data-stu-id="fff04-112">Lists the keys for CosmosDB Account.</span></span> <span data-ttu-id="fff04-113">Nyckel typen kan vara värde från: ConnectionString, Keys och ReadOnlyKeys.</span><span class="sxs-lookup"><span data-stu-id="fff04-113">The Key Type can be value from : ConnectionStrings, Keys and ReadOnlyKeys.</span></span> <span data-ttu-id="fff04-114">Standard är tangenter.</span><span class="sxs-lookup"><span data-stu-id="fff04-114">Default is Keys.</span></span>

## <span data-ttu-id="fff04-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fff04-115">PARAMETERS</span></span>

### <span data-ttu-id="fff04-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fff04-116">-DefaultProfile</span></span>
<span data-ttu-id="fff04-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fff04-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fff04-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fff04-118">-InputObject</span></span>
<span data-ttu-id="fff04-119">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="fff04-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="fff04-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="fff04-120">-Name</span></span>
<span data-ttu-id="fff04-121">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="fff04-121">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fff04-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fff04-122">-ResourceGroupName</span></span>
<span data-ttu-id="fff04-123">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fff04-123">Name of resource group.</span></span>

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

### <span data-ttu-id="fff04-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fff04-124">-ResourceId</span></span>
<span data-ttu-id="fff04-125">ResourceId för resursen.</span><span class="sxs-lookup"><span data-stu-id="fff04-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="fff04-126">– Skriv</span><span class="sxs-lookup"><span data-stu-id="fff04-126">-Type</span></span>
<span data-ttu-id="fff04-127">Värde från: {ConnectionStrings, tangenter, ReadOnlyKeys}.</span><span class="sxs-lookup"><span data-stu-id="fff04-127">Value from: {ConnectionStrings, Keys, ReadOnlyKeys}.</span></span>
<span data-ttu-id="fff04-128">Standard är tangenter.</span><span class="sxs-lookup"><span data-stu-id="fff04-128">Default is Keys.</span></span>

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

### <span data-ttu-id="fff04-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fff04-129">CommonParameters</span></span>
<span data-ttu-id="fff04-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fff04-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fff04-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fff04-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fff04-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fff04-132">INPUTS</span></span>

### <span data-ttu-id="fff04-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="fff04-133">None</span></span>

## <span data-ttu-id="fff04-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fff04-134">OUTPUTS</span></span>

### <span data-ttu-id="fff04-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="fff04-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span></span>

### <span data-ttu-id="fff04-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="fff04-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span></span>

### <span data-ttu-id="fff04-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span><span class="sxs-lookup"><span data-stu-id="fff04-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span></span>

## <span data-ttu-id="fff04-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fff04-138">NOTES</span></span>

## <span data-ttu-id="fff04-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fff04-139">RELATED LINKS</span></span>
