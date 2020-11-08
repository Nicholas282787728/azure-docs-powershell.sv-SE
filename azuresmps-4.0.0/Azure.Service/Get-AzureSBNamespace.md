---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1D433BD2-4604-474B-A2DA-BC80EE935E5C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ffbe5ae961c1733be68c902a9657b200cba0a5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093339"
---
# <span data-ttu-id="82463-101">Get-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="82463-101">Get-AzureSBNamespace</span></span>

## <span data-ttu-id="82463-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82463-102">SYNOPSIS</span></span>
<span data-ttu-id="82463-103">Hämtar namn området.</span><span class="sxs-lookup"><span data-stu-id="82463-103">Gets the namespace.</span></span>


## <span data-ttu-id="82463-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82463-104">SYNTAX</span></span>

```
Get-AzureSBNamespace [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="82463-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82463-105">DESCRIPTION</span></span>
<span data-ttu-id="82463-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="82463-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="82463-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="82463-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="82463-108">Cmdleten **Get-AzureSBNamespace** returnerar de tjänst namn rymder som är associerade med den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="82463-108">The **Get-AzureSBNamespace** cmdlet returns the Service Bus service namespaces associated with the current subscription.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="82463-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82463-109">EXAMPLES</span></span>

### <span data-ttu-id="82463-110">Exempel 1: skaffa Service Bus-namnutrymmet</span><span class="sxs-lookup"><span data-stu-id="82463-110">Example 1: Get the Service Bus namespace</span></span>
```
PS C:\> Get-AzureSBNamespace
```

<span data-ttu-id="82463-111">Det här exemplet får tjänst namn rymderna för Service Bus-tjänsten kopplade till det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="82463-111">This example gets the Service Bus service namespaces associated with the current subscription.</span></span>

## <span data-ttu-id="82463-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82463-112">PARAMETERS</span></span>

### <span data-ttu-id="82463-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="82463-113">-Name</span></span>
<span data-ttu-id="82463-114">Anger namnet på ett Service Bus-namn att leta efter.</span><span class="sxs-lookup"><span data-stu-id="82463-114">Specifies the name of a Service Bus namespace to look for.</span></span>

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

### <span data-ttu-id="82463-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="82463-115">-Profile</span></span>
<span data-ttu-id="82463-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="82463-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="82463-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="82463-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="82463-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82463-118">CommonParameters</span></span>
<span data-ttu-id="82463-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82463-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82463-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82463-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82463-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82463-121">INPUTS</span></span>

## <span data-ttu-id="82463-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82463-122">OUTPUTS</span></span>

## <span data-ttu-id="82463-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82463-123">NOTES</span></span>

## <span data-ttu-id="82463-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82463-124">RELATED LINKS</span></span>

[<span data-ttu-id="82463-125">Get-AzureSBLocation</span><span class="sxs-lookup"><span data-stu-id="82463-125">Get-AzureSBLocation</span></span>](./Get-AzureSBLocation.md)


