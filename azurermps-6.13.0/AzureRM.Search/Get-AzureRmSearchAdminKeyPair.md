---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchAdminKeyPair.md
ms.openlocfilehash: 92b2e7304c0f837e47f7464e84769478902c973a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579999"
---
# <span data-ttu-id="aa7f9-101">Get-AzureRmSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="aa7f9-101">Get-AzureRmSearchAdminKeyPair</span></span>

## <span data-ttu-id="aa7f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aa7f9-102">SYNOPSIS</span></span>
<span data-ttu-id="aa7f9-103">Hämtar administratörs nyckel paret för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="aa7f9-103">Gets admin key pair of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa7f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aa7f9-104">SYNTAX</span></span>

### <span data-ttu-id="aa7f9-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="aa7f9-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa7f9-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa7f9-106">ParentObjectParameterSet</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aa7f9-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa7f9-107">ParentResourceIdParameterSet</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa7f9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aa7f9-108">DESCRIPTION</span></span>
<span data-ttu-id="aa7f9-109">Cmdleten **Get-AzureRmSearchAdminKeyPair** hämtar administratörs nyckel paret för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="aa7f9-109">The **Get-AzureRmSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="aa7f9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aa7f9-110">EXAMPLES</span></span>

### <span data-ttu-id="aa7f9-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="aa7f9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="aa7f9-112">Exemplet får administratörs nyckel paret för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="aa7f9-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="aa7f9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aa7f9-113">PARAMETERS</span></span>

### <span data-ttu-id="aa7f9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa7f9-114">-DefaultProfile</span></span>
<span data-ttu-id="aa7f9-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="aa7f9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa7f9-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="aa7f9-116">-ParentObject</span></span>
<span data-ttu-id="aa7f9-117">Objekt för Sök tjänst.</span><span class="sxs-lookup"><span data-stu-id="aa7f9-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="aa7f9-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="aa7f9-118">-ParentResourceId</span></span>
<span data-ttu-id="aa7f9-119">Sök tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="aa7f9-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="aa7f9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa7f9-120">-ResourceGroupName</span></span>
<span data-ttu-id="aa7f9-121">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="aa7f9-121">Resource Group name.</span></span>

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

### <span data-ttu-id="aa7f9-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="aa7f9-122">-ServiceName</span></span>
<span data-ttu-id="aa7f9-123">Sök tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="aa7f9-123">Search Service name.</span></span>

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

### <span data-ttu-id="aa7f9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa7f9-124">CommonParameters</span></span>
<span data-ttu-id="aa7f9-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa7f9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa7f9-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa7f9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa7f9-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aa7f9-127">INPUTS</span></span>

### <span data-ttu-id="aa7f9-128">Microsoft. Azure. commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="aa7f9-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="aa7f9-129">Parametrar: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="aa7f9-129">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="aa7f9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="aa7f9-130">System.String</span></span>

## <span data-ttu-id="aa7f9-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aa7f9-131">OUTPUTS</span></span>

### <span data-ttu-id="aa7f9-132">Microsoft. Azure. commands. Management. search. Models. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="aa7f9-132">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="aa7f9-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aa7f9-133">NOTES</span></span>

## <span data-ttu-id="aa7f9-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aa7f9-134">RELATED LINKS</span></span>

[<span data-ttu-id="aa7f9-135">New-AzureRmSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="aa7f9-135">New-AzureRmSearchAdminKey</span></span>](./New-AzureRmSearchAdminKey.md)
