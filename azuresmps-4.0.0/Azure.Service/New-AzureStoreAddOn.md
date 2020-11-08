---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 793037C4-8FE5-4799-B59B-94C1605D9F4E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 593ea36e90635472db1f8568254657f782bd1200
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099431"
---
# <span data-ttu-id="4d659-101">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="4d659-101">New-AzureStoreAddOn</span></span>

## <span data-ttu-id="4d659-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d659-102">SYNOPSIS</span></span>
<span data-ttu-id="4d659-103">Köper en ny tilläggs instans.</span><span class="sxs-lookup"><span data-stu-id="4d659-103">Buys a new add-on instance.</span></span>

## <span data-ttu-id="4d659-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d659-104">SYNTAX</span></span>

```
New-AzureStoreAddOn -Name <String> -AddOn <String> -Plan <String> -Location <String> [-PromotionCode <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4d659-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d659-105">DESCRIPTION</span></span>
<span data-ttu-id="4d659-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="4d659-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="4d659-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="4d659-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="4d659-108">Köper en ny tilläggs instans från Azure Store.</span><span class="sxs-lookup"><span data-stu-id="4d659-108">Buys a new add-on instance from the Azure Store.</span></span>

## <span data-ttu-id="4d659-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d659-109">EXAMPLES</span></span>

### <span data-ttu-id="4d659-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4d659-110">Example 1</span></span>
```
PS C:\> New-AzureStoreAddOn -Name MyAddOn -AddOn AddonId -Plan PlanId -Location "West US"
```

<span data-ttu-id="4d659-111">Det här exemplet köper ett tillägg med namnet ' t-AddOn med en PlanId i västra amerikanska platsen.</span><span class="sxs-lookup"><span data-stu-id="4d659-111">This example buys an add-on named MyAddOn with a PlanId in West US location.</span></span>

### <span data-ttu-id="4d659-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4d659-112">Example 2</span></span>
```
PS C:\> New-AzureStoreAddOn -Name MyAddOn -AddOn AddonId -Plan PlanId -Location "West US" -PromotionCode MyPromoCode
```

<span data-ttu-id="4d659-113">I det här exemplet används en kampanj kod för att köpa ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="4d659-113">This example uses a promotional code to buy an add-on.</span></span>

## <span data-ttu-id="4d659-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d659-114">PARAMETERS</span></span>

### <span data-ttu-id="4d659-115">-AddOn</span><span class="sxs-lookup"><span data-stu-id="4d659-115">-AddOn</span></span>
<span data-ttu-id="4d659-116">Anger ID för tilläggsprogram.</span><span class="sxs-lookup"><span data-stu-id="4d659-116">Specifies the add-on ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d659-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="4d659-117">-Location</span></span>
<span data-ttu-id="4d659-118">Anger platsen för tilläggs instans.</span><span class="sxs-lookup"><span data-stu-id="4d659-118">Specifies the add-on instance location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d659-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="4d659-119">-Name</span></span>
<span data-ttu-id="4d659-120">Anger namnet på tilläggs instans.</span><span class="sxs-lookup"><span data-stu-id="4d659-120">Specifies the name of the add-on instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d659-121">-Planera</span><span class="sxs-lookup"><span data-stu-id="4d659-121">-Plan</span></span>
<span data-ttu-id="4d659-122">Anger plan-ID.</span><span class="sxs-lookup"><span data-stu-id="4d659-122">Specifies the plan ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d659-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="4d659-123">-Profile</span></span>
<span data-ttu-id="4d659-124">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="4d659-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4d659-125">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="4d659-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d659-126">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="4d659-126">-PromotionCode</span></span>
<span data-ttu-id="4d659-127">Anger en kampanj kod som ska användas för köpet.</span><span class="sxs-lookup"><span data-stu-id="4d659-127">Specifies a promotion code to apply to the purchase.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d659-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d659-128">CommonParameters</span></span>
<span data-ttu-id="4d659-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d659-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d659-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d659-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d659-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d659-131">INPUTS</span></span>

## <span data-ttu-id="4d659-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d659-132">OUTPUTS</span></span>

## <span data-ttu-id="4d659-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d659-133">NOTES</span></span>

## <span data-ttu-id="4d659-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d659-134">RELATED LINKS</span></span>

[<span data-ttu-id="4d659-135">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="4d659-135">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="4d659-136">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="4d659-136">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)

[<span data-ttu-id="4d659-137">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="4d659-137">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


