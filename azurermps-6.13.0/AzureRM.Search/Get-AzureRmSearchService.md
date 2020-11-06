---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchService.md
ms.openlocfilehash: 57b09ea3267447f16ceadf4d1eae51f997c53a82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575081"
---
# <span data-ttu-id="66249-101">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="66249-101">Get-AzureRmSearchService</span></span>

## <span data-ttu-id="66249-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66249-102">SYNOPSIS</span></span>
<span data-ttu-id="66249-103">Hämtar en Azure Search-tjänst.</span><span class="sxs-lookup"><span data-stu-id="66249-103">Gets an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66249-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66249-104">SYNTAX</span></span>

### <span data-ttu-id="66249-105">ResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="66249-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmSearchService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66249-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66249-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66249-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66249-107">DESCRIPTION</span></span>
<span data-ttu-id="66249-108">Cmdleten **Get-AzureRmSearchService** hämtar den angivna Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="66249-108">The **Get-AzureRmSearchService** cmdlet gets the specified Azure Search service.</span></span>

## <span data-ttu-id="66249-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66249-109">EXAMPLES</span></span>

### <span data-ttu-id="66249-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="66249-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchService -ResourceGroupName felixwa-01


ResourceGroupName : felixwa-01
Name              : felixwa-basic-search
Location          : West US
Sku               : Basic
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/felixwa-01/providers/Microsoft.Search/searchServices/felixwa-basic-search
```

<span data-ttu-id="66249-111">Skaffa en Azure Search-tjänst med angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="66249-111">Get an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="66249-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66249-112">PARAMETERS</span></span>

### <span data-ttu-id="66249-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66249-113">-DefaultProfile</span></span>
<span data-ttu-id="66249-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="66249-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66249-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="66249-115">-Name</span></span>
<span data-ttu-id="66249-116">Sök tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="66249-116">Search Service name.</span></span>

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

### <span data-ttu-id="66249-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66249-117">-ResourceGroupName</span></span>
<span data-ttu-id="66249-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="66249-118">Resource Group name.</span></span>

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

### <span data-ttu-id="66249-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66249-119">-ResourceId</span></span>
<span data-ttu-id="66249-120">Sök tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="66249-120">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="66249-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66249-121">CommonParameters</span></span>
<span data-ttu-id="66249-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66249-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66249-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66249-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66249-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66249-124">INPUTS</span></span>

### <span data-ttu-id="66249-125">System. String</span><span class="sxs-lookup"><span data-stu-id="66249-125">System.String</span></span>

## <span data-ttu-id="66249-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66249-126">OUTPUTS</span></span>

### <span data-ttu-id="66249-127">Microsoft. Azure. commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="66249-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="66249-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66249-128">NOTES</span></span>

## <span data-ttu-id="66249-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66249-129">RELATED LINKS</span></span>

[<span data-ttu-id="66249-130">New-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="66249-130">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="66249-131">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="66249-131">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)

[<span data-ttu-id="66249-132">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="66249-132">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
