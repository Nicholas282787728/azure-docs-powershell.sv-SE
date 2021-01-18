---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: 82b5bdd7e10b8119a058ab3a30f6836ff9255d01
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520575"
---
# <span data-ttu-id="d32d0-101">Get-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="d32d0-101">Get-AzHpcCache</span></span>

## <span data-ttu-id="d32d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d32d0-102">SYNOPSIS</span></span>
<span data-ttu-id="d32d0-103">Hämtar ett/ett/a cacheminne.</span><span class="sxs-lookup"><span data-stu-id="d32d0-103">Gets a cache(s).</span></span>

## <span data-ttu-id="d32d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d32d0-104">SYNTAX</span></span>

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d32d0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d32d0-105">DESCRIPTION</span></span>
<span data-ttu-id="d32d0-106">Cmdleten **Get-AzHpcCache** hämtar en enda cache, cache (er) i en specifik resurs grupp eller en prenumerations lista över cache.</span><span class="sxs-lookup"><span data-stu-id="d32d0-106">The **Get-AzHpcCache** cmdlet gets a single cache, cache(s) in a specific resource group, or subscription wide list of caches.</span></span>

## <span data-ttu-id="d32d0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d32d0-107">EXAMPLES</span></span>

### <span data-ttu-id="d32d0-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d32d0-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### <span data-ttu-id="d32d0-109">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d32d0-109">Example 2</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### <span data-ttu-id="d32d0-110">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="d32d0-110">Example 3</span></span>
```powershell
PS C:\> Get-AzHPCCache
```

## <span data-ttu-id="d32d0-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d32d0-111">PARAMETERS</span></span>

### <span data-ttu-id="d32d0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d32d0-112">-DefaultProfile</span></span>
<span data-ttu-id="d32d0-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d32d0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d32d0-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="d32d0-114">-Name</span></span>
<span data-ttu-id="d32d0-115">Namn på ett specifikt cacheminne.</span><span class="sxs-lookup"><span data-stu-id="d32d0-115">Name of specific cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d32d0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d32d0-116">-ResourceGroupName</span></span>
<span data-ttu-id="d32d0-117">Namnet på den resurs grupp under vilket du vill visa cache (s).</span><span class="sxs-lookup"><span data-stu-id="d32d0-117">Name of resource group under which you want to list cache(s).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d32d0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d32d0-118">CommonParameters</span></span>
<span data-ttu-id="d32d0-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d32d0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d32d0-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d32d0-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d32d0-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d32d0-121">INPUTS</span></span>

### <span data-ttu-id="d32d0-122">System. String</span><span class="sxs-lookup"><span data-stu-id="d32d0-122">System.String</span></span>

## <span data-ttu-id="d32d0-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d32d0-123">OUTPUTS</span></span>

### <span data-ttu-id="d32d0-124">Microsoft. Azure. PowerShell. cmdletar. HPCCache. Models. PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="d32d0-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="d32d0-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d32d0-125">NOTES</span></span>

## <span data-ttu-id="d32d0-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d32d0-126">RELATED LINKS</span></span>
