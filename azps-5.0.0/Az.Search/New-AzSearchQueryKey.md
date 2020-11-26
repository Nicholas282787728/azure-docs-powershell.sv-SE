---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: e01e5e244bd34e3e18aa287e0f2f5709c5e208ec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271419"
---
# <span data-ttu-id="3b9f8-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="3b9f8-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="3b9f8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b9f8-102">SYNOPSIS</span></span>
<span data-ttu-id="3b9f8-103">Skapa en ny sessionsnyckel för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-103">Create a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="3b9f8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b9f8-104">SYNTAX</span></span>

### <span data-ttu-id="3b9f8-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3b9f8-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b9f8-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b9f8-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b9f8-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b9f8-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b9f8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b9f8-108">DESCRIPTION</span></span>
<span data-ttu-id="3b9f8-109">Cmdleten **New-AzSearchQueryKey** skapar en ny sessionsnyckel för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="3b9f8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b9f8-110">EXAMPLES</span></span>

### <span data-ttu-id="3b9f8-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3b9f8-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="3b9f8-112">I exemplet skapas en ny sessionsnyckel för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="3b9f8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b9f8-113">PARAMETERS</span></span>

### <span data-ttu-id="3b9f8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b9f8-114">-DefaultProfile</span></span>
<span data-ttu-id="3b9f8-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b9f8-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="3b9f8-116">-Name</span></span>
<span data-ttu-id="3b9f8-117">Sök tjänstens frågeresultat.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-117">Search Service query key name.</span></span>

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

### <span data-ttu-id="3b9f8-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3b9f8-118">-ParentObject</span></span>
<span data-ttu-id="3b9f8-119">Objekt för Sök tjänst.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="3b9f8-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3b9f8-120">-ParentResourceId</span></span>
<span data-ttu-id="3b9f8-121">Sök tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-121">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="3b9f8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b9f8-122">-ResourceGroupName</span></span>
<span data-ttu-id="3b9f8-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-123">Resource Group name.</span></span>

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

### <span data-ttu-id="3b9f8-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3b9f8-124">-ServiceName</span></span>
<span data-ttu-id="3b9f8-125">Sök tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-125">Search Service name.</span></span>

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

### <span data-ttu-id="3b9f8-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3b9f8-126">-Confirm</span></span>
<span data-ttu-id="3b9f8-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b9f8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b9f8-128">-WhatIf</span></span>
<span data-ttu-id="3b9f8-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b9f8-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b9f8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b9f8-131">CommonParameters</span></span>
<span data-ttu-id="3b9f8-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b9f8-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b9f8-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b9f8-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b9f8-134">INPUTS</span></span>

### <span data-ttu-id="3b9f8-135">Microsoft. Azure. commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="3b9f8-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="3b9f8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3b9f8-136">System.String</span></span>

## <span data-ttu-id="3b9f8-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b9f8-137">OUTPUTS</span></span>

### <span data-ttu-id="3b9f8-138">Microsoft. Azure. commands. Management. search. Models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="3b9f8-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="3b9f8-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b9f8-139">NOTES</span></span>

## <span data-ttu-id="3b9f8-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b9f8-140">RELATED LINKS</span></span>

[<span data-ttu-id="3b9f8-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="3b9f8-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="3b9f8-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="3b9f8-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)