---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchQueryKey.md
ms.openlocfilehash: 3535e9d7723c87e0f528192e47c921d3835ff9e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575085"
---
# <span data-ttu-id="c5f70-101">Get-AzureRmSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="c5f70-101">Get-AzureRmSearchQueryKey</span></span>

## <span data-ttu-id="c5f70-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c5f70-102">SYNOPSIS</span></span>
<span data-ttu-id="c5f70-103">Hämtar fråge nycklar för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c5f70-103">Gets query key(s) of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5f70-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c5f70-104">SYNTAX</span></span>

### <span data-ttu-id="c5f70-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c5f70-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5f70-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5f70-106">ParentObjectParameterSet</span></span>
```
Get-AzureRmSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5f70-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5f70-107">ParentResourceIdParameterSet</span></span>
```
Get-AzureRmSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5f70-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c5f70-108">DESCRIPTION</span></span>
<span data-ttu-id="c5f70-109">Cmdleten **Get-AzureRmSearchQueryKey** hämtar fråge nycklar för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c5f70-109">The **Get-AzureRmSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="c5f70-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c5f70-110">EXAMPLES</span></span>

### <span data-ttu-id="c5f70-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c5f70-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="c5f70-112">Exemplet får alla fråge nycklar för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c5f70-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="c5f70-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c5f70-113">PARAMETERS</span></span>

### <span data-ttu-id="c5f70-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5f70-114">-DefaultProfile</span></span>
<span data-ttu-id="c5f70-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c5f70-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5f70-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c5f70-116">-ParentObject</span></span>
<span data-ttu-id="c5f70-117">Objekt för Sök tjänst.</span><span class="sxs-lookup"><span data-stu-id="c5f70-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="c5f70-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c5f70-118">-ParentResourceId</span></span>
<span data-ttu-id="c5f70-119">Sök tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="c5f70-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="c5f70-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5f70-120">-ResourceGroupName</span></span>
<span data-ttu-id="c5f70-121">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="c5f70-121">Resource Group name.</span></span>

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

### <span data-ttu-id="c5f70-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c5f70-122">-ServiceName</span></span>
<span data-ttu-id="c5f70-123">Sök tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="c5f70-123">Search Service name.</span></span>

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

### <span data-ttu-id="c5f70-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5f70-124">CommonParameters</span></span>
<span data-ttu-id="c5f70-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5f70-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5f70-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5f70-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5f70-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c5f70-127">INPUTS</span></span>

### <span data-ttu-id="c5f70-128">Microsoft. Azure. commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="c5f70-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="c5f70-129">Parametrar: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c5f70-129">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="c5f70-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c5f70-130">System.String</span></span>

## <span data-ttu-id="c5f70-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c5f70-131">OUTPUTS</span></span>

### <span data-ttu-id="c5f70-132">Microsoft. Azure. commands. Management. search. Models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="c5f70-132">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="c5f70-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c5f70-133">NOTES</span></span>

## <span data-ttu-id="c5f70-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c5f70-134">RELATED LINKS</span></span>

[<span data-ttu-id="c5f70-135">New-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="c5f70-135">New-AzureRmSearchQueryKey.md</span></span>](./New-AzureRmSearchQueryKey.md)

[<span data-ttu-id="c5f70-136">Remove-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="c5f70-136">Remove-AzureRmSearchQueryKey.md</span></span>](./Remove-AzureRmSearchQueryKey.md)
