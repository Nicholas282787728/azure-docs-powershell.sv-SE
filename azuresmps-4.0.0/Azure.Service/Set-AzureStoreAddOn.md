---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F5EC8E00-E504-436A-96FF-4E886579AEA4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b72fcfac0b000a8fcfc11dbab6961460cb25b8b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099645"
---
# <span data-ttu-id="6e57d-101">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="6e57d-101">Set-AzureStoreAddOn</span></span>

## <span data-ttu-id="6e57d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6e57d-102">SYNOPSIS</span></span>
<span data-ttu-id="6e57d-103">Uppdaterar en befintlig tilläggs instans.</span><span class="sxs-lookup"><span data-stu-id="6e57d-103">Updates an existing add-on instance.</span></span>

## <span data-ttu-id="6e57d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6e57d-104">SYNTAX</span></span>

```
Set-AzureStoreAddOn -Name <String> -Plan <String> [-PromotionCode <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6e57d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6e57d-105">DESCRIPTION</span></span>
<span data-ttu-id="6e57d-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="6e57d-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6e57d-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="6e57d-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6e57d-108">Denna cmdlet uppdaterar en befintlig tilläggs instans från den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="6e57d-108">This cmdlet updates an existing add-on instance from the current subscription.</span></span>

## <span data-ttu-id="6e57d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6e57d-109">EXAMPLES</span></span>

### <span data-ttu-id="6e57d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6e57d-110">Example 1</span></span>
```
PS C:\> Set-AzureStoreAddOn MyAddOn NewPlanId
```

<span data-ttu-id="6e57d-111">Det här exemplet uppdaterar ett tillägg med ett nytt plan-ID.</span><span class="sxs-lookup"><span data-stu-id="6e57d-111">This example updates an add-on with a new plan ID.</span></span>

### <span data-ttu-id="6e57d-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6e57d-112">Example 2</span></span>
```
PS C:\> Set-AzureStoreAddOn MyAddOn NewPlanId MyPromoCode
```

<span data-ttu-id="6e57d-113">Det här exemplet uppdaterar ett tillägg med ett nytt plan-ID och reklam kod.</span><span class="sxs-lookup"><span data-stu-id="6e57d-113">This example updates an add-on with a new plan ID and promotional code.</span></span>

## <span data-ttu-id="6e57d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6e57d-114">PARAMETERS</span></span>

### <span data-ttu-id="6e57d-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="6e57d-115">-Name</span></span>
<span data-ttu-id="6e57d-116">Anger namnet på tilläggs instans.</span><span class="sxs-lookup"><span data-stu-id="6e57d-116">Specifies the name of the add-on instance.</span></span>

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

### <span data-ttu-id="6e57d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e57d-117">-PassThru</span></span>
<span data-ttu-id="6e57d-118">Om det här alternativet anges returnerar cmdleten sant om kommandot lyckades och falskt om det Miss lyckas.</span><span class="sxs-lookup"><span data-stu-id="6e57d-118">If specified, the cmdlet returns true if the command succeeds and false if it fails.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e57d-119">-Planera</span><span class="sxs-lookup"><span data-stu-id="6e57d-119">-Plan</span></span>
<span data-ttu-id="6e57d-120">Anger plan-ID.</span><span class="sxs-lookup"><span data-stu-id="6e57d-120">Specifies the plan ID.</span></span>

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

### <span data-ttu-id="6e57d-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="6e57d-121">-Profile</span></span>
<span data-ttu-id="6e57d-122">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="6e57d-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6e57d-123">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="6e57d-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6e57d-124">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="6e57d-124">-PromotionCode</span></span>
<span data-ttu-id="6e57d-125">Anger kampanj koden.</span><span class="sxs-lookup"><span data-stu-id="6e57d-125">Specifies the promotional code.</span></span>

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

### <span data-ttu-id="6e57d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e57d-126">CommonParameters</span></span>
<span data-ttu-id="6e57d-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e57d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e57d-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e57d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e57d-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6e57d-129">INPUTS</span></span>

## <span data-ttu-id="6e57d-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6e57d-130">OUTPUTS</span></span>

## <span data-ttu-id="6e57d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6e57d-131">NOTES</span></span>

## <span data-ttu-id="6e57d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6e57d-132">RELATED LINKS</span></span>

[<span data-ttu-id="6e57d-133">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="6e57d-133">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="6e57d-134">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="6e57d-134">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="6e57d-135">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="6e57d-135">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)


