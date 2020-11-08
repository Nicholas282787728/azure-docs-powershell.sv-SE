---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: bf91d1948b4040a35ee77f2a1111861a03076783
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260591"
---
# <span data-ttu-id="ab322-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="ab322-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="ab322-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab322-102">SYNOPSIS</span></span>
<span data-ttu-id="ab322-103">Skapar ett nytt CosmosDB SqlUniqueKeyPolicy-objekt.</span><span class="sxs-lookup"><span data-stu-id="ab322-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="ab322-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab322-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab322-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab322-105">DESCRIPTION</span></span>
<span data-ttu-id="ab322-106">**New-AzCosmosDBSqlUniqueKeyPolicy-** cmdleten skapar ett nytt objekt av typen PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="ab322-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="ab322-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab322-107">EXAMPLES</span></span>

### <span data-ttu-id="ab322-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ab322-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="ab322-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab322-109">PARAMETERS</span></span>

### <span data-ttu-id="ab322-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab322-110">-DefaultProfile</span></span>
<span data-ttu-id="ab322-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ab322-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab322-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="ab322-112">-UniqueKey</span></span>
<span data-ttu-id="ab322-113">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="ab322-113">Database name.</span></span>

```yaml
Type: PSSqlUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab322-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab322-114">CommonParameters</span></span>
<span data-ttu-id="ab322-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab322-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab322-116">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab322-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab322-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab322-117">INPUTS</span></span>

### <span data-ttu-id="ab322-118">Ingen</span><span class="sxs-lookup"><span data-stu-id="ab322-118">None</span></span>

## <span data-ttu-id="ab322-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab322-119">OUTPUTS</span></span>

### <span data-ttu-id="ab322-120">Microsoft. Azure. commands. CosmosDB. Models. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="ab322-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="ab322-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab322-121">NOTES</span></span>

## <span data-ttu-id="ab322-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab322-122">RELATED LINKS</span></span>
