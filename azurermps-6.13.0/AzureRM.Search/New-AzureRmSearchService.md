---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/new-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchService.md
ms.openlocfilehash: 934ba85d438178ee636d5042f1fa145e63d60291
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576091"
---
# <span data-ttu-id="fe755-101">New-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="fe755-101">New-AzureRmSearchService</span></span>

## <span data-ttu-id="fe755-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe755-102">SYNOPSIS</span></span>
<span data-ttu-id="fe755-103">Skapar en Azure Search-tjänst.</span><span class="sxs-lookup"><span data-stu-id="fe755-103">Creates an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe755-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe755-104">SYNTAX</span></span>

```
New-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe755-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe755-105">DESCRIPTION</span></span>
<span data-ttu-id="fe755-106">Cmdleten **New-AzureRmSearchService** skapar en Azure Search-tjänst med angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="fe755-106">The **New-AzureRmSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="fe755-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe755-107">EXAMPLES</span></span>

### <span data-ttu-id="fe755-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fe755-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -Sku "Standard" -Location "West US" -PartitionCount 1 -ReplicaCount 1 -HostingMode Default -Force


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Tags              :
```

<span data-ttu-id="fe755-109">Kommandot skapar en Azure Search-tjänst.</span><span class="sxs-lookup"><span data-stu-id="fe755-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="fe755-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe755-110">PARAMETERS</span></span>

### <span data-ttu-id="fe755-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe755-111">-DefaultProfile</span></span>
<span data-ttu-id="fe755-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe755-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe755-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="fe755-113">-HostingMode</span></span>
<span data-ttu-id="fe755-114">Sök tjänstens värd läge.</span><span class="sxs-lookup"><span data-stu-id="fe755-114">Search Service hosting mode.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSHostingMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, HighDensity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe755-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="fe755-115">-Location</span></span>
<span data-ttu-id="fe755-116">Sök tjänst plats.</span><span class="sxs-lookup"><span data-stu-id="fe755-116">Search Service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe755-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="fe755-117">-Name</span></span>
<span data-ttu-id="fe755-118">Sök tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="fe755-118">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe755-119">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="fe755-119">-PartitionCount</span></span>
<span data-ttu-id="fe755-120">Antal partitioner för Sök tjänsten.</span><span class="sxs-lookup"><span data-stu-id="fe755-120">Search Service partition count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe755-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="fe755-121">-ReplicaCount</span></span>
<span data-ttu-id="fe755-122">Sök tjänstens antal repliker.</span><span class="sxs-lookup"><span data-stu-id="fe755-122">Search Service replica count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe755-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe755-123">-ResourceGroupName</span></span>
<span data-ttu-id="fe755-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="fe755-124">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe755-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="fe755-125">-Sku</span></span>
<span data-ttu-id="fe755-126">SKU för Sök tjänst.</span><span class="sxs-lookup"><span data-stu-id="fe755-126">Search Service Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard, Standard2, Standard3

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe755-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fe755-127">-Confirm</span></span>
<span data-ttu-id="fe755-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fe755-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe755-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe755-129">-WhatIf</span></span>
<span data-ttu-id="fe755-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fe755-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe755-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fe755-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe755-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe755-132">CommonParameters</span></span>
<span data-ttu-id="fe755-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe755-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe755-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe755-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe755-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe755-135">INPUTS</span></span>

### <span data-ttu-id="fe755-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="fe755-136">None</span></span>

## <span data-ttu-id="fe755-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe755-137">OUTPUTS</span></span>

### <span data-ttu-id="fe755-138">Microsoft. Azure. commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="fe755-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="fe755-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe755-139">NOTES</span></span>

## <span data-ttu-id="fe755-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe755-140">RELATED LINKS</span></span>

[<span data-ttu-id="fe755-141">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="fe755-141">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="fe755-142">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="fe755-142">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)

[<span data-ttu-id="fe755-143">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="fe755-143">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
