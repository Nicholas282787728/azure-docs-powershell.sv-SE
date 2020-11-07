---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dd280133b3a0bc536c57f839fcc0faab81669c03
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921787"
---
# <span data-ttu-id="6ddc0-101">Get-AzsStorageFarm</span><span class="sxs-lookup"><span data-stu-id="6ddc0-101">Get-AzsStorageFarm</span></span>

## <span data-ttu-id="6ddc0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6ddc0-102">SYNOPSIS</span></span>
<span data-ttu-id="6ddc0-103">Returnerar en lista över alla lagrings grupper.</span><span class="sxs-lookup"><span data-stu-id="6ddc0-103">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="6ddc0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6ddc0-104">SYNTAX</span></span>

### <span data-ttu-id="6ddc0-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="6ddc0-105">List (Default)</span></span>
```
Get-AzsStorageFarm [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6ddc0-106">Lära</span><span class="sxs-lookup"><span data-stu-id="6ddc0-106">Get</span></span>
```
Get-AzsStorageFarm [-Name] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="6ddc0-107">ID</span><span class="sxs-lookup"><span data-stu-id="6ddc0-107">ResourceId</span></span>
```
Get-AzsStorageFarm -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6ddc0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6ddc0-108">DESCRIPTION</span></span>
<span data-ttu-id="6ddc0-109">Returnerar en lista över alla lagrings grupper.</span><span class="sxs-lookup"><span data-stu-id="6ddc0-109">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="6ddc0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6ddc0-110">EXAMPLES</span></span>

### <span data-ttu-id="6ddc0-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="6ddc0-111">EXAMPLE 1</span></span>
```
Get-AzsStorageFarm
```

<span data-ttu-id="6ddc0-112">Få en lista över alla lagrings grupper.</span><span class="sxs-lookup"><span data-stu-id="6ddc0-112">Get the list of all storage farms.</span></span>

## <span data-ttu-id="6ddc0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6ddc0-113">PARAMETERS</span></span>

### <span data-ttu-id="6ddc0-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="6ddc0-114">-Name</span></span>
<span data-ttu-id="6ddc0-115">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="6ddc0-115">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ddc0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ddc0-116">-ResourceGroupName</span></span>
<span data-ttu-id="6ddc0-117">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="6ddc0-117">Resource group name.</span></span>

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

### <span data-ttu-id="6ddc0-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ddc0-118">-ResourceId</span></span>
<span data-ttu-id="6ddc0-119">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="6ddc0-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ddc0-120">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="6ddc0-120">-Skip</span></span>
<span data-ttu-id="6ddc0-121">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="6ddc0-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="6ddc0-122">-Överst</span><span class="sxs-lookup"><span data-stu-id="6ddc0-122">-Top</span></span>
<span data-ttu-id="6ddc0-123">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="6ddc0-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6ddc0-124">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="6ddc0-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6ddc0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ddc0-125">CommonParameters</span></span>
<span data-ttu-id="6ddc0-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ddc0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ddc0-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ddc0-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ddc0-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6ddc0-128">INPUTS</span></span>

## <span data-ttu-id="6ddc0-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6ddc0-129">OUTPUTS</span></span>

### <span data-ttu-id="6ddc0-130">Microsoft. AzureStack. Management. Storage. admin. Models. Server grupp</span><span class="sxs-lookup"><span data-stu-id="6ddc0-130">Microsoft.AzureStack.Management.Storage.Admin.Models.Farm</span></span>

## <span data-ttu-id="6ddc0-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6ddc0-131">NOTES</span></span>

## <span data-ttu-id="6ddc0-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6ddc0-132">RELATED LINKS</span></span>
