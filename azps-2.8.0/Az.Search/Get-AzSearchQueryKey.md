---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: 9283fb0a2fd366029a5ca2bc618daf7ad8a3de3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920013"
---
# <span data-ttu-id="1b2e9-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="1b2e9-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="1b2e9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b2e9-102">SYNOPSIS</span></span>
<span data-ttu-id="1b2e9-103">Hämtar fråge nycklar för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1b2e9-103">Gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="1b2e9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b2e9-104">SYNTAX</span></span>

### <span data-ttu-id="1b2e9-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1b2e9-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b2e9-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b2e9-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b2e9-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b2e9-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b2e9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b2e9-108">DESCRIPTION</span></span>
<span data-ttu-id="1b2e9-109">Cmdleten **Get-AzSearchQueryKey** hämtar fråge nycklar för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1b2e9-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="1b2e9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b2e9-110">EXAMPLES</span></span>

### <span data-ttu-id="1b2e9-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1b2e9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="1b2e9-112">Exemplet får alla fråge nycklar för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1b2e9-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="1b2e9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b2e9-113">PARAMETERS</span></span>

### <span data-ttu-id="1b2e9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b2e9-114">-DefaultProfile</span></span>
<span data-ttu-id="1b2e9-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1b2e9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b2e9-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1b2e9-116">-ParentObject</span></span>
<span data-ttu-id="1b2e9-117">Objekt för Sök tjänst.</span><span class="sxs-lookup"><span data-stu-id="1b2e9-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="1b2e9-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1b2e9-118">-ParentResourceId</span></span>
<span data-ttu-id="1b2e9-119">Sök tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="1b2e9-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="1b2e9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b2e9-120">-ResourceGroupName</span></span>
<span data-ttu-id="1b2e9-121">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="1b2e9-121">Resource Group name.</span></span>

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

### <span data-ttu-id="1b2e9-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1b2e9-122">-ServiceName</span></span>
<span data-ttu-id="1b2e9-123">Sök tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="1b2e9-123">Search Service name.</span></span>

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

### <span data-ttu-id="1b2e9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b2e9-124">CommonParameters</span></span>
<span data-ttu-id="1b2e9-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b2e9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b2e9-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b2e9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b2e9-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b2e9-127">INPUTS</span></span>

### <span data-ttu-id="1b2e9-128">Microsoft. Azure. commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="1b2e9-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="1b2e9-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1b2e9-129">System.String</span></span>

## <span data-ttu-id="1b2e9-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b2e9-130">OUTPUTS</span></span>

### <span data-ttu-id="1b2e9-131">Microsoft. Azure. commands. Management. search. Models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="1b2e9-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="1b2e9-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b2e9-132">NOTES</span></span>

## <span data-ttu-id="1b2e9-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b2e9-133">RELATED LINKS</span></span>

[<span data-ttu-id="1b2e9-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="1b2e9-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="1b2e9-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="1b2e9-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)