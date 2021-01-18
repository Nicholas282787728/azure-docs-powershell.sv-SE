---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
ms.openlocfilehash: e4751232969c407484b978d495d348dc61810715
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522288"
---
# <span data-ttu-id="c4723-101">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="c4723-101">Get-AzSearchService</span></span>

## <span data-ttu-id="c4723-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4723-102">SYNOPSIS</span></span>
<span data-ttu-id="c4723-103">Hämtar en Azure Search-tjänst.</span><span class="sxs-lookup"><span data-stu-id="c4723-103">Gets an Azure Search service.</span></span>

## <span data-ttu-id="c4723-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4723-104">SYNTAX</span></span>

### <span data-ttu-id="c4723-105">ResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c4723-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSearchService [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4723-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4723-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4723-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4723-107">DESCRIPTION</span></span>
<span data-ttu-id="c4723-108">Cmdleten **Get-AzSearchService** hämtar den angivna Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c4723-108">The **Get-AzSearchService** cmdlet gets the specified Azure Search service.</span></span>

## <span data-ttu-id="c4723-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4723-109">EXAMPLES</span></span>

### <span data-ttu-id="c4723-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c4723-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchService -ResourceGroupName felixwa-01


ResourceGroupName : felixwa-01
Name              : felixwa-basic-search
Location          : West US
Sku               : Basic
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/felixwa-01/providers/Microsoft.Search/searchServices/felixwa-basic-search
```

<span data-ttu-id="c4723-111">Skaffa en Azure Search-tjänst med angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="c4723-111">Get an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="c4723-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4723-112">PARAMETERS</span></span>

### <span data-ttu-id="c4723-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4723-113">-DefaultProfile</span></span>
<span data-ttu-id="c4723-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c4723-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4723-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="c4723-115">-Name</span></span>
<span data-ttu-id="c4723-116">Sök tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="c4723-116">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4723-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4723-117">-ResourceGroupName</span></span>
<span data-ttu-id="c4723-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="c4723-118">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4723-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4723-119">-ResourceId</span></span>
<span data-ttu-id="c4723-120">Sök tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="c4723-120">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4723-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4723-121">CommonParameters</span></span>
<span data-ttu-id="c4723-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4723-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4723-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4723-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4723-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4723-124">INPUTS</span></span>

### <span data-ttu-id="c4723-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c4723-125">System.String</span></span>

## <span data-ttu-id="c4723-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4723-126">OUTPUTS</span></span>

### <span data-ttu-id="c4723-127">Microsoft. Azure. commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="c4723-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="c4723-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4723-128">NOTES</span></span>

## <span data-ttu-id="c4723-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4723-129">RELATED LINKS</span></span>

[<span data-ttu-id="c4723-130">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="c4723-130">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="c4723-131">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="c4723-131">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="c4723-132">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="c4723-132">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)