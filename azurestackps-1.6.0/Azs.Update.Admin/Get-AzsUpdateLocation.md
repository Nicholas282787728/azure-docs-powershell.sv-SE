---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9234cb73b1f9c3652827293ae2813f78d7ce336
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93755014"
---
# <span data-ttu-id="32367-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="32367-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="32367-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="32367-102">SYNOPSIS</span></span>
<span data-ttu-id="32367-103">Hämta listan med uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="32367-103">Get the list of update locations.</span></span>

## <span data-ttu-id="32367-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="32367-104">SYNTAX</span></span>

### <span data-ttu-id="32367-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="32367-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="32367-106">Lära</span><span class="sxs-lookup"><span data-stu-id="32367-106">Get</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="32367-107">ID</span><span class="sxs-lookup"><span data-stu-id="32367-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="32367-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="32367-108">DESCRIPTION</span></span>
<span data-ttu-id="32367-109">Hämta listan med uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="32367-109">Get the list of update locations.</span></span> <span data-ttu-id="32367-110">Platserna som returneras kan användas för att hämta tillgängliga uppdateringar på en viss plats med Get-AzsUpdate.</span><span class="sxs-lookup"><span data-stu-id="32367-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="32367-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="32367-111">EXAMPLES</span></span>

### <span data-ttu-id="32367-112">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="32367-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="32367-113">Hämta listan med uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="32367-113">Get the list of update locations.</span></span>

## <span data-ttu-id="32367-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="32367-114">PARAMETERS</span></span>

### <span data-ttu-id="32367-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="32367-115">-Name</span></span>
<span data-ttu-id="32367-116">Namnet på uppdaterings platsen.</span><span class="sxs-lookup"><span data-stu-id="32367-116">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32367-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32367-117">-ResourceGroupName</span></span>
<span data-ttu-id="32367-118">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="32367-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="32367-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32367-119">-ResourceId</span></span>
<span data-ttu-id="32367-120">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="32367-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32367-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32367-121">CommonParameters</span></span>
<span data-ttu-id="32367-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32367-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32367-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32367-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32367-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="32367-124">INPUTS</span></span>

## <span data-ttu-id="32367-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="32367-125">OUTPUTS</span></span>

### <span data-ttu-id="32367-126">Microsoft. AzureStack. Management. Update. admin. Models. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="32367-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="32367-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="32367-127">NOTES</span></span>

## <span data-ttu-id="32367-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="32367-128">RELATED LINKS</span></span>

