---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 939A28A4-394A-4447-9EFA-8F2876D04DCD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b140c2c0efac81e361e2bab510cfeaf6210ef884
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099037"
---
# <span data-ttu-id="95401-101">Stop-AzureService</span><span class="sxs-lookup"><span data-stu-id="95401-101">Stop-AzureService</span></span>

## <span data-ttu-id="95401-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="95401-102">SYNOPSIS</span></span>
<span data-ttu-id="95401-103">Stoppar den aktuella värdbaserade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="95401-103">Stops the current hosted service.</span></span>

## <span data-ttu-id="95401-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="95401-104">SYNTAX</span></span>

```
Stop-AzureService [-ServiceName <String>] [-Slot <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="95401-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="95401-105">DESCRIPTION</span></span>
<span data-ttu-id="95401-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="95401-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="95401-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="95401-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="95401-108">Cmdleten **Stop-AzureService** stoppar den aktuella värdbaserade tjänsten på platsen i Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="95401-108">The **Stop-AzureService** cmdlet stops the current hosted service in the specified slot in Windows Azure.</span></span>
<span data-ttu-id="95401-109">Om ingen plats anges stoppar cmdleten tjänsten i produktions platsen.</span><span class="sxs-lookup"><span data-stu-id="95401-109">If no slot is specified, the cmdlet stops the service in the Production slot.</span></span>

## <span data-ttu-id="95401-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="95401-110">EXAMPLES</span></span>

## <span data-ttu-id="95401-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="95401-111">PARAMETERS</span></span>

### <span data-ttu-id="95401-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95401-112">-PassThru</span></span>
<span data-ttu-id="95401-113">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="95401-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="95401-114">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="95401-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="95401-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="95401-115">-Profile</span></span>
<span data-ttu-id="95401-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="95401-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="95401-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="95401-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="95401-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="95401-118">-ServiceName</span></span>
<span data-ttu-id="95401-119">Anger namnet på den värdbaserade tjänst som ska stoppas.</span><span class="sxs-lookup"><span data-stu-id="95401-119">Specifies the name of the hosted service to stop.</span></span>
<span data-ttu-id="95401-120">Om inget namn anges stoppar cmdleten den aktuella värdbaserade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="95401-120">If no name is specified, the cmdlet stops the current hosted service.</span></span>

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

### <span data-ttu-id="95401-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="95401-121">-Slot</span></span>
<span data-ttu-id="95401-122">Anger var tjänsten finns, antingen för produktion eller produktion.</span><span class="sxs-lookup"><span data-stu-id="95401-122">Specifies the slot where the service is hosted, either Staging or Production.</span></span>
<span data-ttu-id="95401-123">Om ingen plats är angiven används produktion.</span><span class="sxs-lookup"><span data-stu-id="95401-123">If no slot is specified,  Production is assumed.</span></span>

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

### <span data-ttu-id="95401-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95401-124">CommonParameters</span></span>
<span data-ttu-id="95401-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95401-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95401-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95401-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95401-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="95401-127">INPUTS</span></span>

## <span data-ttu-id="95401-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="95401-128">OUTPUTS</span></span>

## <span data-ttu-id="95401-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="95401-129">NOTES</span></span>

## <span data-ttu-id="95401-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="95401-130">RELATED LINKS</span></span>

[<span data-ttu-id="95401-131">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="95401-131">Remove-AzureService</span></span>](./Remove-AzureService.md)

[<span data-ttu-id="95401-132">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="95401-132">Start-AzureService</span></span>](./Start-AzureService.md)


