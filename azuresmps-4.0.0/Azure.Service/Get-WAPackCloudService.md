---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4BAD0DDE-80D4-4A89-AFFB-78C933D2C0D5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76771d8c0e8d06cbe134e920a06be5fc1b109fe2
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100583"
---
# <span data-ttu-id="c7dea-101">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="c7dea-101">Get-WAPackCloudService</span></span>

## <span data-ttu-id="c7dea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7dea-102">SYNOPSIS</span></span>
<span data-ttu-id="c7dea-103">Hämtar moln tjänst objekt.</span><span class="sxs-lookup"><span data-stu-id="c7dea-103">Gets cloud service objects.</span></span>

## <span data-ttu-id="c7dea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7dea-104">SYNTAX</span></span>

### <span data-ttu-id="c7dea-105">Tom (standard)</span><span class="sxs-lookup"><span data-stu-id="c7dea-105">Empty (Default)</span></span>
```
Get-WAPackCloudService [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c7dea-106">FromName</span><span class="sxs-lookup"><span data-stu-id="c7dea-106">FromName</span></span>
```
Get-WAPackCloudService [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c7dea-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7dea-107">DESCRIPTION</span></span>
<span data-ttu-id="c7dea-108">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="c7dea-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="c7dea-109">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="c7dea-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c7dea-110">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c7dea-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c7dea-111">Cmdleten **Get-WAPackCloudService** hämtar moln tjänst objekt.</span><span class="sxs-lookup"><span data-stu-id="c7dea-111">The **Get-WAPackCloudService** cmdlet gets cloud service objects.</span></span>

## <span data-ttu-id="c7dea-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7dea-112">EXAMPLES</span></span>

## <span data-ttu-id="c7dea-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7dea-113">PARAMETERS</span></span>

### <span data-ttu-id="c7dea-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="c7dea-114">-Name</span></span>
<span data-ttu-id="c7dea-115">Anger namnet på en moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="c7dea-115">Specifies the name of a cloud service.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7dea-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="c7dea-116">-Profile</span></span>
<span data-ttu-id="c7dea-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c7dea-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c7dea-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c7dea-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c7dea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7dea-119">CommonParameters</span></span>
<span data-ttu-id="c7dea-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7dea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7dea-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7dea-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7dea-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7dea-122">INPUTS</span></span>

## <span data-ttu-id="c7dea-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7dea-123">OUTPUTS</span></span>

## <span data-ttu-id="c7dea-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7dea-124">NOTES</span></span>

## <span data-ttu-id="c7dea-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7dea-125">RELATED LINKS</span></span>

[<span data-ttu-id="c7dea-126">New-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="c7dea-126">New-WAPackCloudService</span></span>](./New-WAPackCloudService.md)

[<span data-ttu-id="c7dea-127">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="c7dea-127">Remove-WAPackCloudService</span></span>](./Remove-WAPackCloudService.md)


