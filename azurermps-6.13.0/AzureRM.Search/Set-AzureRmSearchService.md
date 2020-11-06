---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/set-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Set-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Set-AzureRmSearchService.md
ms.openlocfilehash: c938dd611d9f6d731c07d5aee76cb390838f4679
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576088"
---
# <span data-ttu-id="02f43-101">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="02f43-101">Set-AzureRmSearchService</span></span>

## <span data-ttu-id="02f43-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02f43-102">SYNOPSIS</span></span>
<span data-ttu-id="02f43-103">Uppdatera en Azure Search-tjänst.</span><span class="sxs-lookup"><span data-stu-id="02f43-103">Update an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02f43-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02f43-104">SYNTAX</span></span>

### <span data-ttu-id="02f43-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="02f43-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02f43-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02f43-106">InputObjectParameterSet</span></span>
```
Set-AzureRmSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02f43-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02f43-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02f43-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02f43-108">DESCRIPTION</span></span>
<span data-ttu-id="02f43-109">Cmdleten **set-AzureRmSearchService** ändrar en Azure Search-tjänst.</span><span class="sxs-lookup"><span data-stu-id="02f43-109">The **Set-AzureRmSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="02f43-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02f43-110">EXAMPLES</span></span>

### <span data-ttu-id="02f43-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="02f43-111">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 2
PartitionCount    : 2
HostingMode       : Default
Tags              :
```

<span data-ttu-id="02f43-112">Exemplet ändrar antalet partitioner och antalet repliker för Azure Search-tjänsten till 2.</span><span class="sxs-lookup"><span data-stu-id="02f43-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="02f43-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02f43-113">PARAMETERS</span></span>

### <span data-ttu-id="02f43-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02f43-114">-DefaultProfile</span></span>
<span data-ttu-id="02f43-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="02f43-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02f43-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02f43-116">-InputObject</span></span>
<span data-ttu-id="02f43-117">Objekt för Sök tjänst.</span><span class="sxs-lookup"><span data-stu-id="02f43-117">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02f43-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="02f43-118">-Name</span></span>
<span data-ttu-id="02f43-119">Sök tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="02f43-119">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02f43-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="02f43-120">-PartitionCount</span></span>
<span data-ttu-id="02f43-121">Antal partitioner för Sök tjänsten.</span><span class="sxs-lookup"><span data-stu-id="02f43-121">Search Service partition count.</span></span>

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

### <span data-ttu-id="02f43-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="02f43-122">-ReplicaCount</span></span>
<span data-ttu-id="02f43-123">Sök tjänstens antal repliker.</span><span class="sxs-lookup"><span data-stu-id="02f43-123">Search Service replica count.</span></span>

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

### <span data-ttu-id="02f43-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02f43-124">-ResourceGroupName</span></span>
<span data-ttu-id="02f43-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="02f43-125">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02f43-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02f43-126">-ResourceId</span></span>
<span data-ttu-id="02f43-127">Sök tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="02f43-127">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="02f43-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="02f43-128">-Confirm</span></span>
<span data-ttu-id="02f43-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="02f43-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02f43-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02f43-130">-WhatIf</span></span>
<span data-ttu-id="02f43-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="02f43-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02f43-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="02f43-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02f43-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02f43-133">CommonParameters</span></span>
<span data-ttu-id="02f43-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02f43-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02f43-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02f43-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02f43-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02f43-136">INPUTS</span></span>

### <span data-ttu-id="02f43-137">Microsoft. Azure. commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="02f43-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="02f43-138">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="02f43-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="02f43-139">System. String</span><span class="sxs-lookup"><span data-stu-id="02f43-139">System.String</span></span>

## <span data-ttu-id="02f43-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02f43-140">OUTPUTS</span></span>

### <span data-ttu-id="02f43-141">Microsoft. Azure. commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="02f43-141">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="02f43-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02f43-142">NOTES</span></span>

## <span data-ttu-id="02f43-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02f43-143">RELATED LINKS</span></span>

[<span data-ttu-id="02f43-144">New-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="02f43-144">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="02f43-145">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="02f43-145">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="02f43-146">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="02f43-146">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
