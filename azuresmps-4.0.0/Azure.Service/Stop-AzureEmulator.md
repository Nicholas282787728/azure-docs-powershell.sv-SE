---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 43E2C42E-16A3-426E-A7C4-33942F06F908
online version: ''
schema: 2.0.0
ms.openlocfilehash: 501a164fc4470a3d4fd6163050fba495ce3d2705
ms.sourcegitcommit: 25eca7b5f5480758aa2cd830458900cf91cf673c
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/24/2020
ms.locfileid: "95515100"
---
# <span data-ttu-id="18802-101">Stop-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="18802-101">Stop-AzureEmulator</span></span>

## <span data-ttu-id="18802-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="18802-102">SYNOPSIS</span></span>
<span data-ttu-id="18802-103">Avbryter en Compute-emulator.</span><span class="sxs-lookup"><span data-stu-id="18802-103">Stops the compute emulator.</span></span>

## <span data-ttu-id="18802-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="18802-104">SYNTAX</span></span>

```
Stop-AzureEmulator [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="18802-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="18802-105">DESCRIPTION</span></span>
<span data-ttu-id="18802-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="18802-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="18802-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="18802-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="18802-108">Cmdleten **Stop-AzureEmulator** stoppar Azure Compute-emulatorn.</span><span class="sxs-lookup"><span data-stu-id="18802-108">The **Stop-AzureEmulator** cmdlet stops the Azure Compute Emulator.</span></span>
<span data-ttu-id="18802-109">Alla tjänster som körs i emulatorn tas bort.</span><span class="sxs-lookup"><span data-stu-id="18802-109">Any services currently running in the emulator are removed.</span></span>

## <span data-ttu-id="18802-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="18802-110">EXAMPLES</span></span>

## <span data-ttu-id="18802-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="18802-111">PARAMETERS</span></span>

### <span data-ttu-id="18802-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18802-112">-PassThru</span></span>
<span data-ttu-id="18802-113">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="18802-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="18802-114">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="18802-114">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18802-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="18802-115">-Profile</span></span>
<span data-ttu-id="18802-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="18802-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="18802-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="18802-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="18802-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18802-118">CommonParameters</span></span>
<span data-ttu-id="18802-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18802-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18802-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18802-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18802-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="18802-121">INPUTS</span></span>

## <span data-ttu-id="18802-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="18802-122">OUTPUTS</span></span>

## <span data-ttu-id="18802-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="18802-123">NOTES</span></span>

## <span data-ttu-id="18802-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="18802-124">RELATED LINKS</span></span>

[<span data-ttu-id="18802-125">Start-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="18802-125">Start-AzureEmulator</span></span>](./Start-AzureEmulator.md)


