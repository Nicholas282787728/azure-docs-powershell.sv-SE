---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: a0dddf6e7cc5080ca4028b1348381c1b5fb72df6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522291"
---
# <span data-ttu-id="a3bf0-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="a3bf0-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="a3bf0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3bf0-102">SYNOPSIS</span></span>
<span data-ttu-id="a3bf0-103">Hämtar fråge nycklar för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a3bf0-103">Gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="a3bf0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3bf0-104">SYNTAX</span></span>

### <span data-ttu-id="a3bf0-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a3bf0-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3bf0-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3bf0-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3bf0-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3bf0-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3bf0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3bf0-108">DESCRIPTION</span></span>
<span data-ttu-id="a3bf0-109">Cmdleten **Get-AzSearchQueryKey** hämtar fråge nycklar för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a3bf0-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="a3bf0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3bf0-110">EXAMPLES</span></span>

### <span data-ttu-id="a3bf0-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a3bf0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="a3bf0-112">Exemplet får alla fråge nycklar för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a3bf0-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="a3bf0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3bf0-113">PARAMETERS</span></span>

### <span data-ttu-id="a3bf0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3bf0-114">-DefaultProfile</span></span>
<span data-ttu-id="a3bf0-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a3bf0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3bf0-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a3bf0-116">-ParentObject</span></span>
<span data-ttu-id="a3bf0-117">Objekt för Sök tjänst.</span><span class="sxs-lookup"><span data-stu-id="a3bf0-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="a3bf0-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a3bf0-118">-ParentResourceId</span></span>
<span data-ttu-id="a3bf0-119">Sök tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="a3bf0-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="a3bf0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3bf0-120">-ResourceGroupName</span></span>
<span data-ttu-id="a3bf0-121">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="a3bf0-121">Resource Group name.</span></span>

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

### <span data-ttu-id="a3bf0-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a3bf0-122">-ServiceName</span></span>
<span data-ttu-id="a3bf0-123">Sök tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="a3bf0-123">Search Service name.</span></span>

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

### <span data-ttu-id="a3bf0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3bf0-124">CommonParameters</span></span>
<span data-ttu-id="a3bf0-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3bf0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3bf0-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3bf0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3bf0-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3bf0-127">INPUTS</span></span>

### <span data-ttu-id="a3bf0-128">Microsoft. Azure. commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="a3bf0-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="a3bf0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a3bf0-129">System.String</span></span>

## <span data-ttu-id="a3bf0-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3bf0-130">OUTPUTS</span></span>

### <span data-ttu-id="a3bf0-131">Microsoft. Azure. commands. Management. search. Models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="a3bf0-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="a3bf0-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3bf0-132">NOTES</span></span>

## <span data-ttu-id="a3bf0-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3bf0-133">RELATED LINKS</span></span>

[<span data-ttu-id="a3bf0-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="a3bf0-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="a3bf0-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="a3bf0-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)