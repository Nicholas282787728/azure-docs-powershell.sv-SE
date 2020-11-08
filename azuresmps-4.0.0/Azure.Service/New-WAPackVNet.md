---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CB2936E4-E403-44B3-9CB8-617308E54C50
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9059e5bad8441f25846cf98a12c5e8dada2e814a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100627"
---
# <span data-ttu-id="271e4-101">New-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="271e4-101">New-WAPackVNet</span></span>

## <span data-ttu-id="271e4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="271e4-102">SYNOPSIS</span></span>
<span data-ttu-id="271e4-103">Skapar ett virtualiserat nätverk.</span><span class="sxs-lookup"><span data-stu-id="271e4-103">Creates a virtualized network.</span></span>

## <span data-ttu-id="271e4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="271e4-104">SYNTAX</span></span>

```
New-WAPackVNet -LogicalNetwork <LogicalNetwork> -Name <String> [-Description <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="271e4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="271e4-105">DESCRIPTION</span></span>
<span data-ttu-id="271e4-106">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="271e4-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="271e4-107">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="271e4-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="271e4-108">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="271e4-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="271e4-109">Cmdleten **New-WAPackVNet** skapar ett virtualiserat nätverk.</span><span class="sxs-lookup"><span data-stu-id="271e4-109">The **New-WAPackVNet** cmdlet creates a virtualized network.</span></span>

## <span data-ttu-id="271e4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="271e4-110">EXAMPLES</span></span>

### <span data-ttu-id="271e4-111">Exempel 1: skapa ett virtualiserat nätverk</span><span class="sxs-lookup"><span data-stu-id="271e4-111">Example 1: Create a virtualized network</span></span>
```
PS C:\> $LogicalNetwork = Get-WAPackLogicalNetwork -Name "ContosoLogicalNetwork01"
PS C:\> New-WAPackVNet -LogicalNetwork $LogicalNetwork -Name "ContosoVNett01" -Description "A description"
```

<span data-ttu-id="271e4-112">Första kommandot hämtar först det logiska nätverk där vi vill lägga till ett nytt virtualiserat nätverk.</span><span class="sxs-lookup"><span data-stu-id="271e4-112">The first command first retrieves the logical network to which we want to add a new virtualized network.</span></span>
<span data-ttu-id="271e4-113">Detta logiska nätverk heter ContosoLogicalNetwork01.</span><span class="sxs-lookup"><span data-stu-id="271e4-113">This logical network is named ContosoLogicalNetwork01.</span></span>

<span data-ttu-id="271e4-114">Med det andra och sista kommandot skapas ett virtualiserat nätverk med det tidigare hämtade logiska nätverket, ett namn (ContosoVNett01) och en beskrivning (en beskrivning).</span><span class="sxs-lookup"><span data-stu-id="271e4-114">The second and last command creates a virtualized network using the previously retrieved logical network, a name (ContosoVNett01) and a description (A description).</span></span>

## <span data-ttu-id="271e4-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="271e4-115">PARAMETERS</span></span>

### <span data-ttu-id="271e4-116">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="271e4-116">-Description</span></span>
<span data-ttu-id="271e4-117">Anger en beskrivning för det virtualiserade nätverket.</span><span class="sxs-lookup"><span data-stu-id="271e4-117">Specifies a description for the virtualized network.</span></span>

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

### <span data-ttu-id="271e4-118">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="271e4-118">-LogicalNetwork</span></span>
<span data-ttu-id="271e4-119">Anger en LogicalNetwork som är kopplad till det virtualiserade nätverket.</span><span class="sxs-lookup"><span data-stu-id="271e4-119">Specifies a LogicalNetwork associated with the virtualized network.</span></span>

```yaml
Type: LogicalNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="271e4-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="271e4-120">-Name</span></span>
<span data-ttu-id="271e4-121">Anger ett namn för det virtualiserade nätverket.</span><span class="sxs-lookup"><span data-stu-id="271e4-121">Specifies a name for the virtualized network.</span></span>

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

### <span data-ttu-id="271e4-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="271e4-122">-Profile</span></span>
<span data-ttu-id="271e4-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="271e4-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="271e4-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="271e4-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="271e4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="271e4-125">CommonParameters</span></span>
<span data-ttu-id="271e4-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="271e4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="271e4-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="271e4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="271e4-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="271e4-128">INPUTS</span></span>

## <span data-ttu-id="271e4-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="271e4-129">OUTPUTS</span></span>

## <span data-ttu-id="271e4-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="271e4-130">NOTES</span></span>

## <span data-ttu-id="271e4-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="271e4-131">RELATED LINKS</span></span>

[<span data-ttu-id="271e4-132">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="271e4-132">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="271e4-133">Remove-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="271e4-133">Remove-WAPackVNet</span></span>](./Remove-WAPackVNet.md)


