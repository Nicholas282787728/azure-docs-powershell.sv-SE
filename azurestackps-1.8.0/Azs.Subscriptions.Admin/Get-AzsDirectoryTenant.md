---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: eff689d36268f7eaec045c05c00d4fd18e91a026
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921517"
---
# <span data-ttu-id="7c80d-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="7c80d-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="7c80d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7c80d-102">SYNOPSIS</span></span>
<span data-ttu-id="7c80d-103">Visar alla katalog innehavare under aktuell prenumeration och angivet resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="7c80d-103">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="7c80d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7c80d-104">SYNTAX</span></span>

### <span data-ttu-id="7c80d-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="7c80d-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="7c80d-106">Lära</span><span class="sxs-lookup"><span data-stu-id="7c80d-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="7c80d-107">ID</span><span class="sxs-lookup"><span data-stu-id="7c80d-107">ResourceId</span></span>
```
Get-AzsDirectoryTenant -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="7c80d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7c80d-108">DESCRIPTION</span></span>
<span data-ttu-id="7c80d-109">Visar alla katalog innehavare under aktuell prenumeration och angivet resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="7c80d-109">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="7c80d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7c80d-110">EXAMPLES</span></span>

### <span data-ttu-id="7c80d-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7c80d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName "System.Local"
```

<span data-ttu-id="7c80d-112">Visar alla katalog innehavare under aktuell prenumeration och angivet resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="7c80d-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="7c80d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7c80d-113">PARAMETERS</span></span>

### <span data-ttu-id="7c80d-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="7c80d-114">-Name</span></span>
<span data-ttu-id="7c80d-115">Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="7c80d-115">Directory tenant name.</span></span>

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

### <span data-ttu-id="7c80d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c80d-116">-ResourceGroupName</span></span>
<span data-ttu-id="7c80d-117">{{Fill ResourceGroupName Description}}</span><span class="sxs-lookup"><span data-stu-id="7c80d-117">{{Fill ResourceGroupName Description}}</span></span>

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

### <span data-ttu-id="7c80d-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c80d-118">-ResourceId</span></span>
<span data-ttu-id="7c80d-119">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="7c80d-119">The resource id.</span></span>

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

### <span data-ttu-id="7c80d-120">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="7c80d-120">-Skip</span></span>
<span data-ttu-id="7c80d-121">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="7c80d-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="7c80d-122">-Överst</span><span class="sxs-lookup"><span data-stu-id="7c80d-122">-Top</span></span>
<span data-ttu-id="7c80d-123">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="7c80d-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="7c80d-124">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="7c80d-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="7c80d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c80d-125">CommonParameters</span></span>
<span data-ttu-id="7c80d-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c80d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c80d-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c80d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c80d-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7c80d-128">INPUTS</span></span>

## <span data-ttu-id="7c80d-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7c80d-129">OUTPUTS</span></span>

### <span data-ttu-id="7c80d-130">Microsoft. AzureStack. Management. abonnemang. admin. Models. DirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="7c80d-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DirectoryTenant</span></span>

## <span data-ttu-id="7c80d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7c80d-131">NOTES</span></span>

## <span data-ttu-id="7c80d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7c80d-132">RELATED LINKS</span></span>

