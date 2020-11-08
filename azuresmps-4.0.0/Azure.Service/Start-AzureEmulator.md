---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1815E7F-720E-4526-A779-106C181B840D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22b04496d9ce310b58662c62b70a195e8cfa8878
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099261"
---
# <span data-ttu-id="44a3b-101">Start-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="44a3b-101">Start-AzureEmulator</span></span>

## <span data-ttu-id="44a3b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="44a3b-102">SYNOPSIS</span></span>
<span data-ttu-id="44a3b-103">Startar beräknings-och lagrings emulatorer.</span><span class="sxs-lookup"><span data-stu-id="44a3b-103">Starts the compute and storage emulators.</span></span>

## <span data-ttu-id="44a3b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="44a3b-104">SYNTAX</span></span>

```
Start-AzureEmulator [-Launch] [-Mode <ComputeEmulatorMode>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="44a3b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="44a3b-105">DESCRIPTION</span></span>
<span data-ttu-id="44a3b-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="44a3b-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="44a3b-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="44a3b-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="44a3b-108">Cmdleten **Start-AzureEmulator** startar både Compute-och Storage-emulatorerna och är värd för den aktuella tjänsten i Compute-emulatorn.</span><span class="sxs-lookup"><span data-stu-id="44a3b-108">The **Start-AzureEmulator** cmdlet starts both the compute and storage emulators and hosts the current service in the compute emulator.</span></span>

## <span data-ttu-id="44a3b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="44a3b-109">EXAMPLES</span></span>

### <span data-ttu-id="44a3b-110">Exempel 1: starta emulatorn och starta en webbläsare</span><span class="sxs-lookup"><span data-stu-id="44a3b-110">Example 1: Start the emulator and launch a browser</span></span>
```
PS C:\> Start-AzureEmulator -L
```

<span data-ttu-id="44a3b-111">I det här exemplet körs tjänsten i Azure-emulatorn och ett nytt webbläsarfönster öppnas i den emulerade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="44a3b-111">This example runs the service in the Azure emulator and launches a new browser window on the emulated service.</span></span>

## <span data-ttu-id="44a3b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="44a3b-112">PARAMETERS</span></span>

### <span data-ttu-id="44a3b-113">-Lansera</span><span class="sxs-lookup"><span data-stu-id="44a3b-113">-Launch</span></span>
<span data-ttu-id="44a3b-114">Öppnar ett nytt webbläsarfönster på tjänsten när det är inloggat i emulatorn.</span><span class="sxs-lookup"><span data-stu-id="44a3b-114">Opens a new browser window on the service after hosting it in the emulator.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44a3b-115">-Mode</span><span class="sxs-lookup"><span data-stu-id="44a3b-115">-Mode</span></span>
<span data-ttu-id="44a3b-116">Anger emuleringsläge.</span><span class="sxs-lookup"><span data-stu-id="44a3b-116">Specifies the emulator mode.</span></span>
<span data-ttu-id="44a3b-117">Giltiga värden är: full och Express.</span><span class="sxs-lookup"><span data-stu-id="44a3b-117">Valid values are: Full and Express.</span></span>
<span data-ttu-id="44a3b-118">Standardvärdet är uttrycka.</span><span class="sxs-lookup"><span data-stu-id="44a3b-118">The default value is Express.</span></span>

```yaml
Type: ComputeEmulatorMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44a3b-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="44a3b-119">-Profile</span></span>
<span data-ttu-id="44a3b-120">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="44a3b-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="44a3b-121">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="44a3b-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="44a3b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44a3b-122">CommonParameters</span></span>
<span data-ttu-id="44a3b-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44a3b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44a3b-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44a3b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44a3b-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="44a3b-125">INPUTS</span></span>

## <span data-ttu-id="44a3b-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="44a3b-126">OUTPUTS</span></span>

## <span data-ttu-id="44a3b-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="44a3b-127">NOTES</span></span>

## <span data-ttu-id="44a3b-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="44a3b-128">RELATED LINKS</span></span>

[<span data-ttu-id="44a3b-129">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="44a3b-129">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="44a3b-130">Publicera – AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="44a3b-130">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="44a3b-131">Stopp-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="44a3b-131">Stop-AzureEmulator</span></span>](./Stop-AzureEmulator.md)


