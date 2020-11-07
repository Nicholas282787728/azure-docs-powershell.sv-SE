---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: cd944184f4691b3f88934afc3a7bd9132eb23fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919263"
---
# <span data-ttu-id="88b02-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="88b02-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="88b02-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="88b02-102">SYNOPSIS</span></span>
<span data-ttu-id="88b02-103">Hämtar administratörs nyckel paret för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="88b02-103">Gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="88b02-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="88b02-104">SYNTAX</span></span>

### <span data-ttu-id="88b02-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="88b02-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88b02-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88b02-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88b02-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88b02-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88b02-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="88b02-108">DESCRIPTION</span></span>
<span data-ttu-id="88b02-109">Cmdleten **Get-AzSearchAdminKeyPair** hämtar administratörs nyckel paret för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="88b02-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="88b02-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="88b02-110">EXAMPLES</span></span>

### <span data-ttu-id="88b02-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="88b02-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="88b02-112">Exemplet får administratörs nyckel paret för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="88b02-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="88b02-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="88b02-113">PARAMETERS</span></span>

### <span data-ttu-id="88b02-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b02-114">-DefaultProfile</span></span>
<span data-ttu-id="88b02-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="88b02-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88b02-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="88b02-116">-ParentObject</span></span>
<span data-ttu-id="88b02-117">Objekt för Sök tjänst.</span><span class="sxs-lookup"><span data-stu-id="88b02-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="88b02-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="88b02-118">-ParentResourceId</span></span>
<span data-ttu-id="88b02-119">Sök tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="88b02-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="88b02-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88b02-120">-ResourceGroupName</span></span>
<span data-ttu-id="88b02-121">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="88b02-121">Resource Group name.</span></span>

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

### <span data-ttu-id="88b02-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="88b02-122">-ServiceName</span></span>
<span data-ttu-id="88b02-123">Sök tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="88b02-123">Search Service name.</span></span>

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

### <span data-ttu-id="88b02-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b02-124">CommonParameters</span></span>
<span data-ttu-id="88b02-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88b02-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b02-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88b02-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b02-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="88b02-127">INPUTS</span></span>

### <span data-ttu-id="88b02-128">Microsoft. Azure. commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="88b02-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="88b02-129">System. String</span><span class="sxs-lookup"><span data-stu-id="88b02-129">System.String</span></span>

## <span data-ttu-id="88b02-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="88b02-130">OUTPUTS</span></span>

### <span data-ttu-id="88b02-131">Microsoft. Azure. commands. Management. search. Models. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="88b02-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="88b02-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="88b02-132">NOTES</span></span>

## <span data-ttu-id="88b02-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="88b02-133">RELATED LINKS</span></span>

[<span data-ttu-id="88b02-134">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="88b02-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)
