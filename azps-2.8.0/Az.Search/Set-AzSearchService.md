---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: 5967ffbb5b0a39a771604c2f456de008d98de5fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919250"
---
# <span data-ttu-id="3bb36-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="3bb36-101">Set-AzSearchService</span></span>

## <span data-ttu-id="3bb36-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3bb36-102">SYNOPSIS</span></span>
<span data-ttu-id="3bb36-103">Uppdatera en Azure Search-tjänst.</span><span class="sxs-lookup"><span data-stu-id="3bb36-103">Update an Azure Search service.</span></span>

## <span data-ttu-id="3bb36-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3bb36-104">SYNTAX</span></span>

### <span data-ttu-id="3bb36-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3bb36-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bb36-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bb36-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bb36-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bb36-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bb36-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3bb36-108">DESCRIPTION</span></span>
<span data-ttu-id="3bb36-109">Cmdleten **set-AzSearchService** ändrar en Azure Search-tjänst.</span><span class="sxs-lookup"><span data-stu-id="3bb36-109">The **Set-AzSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="3bb36-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3bb36-110">EXAMPLES</span></span>

### <span data-ttu-id="3bb36-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3bb36-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


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

<span data-ttu-id="3bb36-112">Exemplet ändrar antalet partitioner och antalet repliker för Azure Search-tjänsten till 2.</span><span class="sxs-lookup"><span data-stu-id="3bb36-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="3bb36-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3bb36-113">PARAMETERS</span></span>

### <span data-ttu-id="3bb36-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bb36-114">-DefaultProfile</span></span>
<span data-ttu-id="3bb36-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3bb36-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bb36-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bb36-116">-InputObject</span></span>
<span data-ttu-id="3bb36-117">Objekt för Sök tjänst.</span><span class="sxs-lookup"><span data-stu-id="3bb36-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="3bb36-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="3bb36-118">-Name</span></span>
<span data-ttu-id="3bb36-119">Sök tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="3bb36-119">Search Service name.</span></span>

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

### <span data-ttu-id="3bb36-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="3bb36-120">-PartitionCount</span></span>
<span data-ttu-id="3bb36-121">Antal partitioner för Sök tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3bb36-121">Search Service partition count.</span></span>

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

### <span data-ttu-id="3bb36-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="3bb36-122">-ReplicaCount</span></span>
<span data-ttu-id="3bb36-123">Sök tjänstens antal repliker.</span><span class="sxs-lookup"><span data-stu-id="3bb36-123">Search Service replica count.</span></span>

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

### <span data-ttu-id="3bb36-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bb36-124">-ResourceGroupName</span></span>
<span data-ttu-id="3bb36-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="3bb36-125">Resource Group name.</span></span>

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

### <span data-ttu-id="3bb36-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bb36-126">-ResourceId</span></span>
<span data-ttu-id="3bb36-127">Sök tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="3bb36-127">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="3bb36-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3bb36-128">-Confirm</span></span>
<span data-ttu-id="3bb36-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3bb36-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bb36-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bb36-130">-WhatIf</span></span>
<span data-ttu-id="3bb36-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3bb36-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3bb36-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3bb36-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bb36-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bb36-133">CommonParameters</span></span>
<span data-ttu-id="3bb36-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bb36-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bb36-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bb36-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bb36-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3bb36-136">INPUTS</span></span>

### <span data-ttu-id="3bb36-137">Microsoft. Azure. commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="3bb36-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="3bb36-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3bb36-138">System.String</span></span>

## <span data-ttu-id="3bb36-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3bb36-139">OUTPUTS</span></span>

### <span data-ttu-id="3bb36-140">Microsoft. Azure. commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="3bb36-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="3bb36-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3bb36-141">NOTES</span></span>

## <span data-ttu-id="3bb36-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3bb36-142">RELATED LINKS</span></span>

[<span data-ttu-id="3bb36-143">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="3bb36-143">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="3bb36-144">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="3bb36-144">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="3bb36-145">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="3bb36-145">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)