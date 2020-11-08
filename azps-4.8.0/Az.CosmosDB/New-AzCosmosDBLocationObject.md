---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 59fee5840ec279c7ed11b9b9d738561caf03ec66
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101607"
---
# <span data-ttu-id="3a76a-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="3a76a-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="3a76a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3a76a-102">SYNOPSIS</span></span>
<span data-ttu-id="3a76a-103">Skapa ett nytt CosmosDB (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="3a76a-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="3a76a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3a76a-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a76a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3a76a-105">DESCRIPTION</span></span>
<span data-ttu-id="3a76a-106">Skapa ett nytt CosmosDB (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="3a76a-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="3a76a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3a76a-107">EXAMPLES</span></span>

### <span data-ttu-id="3a76a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3a76a-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="3a76a-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3a76a-109">PARAMETERS</span></span>

### <span data-ttu-id="3a76a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a76a-110">-DefaultProfile</span></span>
<span data-ttu-id="3a76a-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3a76a-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a76a-112">-FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="3a76a-112">-FailoverPriority</span></span>
<span data-ttu-id="3a76a-113">Prioritet för platsen.</span><span class="sxs-lookup"><span data-stu-id="3a76a-113">Failover priority of the location.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a76a-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="3a76a-114">-IsZoneRedundant</span></span>
<span data-ttu-id="3a76a-115">Boolean för att ange om det här området är en AvailabilityZone.</span><span class="sxs-lookup"><span data-stu-id="3a76a-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a76a-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="3a76a-116">-LocationName</span></span>
<span data-ttu-id="3a76a-117">Namn på platsen i sträng.</span><span class="sxs-lookup"><span data-stu-id="3a76a-117">Name of the Location in string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a76a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a76a-118">CommonParameters</span></span>
<span data-ttu-id="3a76a-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a76a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a76a-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a76a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a76a-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3a76a-121">INPUTS</span></span>

### <span data-ttu-id="3a76a-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="3a76a-122">None</span></span>

## <span data-ttu-id="3a76a-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3a76a-123">OUTPUTS</span></span>

### <span data-ttu-id="3a76a-124">Microsoft. Azure. commands. CosmosDB. Models. PSLocation</span><span class="sxs-lookup"><span data-stu-id="3a76a-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="3a76a-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3a76a-125">NOTES</span></span>

## <span data-ttu-id="3a76a-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3a76a-126">RELATED LINKS</span></span>
