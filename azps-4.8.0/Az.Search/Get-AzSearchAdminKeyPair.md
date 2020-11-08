---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: dafc9da9669a7c07f982e4fee87a37e1581af40a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259886"
---
# <span data-ttu-id="f71da-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="f71da-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="f71da-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f71da-102">SYNOPSIS</span></span>
<span data-ttu-id="f71da-103">Hämtar administratörs nyckel paret för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f71da-103">Gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="f71da-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f71da-104">SYNTAX</span></span>

### <span data-ttu-id="f71da-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f71da-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f71da-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f71da-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f71da-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f71da-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f71da-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f71da-108">DESCRIPTION</span></span>
<span data-ttu-id="f71da-109">Cmdleten **Get-AzSearchAdminKeyPair** hämtar administratörs nyckel paret för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f71da-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="f71da-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f71da-110">EXAMPLES</span></span>

### <span data-ttu-id="f71da-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f71da-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="f71da-112">Exemplet får administratörs nyckel paret för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f71da-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="f71da-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f71da-113">PARAMETERS</span></span>

### <span data-ttu-id="f71da-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f71da-114">-DefaultProfile</span></span>
<span data-ttu-id="f71da-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f71da-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f71da-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f71da-116">-ParentObject</span></span>
<span data-ttu-id="f71da-117">Objekt för Sök tjänst.</span><span class="sxs-lookup"><span data-stu-id="f71da-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="f71da-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f71da-118">-ParentResourceId</span></span>
<span data-ttu-id="f71da-119">Sök tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="f71da-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="f71da-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f71da-120">-ResourceGroupName</span></span>
<span data-ttu-id="f71da-121">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="f71da-121">Resource Group name.</span></span>

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

### <span data-ttu-id="f71da-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f71da-122">-ServiceName</span></span>
<span data-ttu-id="f71da-123">Sök tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="f71da-123">Search Service name.</span></span>

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

### <span data-ttu-id="f71da-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f71da-124">CommonParameters</span></span>
<span data-ttu-id="f71da-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f71da-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f71da-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f71da-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f71da-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f71da-127">INPUTS</span></span>

### <span data-ttu-id="f71da-128">Microsoft. Azure. commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="f71da-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="f71da-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f71da-129">System.String</span></span>

## <span data-ttu-id="f71da-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f71da-130">OUTPUTS</span></span>

### <span data-ttu-id="f71da-131">Microsoft. Azure. commands. Management. search. Models. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="f71da-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="f71da-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f71da-132">NOTES</span></span>

## <span data-ttu-id="f71da-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f71da-133">RELATED LINKS</span></span>

[<span data-ttu-id="f71da-134">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="f71da-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)
