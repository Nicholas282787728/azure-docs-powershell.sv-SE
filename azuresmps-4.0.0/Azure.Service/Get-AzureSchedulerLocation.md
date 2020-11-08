---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 410A58A3-CB0E-43FE-B490-B1520BD1CCEC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c445e2b42738f288de960f30f4c98d909c71784
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093337"
---
# <span data-ttu-id="f5ced-101">Get-AzureSchedulerLocation</span><span class="sxs-lookup"><span data-stu-id="f5ced-101">Get-AzureSchedulerLocation</span></span>

## <span data-ttu-id="f5ced-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5ced-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ced-103">Hämtar tillgängliga platser för schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="f5ced-103">Gets available scheduler locations.</span></span>

## <span data-ttu-id="f5ced-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5ced-104">SYNTAX</span></span>

```
Get-AzureSchedulerLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f5ced-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5ced-105">DESCRIPTION</span></span>
<span data-ttu-id="f5ced-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="f5ced-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f5ced-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f5ced-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f5ced-108">Cmdleten **Get-AzureSchedulerLocation** hämtar tillgängliga platser för schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="f5ced-108">The **Get-AzureSchedulerLocation** cmdlet gets available scheduler locations.</span></span>

## <span data-ttu-id="f5ced-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5ced-109">EXAMPLES</span></span>

### <span data-ttu-id="f5ced-110">Exempel 1: Hämta tillgängliga platser för Schemaläggaren</span><span class="sxs-lookup"><span data-stu-id="f5ced-110">Example 1: Get available scheduler locations</span></span>
```
PS C:\> Get-AzureSchedulerLocation
```

<span data-ttu-id="f5ced-111">Det här kommandot hämtar tillgängliga platser för schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="f5ced-111">This command gets available scheduler locations.</span></span>

## <span data-ttu-id="f5ced-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5ced-112">PARAMETERS</span></span>

### <span data-ttu-id="f5ced-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="f5ced-113">-Profile</span></span>
<span data-ttu-id="f5ced-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f5ced-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f5ced-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="f5ced-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f5ced-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ced-116">CommonParameters</span></span>
<span data-ttu-id="f5ced-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5ced-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ced-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5ced-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ced-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5ced-119">INPUTS</span></span>

## <span data-ttu-id="f5ced-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5ced-120">OUTPUTS</span></span>

## <span data-ttu-id="f5ced-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5ced-121">NOTES</span></span>

## <span data-ttu-id="f5ced-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5ced-122">RELATED LINKS</span></span>

[<span data-ttu-id="f5ced-123">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="f5ced-123">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)

[<span data-ttu-id="f5ced-124">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f5ced-124">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="f5ced-125">Get-AzureSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="f5ced-125">Get-AzureSchedulerJobHistory</span></span>](./Get-AzureSchedulerJobHistory.md)


