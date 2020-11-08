---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 61CF7F95-F0BB-4282-A971-537CB73708B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d5774213054f3e9e56e9804a9319e31f095f868
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093273"
---
# <span data-ttu-id="1393b-101">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="1393b-101">Get-AzureStoreAddOn</span></span>

## <span data-ttu-id="1393b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1393b-102">SYNOPSIS</span></span>
<span data-ttu-id="1393b-103">Hämtar de tillgängliga Azure Store-tilläggen.</span><span class="sxs-lookup"><span data-stu-id="1393b-103">Gets the available Azure Store add-ons.</span></span>

## <span data-ttu-id="1393b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1393b-104">SYNTAX</span></span>

### <span data-ttu-id="1393b-105">ListAvailable</span><span class="sxs-lookup"><span data-stu-id="1393b-105">ListAvailable</span></span>
```
Get-AzureStoreAddOn [-ListAvailable] [-Country <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1393b-106">GetAddOn</span><span class="sxs-lookup"><span data-stu-id="1393b-106">GetAddOn</span></span>
```
Get-AzureStoreAddOn [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1393b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1393b-107">DESCRIPTION</span></span>
<span data-ttu-id="1393b-108">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="1393b-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="1393b-109">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="1393b-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="1393b-110">Hämtar alla tillgängliga tillägg för att köpa från Azure Store, eller hämtar befintliga tilläggs instanser för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="1393b-110">Gets all the available add-ons for purchasing from the Azure Store, or gets the existing add-on instances for the current subscription.</span></span>

## <span data-ttu-id="1393b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1393b-111">EXAMPLES</span></span>

### <span data-ttu-id="1393b-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1393b-112">Example 1</span></span>
```
PS C:\> Get-AzureStoreAddOn
```

<span data-ttu-id="1393b-113">I det här exemplet hämtas alla inköpta tilläggs instanser för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="1393b-113">This example gets all purchased add-on instances for the current subscription.</span></span>

### <span data-ttu-id="1393b-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1393b-114">Example 2</span></span>
```
PS C:\> Get-AzureStoreAddOn -ListAvailable
```

<span data-ttu-id="1393b-115">Det här exemplet får alla tillgängliga tillägg för att köpa i USA från Azure Store.</span><span class="sxs-lookup"><span data-stu-id="1393b-115">This example gets all the available add-ons for purchasing in United States from the Azure Store.</span></span>

### <span data-ttu-id="1393b-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="1393b-116">Example 3</span></span>
```
PS C:\> Get-AzureStoreAddOn -Name MyAddOn
```

<span data-ttu-id="1393b-117">I det här exemplet hämtas tillägget ' t ' från den inköpta tilläggs instans i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="1393b-117">This example gets an add-on named MyAddOn from the purchased add-on instance in the current subscription.</span></span>

## <span data-ttu-id="1393b-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1393b-118">PARAMETERS</span></span>

### <span data-ttu-id="1393b-119">-Country</span><span class="sxs-lookup"><span data-stu-id="1393b-119">-Country</span></span>
<span data-ttu-id="1393b-120">Om det här alternativet anges returneras endast de instanser för Azure Store-tillägg som är tillgängliga i det angivna landet.</span><span class="sxs-lookup"><span data-stu-id="1393b-120">If specified, returns only the Azure Store add-on instances available in the specified country.</span></span>
<span data-ttu-id="1393b-121">Standardvärdet är "US".</span><span class="sxs-lookup"><span data-stu-id="1393b-121">The default is "US".</span></span>

```yaml
Type: String
Parameter Sets: ListAvailable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1393b-122">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="1393b-122">-ListAvailable</span></span>
<span data-ttu-id="1393b-123">Om det här alternativet anges hämtas tillgängliga tillägg för inköp från Azure Store.</span><span class="sxs-lookup"><span data-stu-id="1393b-123">If specified, gets available add-ons for purchasing from the Azure Store.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailable
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1393b-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="1393b-124">-Name</span></span>
<span data-ttu-id="1393b-125">Returnerar tillägget som matchar det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="1393b-125">Returns the add-on that matches the specified name.</span></span>

```yaml
Type: String
Parameter Sets: GetAddOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1393b-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="1393b-126">-Profile</span></span>
<span data-ttu-id="1393b-127">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="1393b-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1393b-128">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="1393b-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1393b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1393b-129">CommonParameters</span></span>
<span data-ttu-id="1393b-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1393b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1393b-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1393b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1393b-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1393b-132">INPUTS</span></span>

## <span data-ttu-id="1393b-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1393b-133">OUTPUTS</span></span>

## <span data-ttu-id="1393b-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1393b-134">NOTES</span></span>

## <span data-ttu-id="1393b-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1393b-135">RELATED LINKS</span></span>

[<span data-ttu-id="1393b-136">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="1393b-136">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="1393b-137">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="1393b-137">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)

[<span data-ttu-id="1393b-138">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="1393b-138">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


