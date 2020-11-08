---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CCA6334F-A193-4506-B873-76F29980C68D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25749aca2d0fb2682404d6c4d006c8ad1b1f3c6b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099566"
---
# <span data-ttu-id="664ec-101">Get-AzureLocation</span><span class="sxs-lookup"><span data-stu-id="664ec-101">Get-AzureLocation</span></span>

## <span data-ttu-id="664ec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="664ec-102">SYNOPSIS</span></span>
<span data-ttu-id="664ec-103">Hämtar tillgängliga data Center platser för det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="664ec-103">Gets the available data center locations for the current Azure subscription.</span></span>

## <span data-ttu-id="664ec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="664ec-104">SYNTAX</span></span>

```
Get-AzureLocation [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="664ec-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="664ec-105">DESCRIPTION</span></span>
<span data-ttu-id="664ec-106">Cmdleten **Get-AzureLocation** hämtar en lista över tillgängliga Azure Data Center och deras egenskaper för det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="664ec-106">The **Get-AzureLocation** cmdlet gets a list of the available Azure data centers and their properties for the current Azure subscription.</span></span>
<span data-ttu-id="664ec-107">Innan du kör denna cmdlet måste du ange ditt nuvarande abonnemang med hjälp av Select-AzureSubscription och Set-AzureSubscription cmdletar.</span><span class="sxs-lookup"><span data-stu-id="664ec-107">Before you run this cmdlet, you must set your current subscription by using the Select-AzureSubscription and Set-AzureSubscription cmdlets.</span></span>

## <span data-ttu-id="664ec-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="664ec-108">EXAMPLES</span></span>

### <span data-ttu-id="664ec-109">Exempel 1: hitta platser</span><span class="sxs-lookup"><span data-stu-id="664ec-109">Example 1: Get locations</span></span>
```
PS C:\> Get-AzureLocation
```

<span data-ttu-id="664ec-110">Det här kommandot får en lista över tillgängliga data Center och deras egenskaper för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="664ec-110">This command gets a list of available data centers, and their properties, for the current subscription.</span></span>

## <span data-ttu-id="664ec-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="664ec-111">PARAMETERS</span></span>

### <span data-ttu-id="664ec-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="664ec-112">-InformationAction</span></span>
<span data-ttu-id="664ec-113">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="664ec-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="664ec-114">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="664ec-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="664ec-115">Vidare</span><span class="sxs-lookup"><span data-stu-id="664ec-115">Continue</span></span>
- <span data-ttu-id="664ec-116">Över</span><span class="sxs-lookup"><span data-stu-id="664ec-116">Ignore</span></span>
- <span data-ttu-id="664ec-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="664ec-117">Inquire</span></span>
- <span data-ttu-id="664ec-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="664ec-118">SilentlyContinue</span></span>
- <span data-ttu-id="664ec-119">Stanna</span><span class="sxs-lookup"><span data-stu-id="664ec-119">Stop</span></span>
- <span data-ttu-id="664ec-120">Avbryt</span><span class="sxs-lookup"><span data-stu-id="664ec-120">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="664ec-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="664ec-121">-InformationVariable</span></span>
<span data-ttu-id="664ec-122">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="664ec-122">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="664ec-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="664ec-123">-Profile</span></span>
<span data-ttu-id="664ec-124">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="664ec-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="664ec-125">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="664ec-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="664ec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="664ec-126">CommonParameters</span></span>
<span data-ttu-id="664ec-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="664ec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="664ec-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="664ec-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="664ec-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="664ec-129">INPUTS</span></span>

## <span data-ttu-id="664ec-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="664ec-130">OUTPUTS</span></span>

## <span data-ttu-id="664ec-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="664ec-131">NOTES</span></span>

## <span data-ttu-id="664ec-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="664ec-132">RELATED LINKS</span></span>

