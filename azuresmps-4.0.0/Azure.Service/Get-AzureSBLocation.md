---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 03E0442D-248E-41DB-98F5-DB3132CD0DCC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 492abdaab507b3ea5f7a8715c82dc0c29e3e94ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099542"
---
# <span data-ttu-id="41c0d-101">Get-AzureSBLocation</span><span class="sxs-lookup"><span data-stu-id="41c0d-101">Get-AzureSBLocation</span></span>

## <span data-ttu-id="41c0d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="41c0d-102">SYNOPSIS</span></span>
<span data-ttu-id="41c0d-103">Hämtar tjänst bussens plats.</span><span class="sxs-lookup"><span data-stu-id="41c0d-103">Gets the location of the Service Bus.</span></span>

## <span data-ttu-id="41c0d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="41c0d-104">SYNTAX</span></span>

```
Get-AzureSBLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="41c0d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="41c0d-105">DESCRIPTION</span></span>
<span data-ttu-id="41c0d-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="41c0d-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="41c0d-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="41c0d-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="41c0d-108">Cmdleten **Get-AzureSBLocation** returnerar platserna som tjänst bussen är tillgänglig från.</span><span class="sxs-lookup"><span data-stu-id="41c0d-108">The **Get-AzureSBLocation** cmdlet returns the locations from which the Service Bus is available.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="41c0d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="41c0d-109">EXAMPLES</span></span>

### <span data-ttu-id="41c0d-110">Exempel 1: skaffa Service Bus-platsen</span><span class="sxs-lookup"><span data-stu-id="41c0d-110">Example 1: Get the Service Bus location</span></span>
```
PS C:\> Get-AzureSBLocation
```

<span data-ttu-id="41c0d-111">I det här exemplet får du platsen för Service Bus.</span><span class="sxs-lookup"><span data-stu-id="41c0d-111">This example gets the location of the Service Bus.</span></span>

## <span data-ttu-id="41c0d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="41c0d-112">PARAMETERS</span></span>

### <span data-ttu-id="41c0d-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="41c0d-113">-Profile</span></span>
<span data-ttu-id="41c0d-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="41c0d-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="41c0d-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="41c0d-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="41c0d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41c0d-116">CommonParameters</span></span>
<span data-ttu-id="41c0d-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41c0d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41c0d-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41c0d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41c0d-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="41c0d-119">INPUTS</span></span>

## <span data-ttu-id="41c0d-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="41c0d-120">OUTPUTS</span></span>

## <span data-ttu-id="41c0d-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="41c0d-121">NOTES</span></span>

## <span data-ttu-id="41c0d-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="41c0d-122">RELATED LINKS</span></span>

[<span data-ttu-id="41c0d-123">Get-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="41c0d-123">Get-AzureSBNamespace</span></span>](./Get-AzureSBNamespace.md)


