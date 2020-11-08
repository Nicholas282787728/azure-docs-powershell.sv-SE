---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
ms.openlocfilehash: 5c6dffe65022fa0282ab53bb04efe651ec123c2d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260605"
---
# <span data-ttu-id="9011f-101">Get-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="9011f-101">Get-AzCosmosDBAccount</span></span>

## <span data-ttu-id="9011f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9011f-102">SYNOPSIS</span></span>
<span data-ttu-id="9011f-103">Skaffa CosmosDB-konto.</span><span class="sxs-lookup"><span data-stu-id="9011f-103">Get CosmosDB Account.</span></span>

## <span data-ttu-id="9011f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9011f-104">SYNTAX</span></span>

### <span data-ttu-id="9011f-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9011f-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9011f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9011f-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9011f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9011f-107">DESCRIPTION</span></span>
<span data-ttu-id="9011f-108">Cmdleten **Get-AzCosmosDBAccount** hämtar listan över alla befintliga CosmosDB-konton för en viss ResourceGroupName och får ett enda CosmosDB-konto för ett givet ResourceGroupName och AccountName.</span><span class="sxs-lookup"><span data-stu-id="9011f-108">The **Get-AzCosmosDBAccount** cmdlet gets the list of all existing CosmosDB accounts for a given ResourceGroupName and gets a single CosmosDB account for a given ResourceGroupName and AccountName.</span></span>

## <span data-ttu-id="9011f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9011f-109">EXAMPLES</span></span>

### <span data-ttu-id="9011f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9011f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBAccount -ResourceGroupName {resourceGroupName} -Name {databaseAccountName}


Id                            : /subscriptions/{subscriptionid}/resourceGroups/{resourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{databaseAccountName}
Name                          : {databaseAccountName}
FailoverPolicies              : {databaseAccountName-region1}
ReadLocations                 : {databaseAccountName-region1}
WriteLocations                : {databaseAccountName-region1}
Capabilities                  : {}
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Models.ConsistencyPolicy
EnableAutomaticFailover       : False
IsVirtualNetworkFilterEnabled : False
IpRangeFilter                 :
DatabaseAccountOfferType      : Standard
DocumentEndpoint              : https://databaseAccountName.documents.azure.com:443/
ProvisioningState             : Succeeded
Kind                          : GlobalDocumentDB
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
```

<span data-ttu-id="9011f-111">Hämta CosmosDB databas konto med namnet databaseAccountName i ResourceGroup resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="9011f-111">Get CosmosDB database account with name databaseAccountName in ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="9011f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9011f-112">PARAMETERS</span></span>

### <span data-ttu-id="9011f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9011f-113">-DefaultProfile</span></span>
<span data-ttu-id="9011f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9011f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9011f-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="9011f-115">-Name</span></span>
<span data-ttu-id="9011f-116">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="9011f-116">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9011f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9011f-117">-ResourceGroupName</span></span>
<span data-ttu-id="9011f-118">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9011f-118">Name of resource group.</span></span>

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

### <span data-ttu-id="9011f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9011f-119">-ResourceId</span></span>
<span data-ttu-id="9011f-120">ResourceId för resursen.</span><span class="sxs-lookup"><span data-stu-id="9011f-120">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="9011f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9011f-121">CommonParameters</span></span>
<span data-ttu-id="9011f-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9011f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9011f-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9011f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9011f-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9011f-124">INPUTS</span></span>

### <span data-ttu-id="9011f-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="9011f-125">None</span></span>

## <span data-ttu-id="9011f-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9011f-126">OUTPUTS</span></span>

### <span data-ttu-id="9011f-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="9011f-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="9011f-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9011f-128">NOTES</span></span>

## <span data-ttu-id="9011f-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9011f-129">RELATED LINKS</span></span>
