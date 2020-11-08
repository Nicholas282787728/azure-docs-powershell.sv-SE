---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83d47f93addf05af19b523db6ba454443af2c34f
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/26/2020
ms.locfileid: "94100572"
---
# <span data-ttu-id="6df7a-101">Get-AzsAzureBridgeActivation</span><span class="sxs-lookup"><span data-stu-id="6df7a-101">Get-AzsAzureBridgeActivation</span></span>

## <span data-ttu-id="6df7a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6df7a-102">SYNOPSIS</span></span>
<span data-ttu-id="6df7a-103">Returnerar aktiveringen av Azure-bryggan.</span><span class="sxs-lookup"><span data-stu-id="6df7a-103">Returns the Azure Bridge Activation.</span></span>

## <span data-ttu-id="6df7a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6df7a-104">SYNTAX</span></span>

### <span data-ttu-id="6df7a-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="6df7a-105">List (Default)</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6df7a-106">Lära</span><span class="sxs-lookup"><span data-stu-id="6df7a-106">Get</span></span>
```
Get-AzsAzureBridgeActivation -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="6df7a-107">ID</span><span class="sxs-lookup"><span data-stu-id="6df7a-107">ResourceId</span></span>
```
Get-AzsAzureBridgeActivation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6df7a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6df7a-108">DESCRIPTION</span></span>
<span data-ttu-id="6df7a-109">När Azure-stacken har registrerats innehåller aktiverings objektet information som länkar en Azure Stack-distribution till dess registrering i Azure, till exempel förfallo datum, namn, etc.</span><span class="sxs-lookup"><span data-stu-id="6df7a-109">Once Azure Stack has been registered, the activation object contains information that links an Azure Stack deployment to its registration in Azure, for example, the registration expiration date, name, etc.</span></span>

## <span data-ttu-id="6df7a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6df7a-110">EXAMPLES</span></span>

### <span data-ttu-id="6df7a-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6df7a-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName 'activationRG'
```

<span data-ttu-id="6df7a-112">Få en lista med Azure Bridge-aktiveringar under resurs gruppen "activationRG"</span><span class="sxs-lookup"><span data-stu-id="6df7a-112">Get a list of Azure Bridge Activations under the resource group "activationRG"</span></span>

### <span data-ttu-id="6df7a-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="6df7a-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeActivation -Name 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="6df7a-114">Få en Azure Bridge-aktivering med namn ' aktiveringsbegäran ' under ' activationRG '</span><span class="sxs-lookup"><span data-stu-id="6df7a-114">Get an Azure Bridge Activation by name 'myActivation' situated under 'activationRG'</span></span>

## <span data-ttu-id="6df7a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6df7a-115">PARAMETERS</span></span>

### <span data-ttu-id="6df7a-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="6df7a-116">-Name</span></span>
<span data-ttu-id="6df7a-117">Namn på aktiveringen.</span><span class="sxs-lookup"><span data-stu-id="6df7a-117">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df7a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6df7a-118">-ResourceGroupName</span></span>
<span data-ttu-id="6df7a-119">Resurs gruppen som används vid registrering av Azure Stack; Du kan också Visa resurs grupp namn i portalen.</span><span class="sxs-lookup"><span data-stu-id="6df7a-119">The Resource Group used during the registration of Azure Stack; you can also view Resource Group names in the portal.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df7a-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6df7a-120">-ResourceId</span></span>
<span data-ttu-id="6df7a-121">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="6df7a-121">The resource id.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df7a-122">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="6df7a-122">-Skip</span></span>
<span data-ttu-id="6df7a-123">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="6df7a-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="6df7a-124">-Överst</span><span class="sxs-lookup"><span data-stu-id="6df7a-124">-Top</span></span>
<span data-ttu-id="6df7a-125">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="6df7a-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6df7a-126">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="6df7a-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6df7a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6df7a-127">CommonParameters</span></span>
<span data-ttu-id="6df7a-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6df7a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6df7a-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6df7a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6df7a-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6df7a-130">INPUTS</span></span>

## <span data-ttu-id="6df7a-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6df7a-131">OUTPUTS</span></span>

### <span data-ttu-id="6df7a-132">Microsoft. AzureStack. Management. AzureBridge. admin. Models. ActivationResource</span><span class="sxs-lookup"><span data-stu-id="6df7a-132">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ActivationResource</span></span>

## <span data-ttu-id="6df7a-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6df7a-133">NOTES</span></span>

## <span data-ttu-id="6df7a-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6df7a-134">RELATED LINKS</span></span>

