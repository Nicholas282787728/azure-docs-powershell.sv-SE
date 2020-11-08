---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D927B159-AD68-4071-ADE3-FA2430750D72
online version: ''
schema: 2.0.0
ms.openlocfilehash: 001466cb00ad15f1cbfef6dcf9fd3ce9b931109b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099685"
---
# <span data-ttu-id="4fff0-101">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="4fff0-101">Remove-AzureStoreAddOn</span></span>

## <span data-ttu-id="4fff0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4fff0-102">SYNOPSIS</span></span>
<span data-ttu-id="4fff0-103">Tar bort en befintlig tilläggs instans.</span><span class="sxs-lookup"><span data-stu-id="4fff0-103">Removes an existing add-on instance.</span></span>

## <span data-ttu-id="4fff0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4fff0-104">SYNTAX</span></span>

```
Remove-AzureStoreAddOn -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4fff0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4fff0-105">DESCRIPTION</span></span>
<span data-ttu-id="4fff0-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="4fff0-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="4fff0-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="4fff0-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="4fff0-108">Tar bort en befintlig tilläggs instans från aktuell prenumeration.</span><span class="sxs-lookup"><span data-stu-id="4fff0-108">Removes an existing add-on instance from the current subscription.</span></span>

## <span data-ttu-id="4fff0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4fff0-109">EXAMPLES</span></span>

### <span data-ttu-id="4fff0-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4fff0-110">Example 1</span></span>
```
PS C:\> Remove-AzureStoreAddOn MyAddOn
```

<span data-ttu-id="4fff0-111">Det här exemplet tar bort ett tillägg med namnet ' t ' från det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4fff0-111">This example removes an add-on named MyAddOn from the current subscription.</span></span>

## <span data-ttu-id="4fff0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4fff0-112">PARAMETERS</span></span>

### <span data-ttu-id="4fff0-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="4fff0-113">-Name</span></span>
<span data-ttu-id="4fff0-114">Anger namnet på den instans som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4fff0-114">Specifies the name of the add-on instance to remove.</span></span>

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

### <span data-ttu-id="4fff0-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fff0-115">-PassThru</span></span>
<span data-ttu-id="4fff0-116">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="4fff0-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4fff0-117">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="4fff0-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4fff0-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="4fff0-118">-Profile</span></span>
<span data-ttu-id="4fff0-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="4fff0-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4fff0-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="4fff0-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4fff0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fff0-121">CommonParameters</span></span>
<span data-ttu-id="4fff0-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fff0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fff0-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fff0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fff0-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4fff0-124">INPUTS</span></span>

## <span data-ttu-id="4fff0-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4fff0-125">OUTPUTS</span></span>

## <span data-ttu-id="4fff0-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4fff0-126">NOTES</span></span>

## <span data-ttu-id="4fff0-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4fff0-127">RELATED LINKS</span></span>

[<span data-ttu-id="4fff0-128">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="4fff0-128">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="4fff0-129">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="4fff0-129">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="4fff0-130">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="4fff0-130">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


