---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CEFFEF9F-4500-447E-99F1-FE053AED880A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e5b65a88e41ce08ec1d60bc140828963950f447
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093324"
---
# <span data-ttu-id="94960-101">Get-AzureServiceProjectRoleRuntime</span><span class="sxs-lookup"><span data-stu-id="94960-101">Get-AzureServiceProjectRoleRuntime</span></span>

## <span data-ttu-id="94960-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94960-102">SYNOPSIS</span></span>
<span data-ttu-id="94960-103">Få de program vara som är tillgängliga för installation i en roll.</span><span class="sxs-lookup"><span data-stu-id="94960-103">Get the runtimes available to install in a role.</span></span>

## <span data-ttu-id="94960-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94960-104">SYNTAX</span></span>

```
Get-AzureServiceProjectRoleRuntime [-Runtime <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="94960-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94960-105">DESCRIPTION</span></span>
<span data-ttu-id="94960-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="94960-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="94960-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="94960-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="94960-108">Hämtar de program vara som är tillgängliga för installation i en roll.</span><span class="sxs-lookup"><span data-stu-id="94960-108">Gets the runtimes available to install in a role.</span></span>

## <span data-ttu-id="94960-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94960-109">EXAMPLES</span></span>

## <span data-ttu-id="94960-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94960-110">PARAMETERS</span></span>

### <span data-ttu-id="94960-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="94960-111">-Profile</span></span>
<span data-ttu-id="94960-112">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="94960-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="94960-113">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="94960-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="94960-114">-Runtime</span><span class="sxs-lookup"><span data-stu-id="94960-114">-Runtime</span></span>
<span data-ttu-id="94960-115">Namnet på körnings miljön.</span><span class="sxs-lookup"><span data-stu-id="94960-115">The name of the runtime.</span></span>
<span data-ttu-id="94960-116">Om du har angett en kör tid returneras bara de specifika versioner av programmet som är tillgängliga för installation i din roll i Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="94960-116">If a runtime specified, only the specific versions of that runtime available to install in your role in Windows Azure will be returned.</span></span>

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

### <span data-ttu-id="94960-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94960-117">CommonParameters</span></span>
<span data-ttu-id="94960-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94960-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94960-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94960-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94960-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94960-120">INPUTS</span></span>

## <span data-ttu-id="94960-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94960-121">OUTPUTS</span></span>

## <span data-ttu-id="94960-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94960-122">NOTES</span></span>

## <span data-ttu-id="94960-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94960-123">RELATED LINKS</span></span>

[<span data-ttu-id="94960-124">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="94960-124">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="94960-125">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="94960-125">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="94960-126">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="94960-126">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)

[<span data-ttu-id="94960-127">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="94960-127">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


