---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA2E37AB-F137-4A62-9ABC-90565305A23B
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6d1bbac3db6f69f5cdda14870de20eee7f8170b
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100587"
---
# <span data-ttu-id="9190f-101">New-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="9190f-101">New-WAPackCloudService</span></span>

## <span data-ttu-id="9190f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9190f-102">SYNOPSIS</span></span>
<span data-ttu-id="9190f-103">Skapar en moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="9190f-103">Creates a cloud service.</span></span>

## <span data-ttu-id="9190f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9190f-104">SYNTAX</span></span>

```
New-WAPackCloudService -Name <String> -Label <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9190f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9190f-105">DESCRIPTION</span></span>
<span data-ttu-id="9190f-106">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="9190f-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="9190f-107">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="9190f-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9190f-108">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9190f-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9190f-109">Cmdleten **New-WAPackCloudService** skapar en moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="9190f-109">The **New-WAPackCloudService** cmdlet creates a cloud service.</span></span>

## <span data-ttu-id="9190f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9190f-110">EXAMPLES</span></span>

### <span data-ttu-id="9190f-111">Exempel 1: skapa en moln tjänst</span><span class="sxs-lookup"><span data-stu-id="9190f-111">Example 1: Create a cloud service</span></span>
```
PS C:\> New-WAPackCloudService -Name "ContosoCloudService01" -Label "A label"
```

<span data-ttu-id="9190f-112">Kommandot skapar en moln tjänst med namnet ContosoCloudService01 med en etikett.</span><span class="sxs-lookup"><span data-stu-id="9190f-112">The command creates a cloud service named ContosoCloudService01 with a label.</span></span>

## <span data-ttu-id="9190f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9190f-113">PARAMETERS</span></span>

### <span data-ttu-id="9190f-114">-Etikett</span><span class="sxs-lookup"><span data-stu-id="9190f-114">-Label</span></span>
<span data-ttu-id="9190f-115">Anger en etikett för moln tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9190f-115">Specifies a label for the cloud service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9190f-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="9190f-116">-Name</span></span>
<span data-ttu-id="9190f-117">Anger ett namn för cloudservice.</span><span class="sxs-lookup"><span data-stu-id="9190f-117">Specifies a name for the cloudservice.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9190f-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="9190f-118">-Profile</span></span>
<span data-ttu-id="9190f-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="9190f-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9190f-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="9190f-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9190f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9190f-121">CommonParameters</span></span>
<span data-ttu-id="9190f-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9190f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9190f-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9190f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9190f-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9190f-124">INPUTS</span></span>

## <span data-ttu-id="9190f-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9190f-125">OUTPUTS</span></span>

## <span data-ttu-id="9190f-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9190f-126">NOTES</span></span>

## <span data-ttu-id="9190f-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9190f-127">RELATED LINKS</span></span>

[<span data-ttu-id="9190f-128">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="9190f-128">Get-WAPackCloudService</span></span>](./Get-WAPackCloudService.md)

[<span data-ttu-id="9190f-129">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="9190f-129">Remove-WAPackCloudService</span></span>](./Remove-WAPackCloudService.md)


