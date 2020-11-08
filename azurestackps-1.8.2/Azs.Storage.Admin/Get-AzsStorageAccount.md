---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b4ec0639e31df3766550d6f7acc655cd3b5608bf
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100123"
---
# <span data-ttu-id="48c7c-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48c7c-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="48c7c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48c7c-102">SYNOPSIS</span></span>
<span data-ttu-id="48c7c-103">Returnerar det begärda lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="48c7c-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="48c7c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48c7c-104">SYNTAX</span></span>

### <span data-ttu-id="48c7c-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="48c7c-105">List (Default)</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-ResourceGroupName <String>] [-Summary] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="48c7c-106">Lära</span><span class="sxs-lookup"><span data-stu-id="48c7c-106">Get</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="48c7c-107">ID</span><span class="sxs-lookup"><span data-stu-id="48c7c-107">ResourceId</span></span>
```
Get-AzsStorageAccount [-ResourceId <String>] [<CommonParameters>]
```

## <span data-ttu-id="48c7c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48c7c-108">DESCRIPTION</span></span>
<span data-ttu-id="48c7c-109">Returnerar det begärda lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="48c7c-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="48c7c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48c7c-110">EXAMPLES</span></span>

### <span data-ttu-id="48c7c-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="48c7c-111">EXAMPLE 1</span></span>
```
Get-AzsStorageAccount -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Summary
```

<span data-ttu-id="48c7c-112">Få en lista med lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="48c7c-112">Get a list of storage accounts.</span></span>

### <span data-ttu-id="48c7c-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="48c7c-113">EXAMPLE 2</span></span>
```
Get-AzsStorageAccount -FarmName 431e8245-9e38-43e9-bf73-5f9cb2fbbdb6 -Name f8f7ff7335cb4ba284fb855547e48f34
```

<span data-ttu-id="48c7c-114">Få information om det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="48c7c-114">Get details of the specified storage account.</span></span>

## <span data-ttu-id="48c7c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48c7c-115">PARAMETERS</span></span>

### <span data-ttu-id="48c7c-116">-FarmName</span><span class="sxs-lookup"><span data-stu-id="48c7c-116">-FarmName</span></span>
<span data-ttu-id="48c7c-117">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="48c7c-117">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c7c-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="48c7c-118">-Name</span></span>
<span data-ttu-id="48c7c-119">Internt lagrings konto-ID som inte är synligt för klient organisationen.</span><span class="sxs-lookup"><span data-stu-id="48c7c-119">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c7c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48c7c-120">-ResourceGroupName</span></span>
<span data-ttu-id="48c7c-121">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="48c7c-121">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c7c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48c7c-122">-ResourceId</span></span>
<span data-ttu-id="48c7c-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="48c7c-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48c7c-124">-Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48c7c-124">-Summary</span></span>
<span data-ttu-id="48c7c-125">Växeln för wheter-Sammanfattning eller detaljerad information returneras.</span><span class="sxs-lookup"><span data-stu-id="48c7c-125">Switch for wheter summary or detailed information is returned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c7c-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="48c7c-126">-Skip</span></span>
<span data-ttu-id="48c7c-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="48c7c-127">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c7c-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="48c7c-128">-Top</span></span>
<span data-ttu-id="48c7c-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="48c7c-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="48c7c-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="48c7c-130">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c7c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48c7c-131">CommonParameters</span></span>
<span data-ttu-id="48c7c-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48c7c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48c7c-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48c7c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48c7c-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48c7c-134">INPUTS</span></span>

## <span data-ttu-id="48c7c-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48c7c-135">OUTPUTS</span></span>

### <span data-ttu-id="48c7c-136">Microsoft. AzureStack. Management. Storage. admin. Models. StorageAccount</span><span class="sxs-lookup"><span data-stu-id="48c7c-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageAccount</span></span>

## <span data-ttu-id="48c7c-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48c7c-137">NOTES</span></span>

## <span data-ttu-id="48c7c-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48c7c-138">RELATED LINKS</span></span>
