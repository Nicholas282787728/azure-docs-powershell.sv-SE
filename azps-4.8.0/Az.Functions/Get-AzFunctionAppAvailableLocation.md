---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappavailablelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
ms.openlocfilehash: 3ab2ab4778b7fdb12334db416c953a7c373c63b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261295"
---
# <span data-ttu-id="e39b5-101">Get-AzFunctionAppAvailableLocation</span><span class="sxs-lookup"><span data-stu-id="e39b5-101">Get-AzFunctionAppAvailableLocation</span></span>

## <span data-ttu-id="e39b5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e39b5-102">SYNOPSIS</span></span>
<span data-ttu-id="e39b5-103">Hämtar platsen där en Function-app för den givna OS-och plan typen är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="e39b5-103">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="e39b5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e39b5-104">SYNTAX</span></span>

```
Get-AzFunctionAppAvailableLocation [[-SubscriptionId] <String[]>] [[-PlanType] <String>] [[-OSType] <String>]
 [[-DefaultProfile] <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e39b5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e39b5-105">DESCRIPTION</span></span>
<span data-ttu-id="e39b5-106">Hämtar platsen där en Function-app för den givna OS-och plan typen är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="e39b5-106">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="e39b5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e39b5-107">EXAMPLES</span></span>

### <span data-ttu-id="e39b5-108">Exempel 1: Hämta de platser där Premium är tillgängligt för Windows.</span><span class="sxs-lookup"><span data-stu-id="e39b5-108">Example 1: Get the locations where Premium is available for Windows.</span></span> <span data-ttu-id="e39b5-109">Om inga parametrar anges är PlanType inställt på "Premium" och OSType är inställt på "Windows".</span><span class="sxs-lookup"><span data-stu-id="e39b5-109">If no parameters are specified, PlanType is set to 'Premium' and OSType is set to 'Windows'.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
East Asia (Stage)
West India
South India
Canada Central
West US 2
UK West
UK South
East US 2 EUAP
Central US EUAP
Korea Central
France Central
Australia Central 2
Australia Central
Germany West Central
Norway East
```

<span data-ttu-id="e39b5-110">Det här kommandot får plats där Premium är tillgängligt för Windows.</span><span class="sxs-lookup"><span data-stu-id="e39b5-110">This command gets the locations where Premium is available for Windows.</span></span>

### <span data-ttu-id="e39b5-111">Exempel 2: Hämta de platser där Premium finns för Linux.</span><span class="sxs-lookup"><span data-stu-id="e39b5-111">Example 2: Get the locations where Premium is available for Linux.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation -PlanType Premium -OSType Linux

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
West India
Canada Central
West Central US
West US 2
UK West
UK South
Central US EUAP
Korea Central
France Central
Norway East
```

<span data-ttu-id="e39b5-112">Det här kommandot får plats där Premium finns för Linux.</span><span class="sxs-lookup"><span data-stu-id="e39b5-112">This command gets the locations where Premium is available for Linux.</span></span>

### <span data-ttu-id="e39b5-113">Exempel 3: Hämta de platser där förbrukning är tillgänglig för Windows.</span><span class="sxs-lookup"><span data-stu-id="e39b5-113">Example 3: Get the locations where Consumption is available for Windows.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation -PlanType Consumption -OSType Windows

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
East Asia (Stage)
Central India
West India
South India
Canada Central
Canada East
West Central US
West US 2
UK West
UK South
East US 2 EUAP
Central US EUAP
Korea Central
France Central
Australia Central 2
Australia Central
South Africa North
Switzerland North
Germany West Central
```

<span data-ttu-id="e39b5-114">Det här kommandot får plats där förbrukning är tillgänglig för Windows.</span><span class="sxs-lookup"><span data-stu-id="e39b5-114">This command gets the locations where Consumption is available for Windows.</span></span>

## <span data-ttu-id="e39b5-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e39b5-115">PARAMETERS</span></span>

### <span data-ttu-id="e39b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e39b5-116">-DefaultProfile</span></span>
<span data-ttu-id="e39b5-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e39b5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39b5-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="e39b5-118">-OSType</span></span>
<span data-ttu-id="e39b5-119">OS-typen för tjänste abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e39b5-119">The OS type for the service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39b5-120">-PlanType</span><span class="sxs-lookup"><span data-stu-id="e39b5-120">-PlanType</span></span>
<span data-ttu-id="e39b5-121">Abonnemangs typen.</span><span class="sxs-lookup"><span data-stu-id="e39b5-121">The plan type.</span></span>
<span data-ttu-id="e39b5-122">Giltiga inmatningar: förbrukning eller premie</span><span class="sxs-lookup"><span data-stu-id="e39b5-122">Valid inputs: Consumption or Premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39b5-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e39b5-123">-SubscriptionId</span></span>
<span data-ttu-id="e39b5-124">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="e39b5-124">The Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39b5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e39b5-125">CommonParameters</span></span>
<span data-ttu-id="e39b5-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e39b5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e39b5-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e39b5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e39b5-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e39b5-128">INPUTS</span></span>

## <span data-ttu-id="e39b5-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e39b5-129">OUTPUTS</span></span>

### <span data-ttu-id="e39b5-130">Microsoft. Azure. PowerShell. cmdletar. functions. Models. Api20190801. IGeoRegion</span><span class="sxs-lookup"><span data-stu-id="e39b5-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span></span>

## <span data-ttu-id="e39b5-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e39b5-131">NOTES</span></span>

<span data-ttu-id="e39b5-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e39b5-132">ALIASES</span></span>

## <span data-ttu-id="e39b5-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e39b5-133">RELATED LINKS</span></span>

