---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 92E2409B-14BC-428F-8BAF-60D8DAFA5F57
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1adaafdfdd4331bbba86530eb532964430ed7c69
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099165"
---
# <span data-ttu-id="e80f9-101">Test-AzureTrafficManagerDomainName</span><span class="sxs-lookup"><span data-stu-id="e80f9-101">Test-AzureTrafficManagerDomainName</span></span>

## <span data-ttu-id="e80f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e80f9-102">SYNOPSIS</span></span>
<span data-ttu-id="e80f9-103">Kontrollerar om ett domän namn är tillgängligt som Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="e80f9-103">Checks whether a domain name is available as a Traffic Manager profile.</span></span>

## <span data-ttu-id="e80f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e80f9-104">SYNTAX</span></span>

```
Test-AzureTrafficManagerDomainName -DomainName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e80f9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e80f9-105">DESCRIPTION</span></span>
<span data-ttu-id="e80f9-106">**Test-AzureTrafficManagerDomainName** cmdlet kontrollerar om ett domän namn är tillgängligt som en Microsoft Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="e80f9-106">The **Test-AzureTrafficManagerDomainName** cmdlet checks whether a domain name is available as a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="e80f9-107">Om domän namnet är tillgängligt returnerar denna cmdlet ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="e80f9-107">If the domain name is available, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="e80f9-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e80f9-108">EXAMPLES</span></span>

### <span data-ttu-id="e80f9-109">Exempel 1: kontrol lera om ett domän namn är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="e80f9-109">Example 1: Check whether a domain name is available</span></span>
```
PS C:\>Test-AzureTrafficManagerDomainName -DomainName "ContosoApp.trafficmanager.net"
$True
```

<span data-ttu-id="e80f9-110">Det här kommandot kontrollerar om domän namnet ContosoApp.trafficmanager.net är tillgängligt som Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="e80f9-110">This command checks whether the domain name ContosoApp.trafficmanager.net is available as a Traffic Manager profile.</span></span>

## <span data-ttu-id="e80f9-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e80f9-111">PARAMETERS</span></span>

### <span data-ttu-id="e80f9-112">-Domän namn</span><span class="sxs-lookup"><span data-stu-id="e80f9-112">-DomainName</span></span>
<span data-ttu-id="e80f9-113">Anger det domän namn som ska testas.</span><span class="sxs-lookup"><span data-stu-id="e80f9-113">Specifies the domain name to test.</span></span>
<span data-ttu-id="e80f9-114">Du måste ta med följande sträng:</span><span class="sxs-lookup"><span data-stu-id="e80f9-114">You must include the following string:</span></span> 

<span data-ttu-id="e80f9-115">. trafficmanager.net</span><span class="sxs-lookup"><span data-stu-id="e80f9-115">.trafficmanager.net</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e80f9-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="e80f9-116">-Profile</span></span>
<span data-ttu-id="e80f9-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e80f9-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e80f9-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e80f9-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e80f9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e80f9-119">CommonParameters</span></span>
<span data-ttu-id="e80f9-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e80f9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e80f9-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e80f9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e80f9-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e80f9-122">INPUTS</span></span>

## <span data-ttu-id="e80f9-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e80f9-123">OUTPUTS</span></span>

### <span data-ttu-id="e80f9-124">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e80f9-124">System.Boolean</span></span>
<span data-ttu-id="e80f9-125">Denna cmdlet skapar $True eller $False.</span><span class="sxs-lookup"><span data-stu-id="e80f9-125">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="e80f9-126">Om domän namnet är tillgängligt returnerar denna cmdlet ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="e80f9-126">If the domain name is available, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="e80f9-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e80f9-127">NOTES</span></span>

## <span data-ttu-id="e80f9-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e80f9-128">RELATED LINKS</span></span>

