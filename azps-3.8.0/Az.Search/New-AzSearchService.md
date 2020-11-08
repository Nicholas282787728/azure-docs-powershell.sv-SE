---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 3fa4a8c1868673b4ce9bc630a70e02bb92a55fda
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090047"
---
# <span data-ttu-id="757b3-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="757b3-101">New-AzSearchService</span></span>

## <span data-ttu-id="757b3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="757b3-102">SYNOPSIS</span></span>
<span data-ttu-id="757b3-103">Skapar en Azure Search-tjänst.</span><span class="sxs-lookup"><span data-stu-id="757b3-103">Creates an Azure Search service.</span></span>

## <span data-ttu-id="757b3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="757b3-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="757b3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="757b3-105">DESCRIPTION</span></span>
<span data-ttu-id="757b3-106">Cmdleten **New-AzSearchService** skapar en Azure Search-tjänst med angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="757b3-106">The **New-AzSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="757b3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="757b3-107">EXAMPLES</span></span>

### <span data-ttu-id="757b3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="757b3-108">Example 1</span></span>
```powershell
PS C:\> New-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -Sku "Standard" -Location "West US" -PartitionCount 1 -ReplicaCount 1 -HostingMode Default -Force


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

<span data-ttu-id="757b3-109">Kommandot skapar en Azure Search-tjänst.</span><span class="sxs-lookup"><span data-stu-id="757b3-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="757b3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="757b3-110">PARAMETERS</span></span>

### <span data-ttu-id="757b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="757b3-111">-DefaultProfile</span></span>
<span data-ttu-id="757b3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="757b3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="757b3-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="757b3-113">-HostingMode</span></span>
<span data-ttu-id="757b3-114">Sök tjänstens värd läge.</span><span class="sxs-lookup"><span data-stu-id="757b3-114">Search Service hosting mode.</span></span>

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

### <span data-ttu-id="757b3-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="757b3-115">-Location</span></span>
<span data-ttu-id="757b3-116">Sök tjänst plats.</span><span class="sxs-lookup"><span data-stu-id="757b3-116">Search Service location.</span></span>

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

### <span data-ttu-id="757b3-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="757b3-117">-Name</span></span>
<span data-ttu-id="757b3-118">Sök tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="757b3-118">Search Service name.</span></span>

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

### <span data-ttu-id="757b3-119">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="757b3-119">-PartitionCount</span></span>
<span data-ttu-id="757b3-120">Antal partitioner för Sök tjänsten.</span><span class="sxs-lookup"><span data-stu-id="757b3-120">Search Service partition count.</span></span>

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

### <span data-ttu-id="757b3-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="757b3-121">-ReplicaCount</span></span>
<span data-ttu-id="757b3-122">Sök tjänstens antal repliker.</span><span class="sxs-lookup"><span data-stu-id="757b3-122">Search Service replica count.</span></span>

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

### <span data-ttu-id="757b3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="757b3-123">-ResourceGroupName</span></span>
<span data-ttu-id="757b3-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="757b3-124">Resource Group name.</span></span>

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

### <span data-ttu-id="757b3-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="757b3-125">-Sku</span></span>
<span data-ttu-id="757b3-126">SKU för Sök tjänst.</span><span class="sxs-lookup"><span data-stu-id="757b3-126">Search Service Sku.</span></span>

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

### <span data-ttu-id="757b3-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="757b3-127">-Confirm</span></span>
<span data-ttu-id="757b3-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="757b3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="757b3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="757b3-129">-WhatIf</span></span>
<span data-ttu-id="757b3-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="757b3-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="757b3-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="757b3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="757b3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="757b3-132">CommonParameters</span></span>
<span data-ttu-id="757b3-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="757b3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="757b3-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="757b3-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="757b3-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="757b3-135">INPUTS</span></span>

### <span data-ttu-id="757b3-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="757b3-136">None</span></span>

## <span data-ttu-id="757b3-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="757b3-137">OUTPUTS</span></span>

### <span data-ttu-id="757b3-138">Microsoft. Azure. commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="757b3-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="757b3-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="757b3-139">NOTES</span></span>

## <span data-ttu-id="757b3-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="757b3-140">RELATED LINKS</span></span>

[<span data-ttu-id="757b3-141">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="757b3-141">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="757b3-142">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="757b3-142">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="757b3-143">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="757b3-143">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)