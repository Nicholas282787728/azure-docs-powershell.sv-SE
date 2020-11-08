---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: a0dddf6e7cc5080ca4028b1348381c1b5fb72df6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926398"
---
# <span data-ttu-id="acc3e-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="acc3e-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="acc3e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="acc3e-102">SYNOPSIS</span></span>
<span data-ttu-id="acc3e-103">Hämtar fråge nycklar för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="acc3e-103">Gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="acc3e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="acc3e-104">SYNTAX</span></span>

### <span data-ttu-id="acc3e-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="acc3e-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc3e-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="acc3e-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="acc3e-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="acc3e-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="acc3e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="acc3e-108">DESCRIPTION</span></span>
<span data-ttu-id="acc3e-109">Cmdleten **Get-AzSearchQueryKey** hämtar fråge nycklar för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="acc3e-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="acc3e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="acc3e-110">EXAMPLES</span></span>

### <span data-ttu-id="acc3e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="acc3e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="acc3e-112">Exemplet får alla fråge nycklar för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="acc3e-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="acc3e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="acc3e-113">PARAMETERS</span></span>

### <span data-ttu-id="acc3e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc3e-114">-DefaultProfile</span></span>
<span data-ttu-id="acc3e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="acc3e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acc3e-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="acc3e-116">-ParentObject</span></span>
<span data-ttu-id="acc3e-117">Objekt för Sök tjänst.</span><span class="sxs-lookup"><span data-stu-id="acc3e-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="acc3e-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="acc3e-118">-ParentResourceId</span></span>
<span data-ttu-id="acc3e-119">Sök tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="acc3e-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="acc3e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acc3e-120">-ResourceGroupName</span></span>
<span data-ttu-id="acc3e-121">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="acc3e-121">Resource Group name.</span></span>

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

### <span data-ttu-id="acc3e-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="acc3e-122">-ServiceName</span></span>
<span data-ttu-id="acc3e-123">Sök tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="acc3e-123">Search Service name.</span></span>

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

### <span data-ttu-id="acc3e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc3e-124">CommonParameters</span></span>
<span data-ttu-id="acc3e-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acc3e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc3e-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acc3e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc3e-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="acc3e-127">INPUTS</span></span>

### <span data-ttu-id="acc3e-128">Microsoft. Azure. commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="acc3e-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="acc3e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="acc3e-129">System.String</span></span>

## <span data-ttu-id="acc3e-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="acc3e-130">OUTPUTS</span></span>

### <span data-ttu-id="acc3e-131">Microsoft. Azure. commands. Management. search. Models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="acc3e-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="acc3e-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="acc3e-132">NOTES</span></span>

## <span data-ttu-id="acc3e-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="acc3e-133">RELATED LINKS</span></span>

[<span data-ttu-id="acc3e-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="acc3e-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="acc3e-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="acc3e-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)