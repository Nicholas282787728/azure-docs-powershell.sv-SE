---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/new-azurermsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchQueryKey.md
ms.openlocfilehash: 417e1a546777824df86b72f3740079ac91835192
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580708"
---
# <span data-ttu-id="7c6aa-101">New-AzureRmSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="7c6aa-101">New-AzureRmSearchQueryKey</span></span>

## <span data-ttu-id="7c6aa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7c6aa-102">SYNOPSIS</span></span>
<span data-ttu-id="7c6aa-103">Skapa en ny sessionsnyckel för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7c6aa-103">Create a new query key for the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c6aa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7c6aa-104">SYNTAX</span></span>

### <span data-ttu-id="7c6aa-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7c6aa-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c6aa-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c6aa-106">ParentObjectParameterSet</span></span>
```
New-AzureRmSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c6aa-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c6aa-107">ParentResourceIdParameterSet</span></span>
```
New-AzureRmSearchQueryKey [-ParentResourceId] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c6aa-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7c6aa-108">DESCRIPTION</span></span>
<span data-ttu-id="7c6aa-109">Cmdleten **New-AzureRmSearchQueryKey** skapar en ny sessionsnyckel för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7c6aa-109">The **New-AzureRmSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="7c6aa-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7c6aa-110">EXAMPLES</span></span>

### <span data-ttu-id="7c6aa-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7c6aa-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="7c6aa-112">I exemplet skapas en ny sessionsnyckel för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7c6aa-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="7c6aa-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7c6aa-113">PARAMETERS</span></span>

### <span data-ttu-id="7c6aa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c6aa-114">-DefaultProfile</span></span>
<span data-ttu-id="7c6aa-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7c6aa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c6aa-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="7c6aa-116">-Name</span></span>
<span data-ttu-id="7c6aa-117">Sök tjänstens frågeresultat.</span><span class="sxs-lookup"><span data-stu-id="7c6aa-117">Search Service query key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c6aa-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7c6aa-118">-ParentObject</span></span>
<span data-ttu-id="7c6aa-119">Objekt för Sök tjänst.</span><span class="sxs-lookup"><span data-stu-id="7c6aa-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c6aa-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7c6aa-120">-ParentResourceId</span></span>
<span data-ttu-id="7c6aa-121">Sök tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="7c6aa-121">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c6aa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c6aa-122">-ResourceGroupName</span></span>
<span data-ttu-id="7c6aa-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="7c6aa-123">Resource Group name.</span></span>

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

### <span data-ttu-id="7c6aa-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7c6aa-124">-ServiceName</span></span>
<span data-ttu-id="7c6aa-125">Sök tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="7c6aa-125">Search Service name.</span></span>

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

### <span data-ttu-id="7c6aa-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7c6aa-126">-Confirm</span></span>
<span data-ttu-id="7c6aa-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7c6aa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c6aa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c6aa-128">-WhatIf</span></span>
<span data-ttu-id="7c6aa-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7c6aa-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c6aa-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7c6aa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c6aa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c6aa-131">CommonParameters</span></span>
<span data-ttu-id="7c6aa-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c6aa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c6aa-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c6aa-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c6aa-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7c6aa-134">INPUTS</span></span>

### <span data-ttu-id="7c6aa-135">Microsoft. Azure. commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="7c6aa-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="7c6aa-136">Parametrar: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7c6aa-136">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="7c6aa-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7c6aa-137">System.String</span></span>

## <span data-ttu-id="7c6aa-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7c6aa-138">OUTPUTS</span></span>

### <span data-ttu-id="7c6aa-139">Microsoft. Azure. commands. Management. search. Models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="7c6aa-139">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="7c6aa-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7c6aa-140">NOTES</span></span>

## <span data-ttu-id="7c6aa-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7c6aa-141">RELATED LINKS</span></span>

[<span data-ttu-id="7c6aa-142">Get-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="7c6aa-142">Get-AzureRmSearchQueryKey.md</span></span>](./Get-AzureRmSearchQueryKey.md)

[<span data-ttu-id="7c6aa-143">Remove-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="7c6aa-143">Remove-AzureRmSearchQueryKey.md</span></span>](./Remove-AzureRmSearchQueryKey.md)
