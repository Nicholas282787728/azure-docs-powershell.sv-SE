---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 811a69b8d18c5e723702f73873188961f2739360
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/22/2020
ms.locfileid: "93931678"
---
# <span data-ttu-id="a5e90-101">Get-AzsAzureBridgeActivation</span><span class="sxs-lookup"><span data-stu-id="a5e90-101">Get-AzsAzureBridgeActivation</span></span>

## <span data-ttu-id="a5e90-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5e90-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e90-103">Returnerar aktiveringen av Azure-bryggan.</span><span class="sxs-lookup"><span data-stu-id="a5e90-103">Returns the Azure Bridge Activation.</span></span>

## <span data-ttu-id="a5e90-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5e90-104">SYNTAX</span></span>

### <span data-ttu-id="a5e90-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="a5e90-105">List (Default)</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a5e90-106">Lära</span><span class="sxs-lookup"><span data-stu-id="a5e90-106">Get</span></span>
```
Get-AzsAzureBridgeActivation -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="a5e90-107">ID</span><span class="sxs-lookup"><span data-stu-id="a5e90-107">ResourceId</span></span>
```
Get-AzsAzureBridgeActivation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a5e90-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5e90-108">DESCRIPTION</span></span>
<span data-ttu-id="a5e90-109">När Azure-stacken har registrerats innehåller aktiverings objektet information som länkar en Azure Stack-distribution till dess registrering i Azure, till exempel förfallo datum, namn, etc.</span><span class="sxs-lookup"><span data-stu-id="a5e90-109">Once Azure Stack has been registered, the activation object contains information that links an Azure Stack deployment to its registration in Azure, for example, the registration expiration date, name, etc.</span></span>

## <span data-ttu-id="a5e90-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5e90-110">EXAMPLES</span></span>

### <span data-ttu-id="a5e90-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a5e90-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName 'activationRG'
```

<span data-ttu-id="a5e90-112">Få en lista med Azure Bridge-aktiveringar under resurs gruppen "activationRG"</span><span class="sxs-lookup"><span data-stu-id="a5e90-112">Get a list of Azure Bridge Activations under the resource group "activationRG"</span></span>

### <span data-ttu-id="a5e90-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a5e90-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeActivation -Name 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="a5e90-114">Få en Azure Bridge-aktivering med namn ' aktiveringsbegäran ' under ' activationRG '</span><span class="sxs-lookup"><span data-stu-id="a5e90-114">Get an Azure Bridge Activation by name 'myActivation' situated under 'activationRG'</span></span>

## <span data-ttu-id="a5e90-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5e90-115">PARAMETERS</span></span>

### <span data-ttu-id="a5e90-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="a5e90-116">-Name</span></span>
<span data-ttu-id="a5e90-117">Namn på aktiveringen.</span><span class="sxs-lookup"><span data-stu-id="a5e90-117">Name of the activation.</span></span>

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

### <span data-ttu-id="a5e90-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5e90-118">-ResourceGroupName</span></span>
<span data-ttu-id="a5e90-119">Resurs gruppen som används vid registrering av Azure Stack; Du kan också Visa resurs grupp namn i portalen.</span><span class="sxs-lookup"><span data-stu-id="a5e90-119">The Resource Group used during the registration of Azure Stack; you can also view Resource Group names in the portal.</span></span>

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

### <span data-ttu-id="a5e90-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5e90-120">-ResourceId</span></span>
<span data-ttu-id="a5e90-121">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="a5e90-121">The resource id.</span></span>

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

### <span data-ttu-id="a5e90-122">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="a5e90-122">-Skip</span></span>
<span data-ttu-id="a5e90-123">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="a5e90-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a5e90-124">-Överst</span><span class="sxs-lookup"><span data-stu-id="a5e90-124">-Top</span></span>
<span data-ttu-id="a5e90-125">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="a5e90-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a5e90-126">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="a5e90-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a5e90-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e90-127">CommonParameters</span></span>
<span data-ttu-id="a5e90-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5e90-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e90-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5e90-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e90-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5e90-130">INPUTS</span></span>

## <span data-ttu-id="a5e90-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5e90-131">OUTPUTS</span></span>

### <span data-ttu-id="a5e90-132">Microsoft. AzureStack. Management. AzureBridge. admin. Models. ActivationResource</span><span class="sxs-lookup"><span data-stu-id="a5e90-132">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ActivationResource</span></span>

## <span data-ttu-id="a5e90-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5e90-133">NOTES</span></span>

## <span data-ttu-id="a5e90-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5e90-134">RELATED LINKS</span></span>

