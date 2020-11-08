---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: e3c96cfd4051a186e0584d810088bc06a57ad862
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262343"
---
# <span data-ttu-id="90123-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="90123-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="90123-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90123-102">SYNOPSIS</span></span>
<span data-ttu-id="90123-103">Skapar ett nytt CosmosDB SQL UniqueKey-objekt.</span><span class="sxs-lookup"><span data-stu-id="90123-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="90123-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90123-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90123-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90123-105">DESCRIPTION</span></span>
<span data-ttu-id="90123-106">**New-AzCosmosDBSqlUniqueKey-** cmdleten skapar ett nytt objekt av typen PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="90123-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="90123-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90123-107">EXAMPLES</span></span>

### <span data-ttu-id="90123-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="90123-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="90123-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90123-109">PARAMETERS</span></span>

### <span data-ttu-id="90123-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90123-110">-DefaultProfile</span></span>
<span data-ttu-id="90123-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="90123-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90123-112">-Path</span><span class="sxs-lookup"><span data-stu-id="90123-112">-Path</span></span>
<span data-ttu-id="90123-113">Matris med Sök vägs värden</span><span class="sxs-lookup"><span data-stu-id="90123-113">Array of string of path values</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90123-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90123-114">CommonParameters</span></span>
<span data-ttu-id="90123-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90123-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90123-116">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90123-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90123-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90123-117">INPUTS</span></span>

### <span data-ttu-id="90123-118">Ingen</span><span class="sxs-lookup"><span data-stu-id="90123-118">None</span></span>

## <span data-ttu-id="90123-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90123-119">OUTPUTS</span></span>

### <span data-ttu-id="90123-120">Microsoft. Azure. commands. CosmosDB. Models. PSSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="90123-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="90123-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90123-121">NOTES</span></span>

## <span data-ttu-id="90123-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90123-122">RELATED LINKS</span></span>
