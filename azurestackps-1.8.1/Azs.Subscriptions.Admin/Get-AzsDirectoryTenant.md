---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: eff689d36268f7eaec045c05c00d4fd18e91a026
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921676"
---
# <span data-ttu-id="b619b-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="b619b-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="b619b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b619b-102">SYNOPSIS</span></span>
<span data-ttu-id="b619b-103">Visar alla katalog innehavare under aktuell prenumeration och angivet resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="b619b-103">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="b619b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b619b-104">SYNTAX</span></span>

### <span data-ttu-id="b619b-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="b619b-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b619b-106">Lära</span><span class="sxs-lookup"><span data-stu-id="b619b-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="b619b-107">ID</span><span class="sxs-lookup"><span data-stu-id="b619b-107">ResourceId</span></span>
```
Get-AzsDirectoryTenant -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b619b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b619b-108">DESCRIPTION</span></span>
<span data-ttu-id="b619b-109">Visar alla katalog innehavare under aktuell prenumeration och angivet resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="b619b-109">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="b619b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b619b-110">EXAMPLES</span></span>

### <span data-ttu-id="b619b-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b619b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName "System.Local"
```

<span data-ttu-id="b619b-112">Visar alla katalog innehavare under aktuell prenumeration och angivet resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="b619b-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="b619b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b619b-113">PARAMETERS</span></span>

### <span data-ttu-id="b619b-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="b619b-114">-Name</span></span>
<span data-ttu-id="b619b-115">Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="b619b-115">Directory tenant name.</span></span>

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

### <span data-ttu-id="b619b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b619b-116">-ResourceGroupName</span></span>
<span data-ttu-id="b619b-117">{{Fill ResourceGroupName Description}}</span><span class="sxs-lookup"><span data-stu-id="b619b-117">{{Fill ResourceGroupName Description}}</span></span>

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

### <span data-ttu-id="b619b-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b619b-118">-ResourceId</span></span>
<span data-ttu-id="b619b-119">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b619b-119">The resource id.</span></span>

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

### <span data-ttu-id="b619b-120">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="b619b-120">-Skip</span></span>
<span data-ttu-id="b619b-121">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="b619b-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b619b-122">-Överst</span><span class="sxs-lookup"><span data-stu-id="b619b-122">-Top</span></span>
<span data-ttu-id="b619b-123">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="b619b-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b619b-124">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="b619b-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b619b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b619b-125">CommonParameters</span></span>
<span data-ttu-id="b619b-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b619b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b619b-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b619b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b619b-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b619b-128">INPUTS</span></span>

## <span data-ttu-id="b619b-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b619b-129">OUTPUTS</span></span>

### <span data-ttu-id="b619b-130">Microsoft. AzureStack. Management. abonnemang. admin. Models. DirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="b619b-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DirectoryTenant</span></span>

## <span data-ttu-id="b619b-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b619b-131">NOTES</span></span>

## <span data-ttu-id="b619b-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b619b-132">RELATED LINKS</span></span>

