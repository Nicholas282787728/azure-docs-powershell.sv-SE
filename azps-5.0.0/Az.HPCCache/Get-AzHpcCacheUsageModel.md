---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccacheusagemodels
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
ms.openlocfilehash: 4552de7be0f2a489aa152a922e39df623736f842
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271043"
---
# <span data-ttu-id="c2824-101">Get-AzHpcCacheUsageModel</span><span class="sxs-lookup"><span data-stu-id="c2824-101">Get-AzHpcCacheUsageModel</span></span>

## <span data-ttu-id="c2824-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2824-102">SYNOPSIS</span></span>
<span data-ttu-id="c2824-103">Hämtar alla usageModels för NFS-lagringsenheten.</span><span class="sxs-lookup"><span data-stu-id="c2824-103">Gets all usageModels for NFS Storage Target.</span></span>

## <span data-ttu-id="c2824-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2824-104">SYNTAX</span></span>

```
Get-AzHpcCacheUsageModel [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2824-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2824-105">DESCRIPTION</span></span>
<span data-ttu-id="c2824-106">Cmdleten **Get-AzHpcCacheUsageModel** returnerar en lista över användnings modeller för NFS-lagringsenheten.</span><span class="sxs-lookup"><span data-stu-id="c2824-106">The **Get-AzHpcCacheUsageModel** cmdlet returns a list of usage models for NFS Storage Target.</span></span>

## <span data-ttu-id="c2824-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2824-107">EXAMPLES</span></span>

### <span data-ttu-id="c2824-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c2824-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheUsageModel
```

## <span data-ttu-id="c2824-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2824-109">PARAMETERS</span></span>

### <span data-ttu-id="c2824-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2824-110">-DefaultProfile</span></span>
<span data-ttu-id="c2824-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2824-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2824-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2824-112">CommonParameters</span></span>
<span data-ttu-id="c2824-113">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2824-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2824-114">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2824-114">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2824-115">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2824-115">INPUTS</span></span>

### <span data-ttu-id="c2824-116">Ingen</span><span class="sxs-lookup"><span data-stu-id="c2824-116">None</span></span>

## <span data-ttu-id="c2824-117">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2824-117">OUTPUTS</span></span>

### <span data-ttu-id="c2824-118">Microsoft. Azure. PowerShell. cmdletar. HPCCache. Models. PSHpcUsageModels</span><span class="sxs-lookup"><span data-stu-id="c2824-118">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcUsageModels</span></span>

### <span data-ttu-id="c2824-119">System. Object</span><span class="sxs-lookup"><span data-stu-id="c2824-119">System.Object</span></span>
## <span data-ttu-id="c2824-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2824-120">NOTES</span></span>

## <span data-ttu-id="c2824-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2824-121">RELATED LINKS</span></span>