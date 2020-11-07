---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3ae30d06970d9533c32c96f33a1917fa8d2a6e41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921162"
---
# <span data-ttu-id="ce0a8-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="ce0a8-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="ce0a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce0a8-102">SYNOPSIS</span></span>
<span data-ttu-id="ce0a8-103">Visar alla katalog innehavare under aktuell prenumeration och angivet resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="ce0a8-103">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="ce0a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce0a8-104">SYNTAX</span></span>

### <span data-ttu-id="ce0a8-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="ce0a8-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="ce0a8-106">Lära</span><span class="sxs-lookup"><span data-stu-id="ce0a8-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="ce0a8-107">ID</span><span class="sxs-lookup"><span data-stu-id="ce0a8-107">ResourceId</span></span>
```
Get-AzsDirectoryTenant -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ce0a8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce0a8-108">DESCRIPTION</span></span>
<span data-ttu-id="ce0a8-109">Visar alla katalog innehavare under aktuell prenumeration och angivet resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="ce0a8-109">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="ce0a8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce0a8-110">EXAMPLES</span></span>

### <span data-ttu-id="ce0a8-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ce0a8-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName "System.Local"
```

<span data-ttu-id="ce0a8-112">Visar alla katalog innehavare under aktuell prenumeration och angivet resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="ce0a8-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="ce0a8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce0a8-113">PARAMETERS</span></span>

### <span data-ttu-id="ce0a8-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="ce0a8-114">-Name</span></span>
<span data-ttu-id="ce0a8-115">Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="ce0a8-115">Directory tenant name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0a8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce0a8-116">-ResourceGroupName</span></span>
<span data-ttu-id="ce0a8-117">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="ce0a8-117">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="ce0a8-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce0a8-118">-ResourceId</span></span>
<span data-ttu-id="ce0a8-119">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ce0a8-119">The resource id.</span></span>

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

### <span data-ttu-id="ce0a8-120">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="ce0a8-120">-Skip</span></span>
<span data-ttu-id="ce0a8-121">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="ce0a8-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ce0a8-122">-Överst</span><span class="sxs-lookup"><span data-stu-id="ce0a8-122">-Top</span></span>
<span data-ttu-id="ce0a8-123">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="ce0a8-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ce0a8-124">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="ce0a8-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ce0a8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce0a8-125">CommonParameters</span></span>
<span data-ttu-id="ce0a8-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce0a8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce0a8-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce0a8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce0a8-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce0a8-128">INPUTS</span></span>

## <span data-ttu-id="ce0a8-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce0a8-129">OUTPUTS</span></span>

### <span data-ttu-id="ce0a8-130">Microsoft. AzureStack. Management. abonnemang. admin. Models. DirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="ce0a8-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DirectoryTenant</span></span>

## <span data-ttu-id="ce0a8-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce0a8-131">NOTES</span></span>

## <span data-ttu-id="ce0a8-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce0a8-132">RELATED LINKS</span></span>

