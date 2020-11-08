---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9445B7FA-FC72-4F71-BD44-8AA55BE9BA0E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d2a3dbabb5bbe78ed571806aa69b9d79d4782b3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093186"
---
# <span data-ttu-id="6fd6f-101">Save-AzureServiceProjectPackage</span><span class="sxs-lookup"><span data-stu-id="6fd6f-101">Save-AzureServiceProjectPackage</span></span>

## <span data-ttu-id="6fd6f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6fd6f-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd6f-103">Paketerar tjänste projektet i Azure Cloud-paketet.</span><span class="sxs-lookup"><span data-stu-id="6fd6f-103">Packages the service project into Azure cloud package.</span></span>

## <span data-ttu-id="6fd6f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6fd6f-104">SYNTAX</span></span>

```
Save-AzureServiceProjectPackage [-Local] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6fd6f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6fd6f-105">DESCRIPTION</span></span>
<span data-ttu-id="6fd6f-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="6fd6f-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6fd6f-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="6fd6f-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6fd6f-108">**AzureServiceProjectPackage** cmdlet-paket till ett Azure Cloud-paket (\*. cspkg).</span><span class="sxs-lookup"><span data-stu-id="6fd6f-108">The **Save-AzureServiceProjectPackage** cmdlet packages the service project into an Azure cloud package (\*.cspkg).</span></span>

## <span data-ttu-id="6fd6f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6fd6f-109">EXAMPLES</span></span>

### <span data-ttu-id="6fd6f-110">Exempel 1: skapa ett paket med service projekt</span><span class="sxs-lookup"><span data-stu-id="6fd6f-110">Example 1: Create a service project package</span></span>
```
PS C:\> Save-AzureServiceProjectPackage
```

<span data-ttu-id="6fd6f-111">I det här exemplet skapas ett \*. cspgk för ett tjänst projekt med namnet MyAzureServiceProject.</span><span class="sxs-lookup"><span data-stu-id="6fd6f-111">This example creates a \*.cspgk for a service project named MyAzureServiceProject.</span></span>

## <span data-ttu-id="6fd6f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6fd6f-112">PARAMETERS</span></span>

### <span data-ttu-id="6fd6f-113">-Lokal</span><span class="sxs-lookup"><span data-stu-id="6fd6f-113">-Local</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd6f-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="6fd6f-114">-Profile</span></span>
<span data-ttu-id="6fd6f-115">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="6fd6f-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6fd6f-116">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="6fd6f-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6fd6f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd6f-117">CommonParameters</span></span>
<span data-ttu-id="6fd6f-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fd6f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd6f-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fd6f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd6f-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6fd6f-120">INPUTS</span></span>

## <span data-ttu-id="6fd6f-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6fd6f-121">OUTPUTS</span></span>

## <span data-ttu-id="6fd6f-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6fd6f-122">NOTES</span></span>

## <span data-ttu-id="6fd6f-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6fd6f-123">RELATED LINKS</span></span>

[<span data-ttu-id="6fd6f-124">Publicera – AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="6fd6f-124">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)


