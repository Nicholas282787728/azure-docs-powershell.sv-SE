---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7D51BE56-C0A2-4A32-BB7F-8FA9CC67F8F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 986d4998119c4ede1780fa35ad6baadce4574a81
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100584"
---
# <span data-ttu-id="d9cd5-101">Get-WAPackLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="d9cd5-101">Get-WAPackLogicalNetwork</span></span>

## <span data-ttu-id="d9cd5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9cd5-102">SYNOPSIS</span></span>
<span data-ttu-id="d9cd5-103">Hämtar logiska nätverks objekt.</span><span class="sxs-lookup"><span data-stu-id="d9cd5-103">Gets logical network objects.</span></span>

## <span data-ttu-id="d9cd5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9cd5-104">SYNTAX</span></span>

### <span data-ttu-id="d9cd5-105">Tom (standard)</span><span class="sxs-lookup"><span data-stu-id="d9cd5-105">Empty (Default)</span></span>
```
Get-WAPackLogicalNetwork [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d9cd5-106">FromName</span><span class="sxs-lookup"><span data-stu-id="d9cd5-106">FromName</span></span>
```
Get-WAPackLogicalNetwork [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d9cd5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9cd5-107">DESCRIPTION</span></span>
<span data-ttu-id="d9cd5-108">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="d9cd5-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="d9cd5-109">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="d9cd5-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d9cd5-110">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d9cd5-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d9cd5-111">Cmdleten **Get-WAPackLogicalNetwork** hämtar logiska nätverks objekt.</span><span class="sxs-lookup"><span data-stu-id="d9cd5-111">The **Get-WAPackLogicalNetwork** cmdlet gets logical network objects.</span></span>

## <span data-ttu-id="d9cd5-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9cd5-112">EXAMPLES</span></span>

### <span data-ttu-id="d9cd5-113">Exempel 1: skaffa ett logiskt nätverk genom att använda ett namn</span><span class="sxs-lookup"><span data-stu-id="d9cd5-113">Example 1: Get a logical network by using a name</span></span>
```
PS C:\> Get-WAPackLogicalNetwork -Name "ContosoLogicalNetwork01"
```

<span data-ttu-id="d9cd5-114">Det här kommandot får ett logiskt nätverk som heter ContosoLogicalNetwork01.</span><span class="sxs-lookup"><span data-stu-id="d9cd5-114">This command gets a logical network named ContosoLogicalNetwork01.</span></span>

### <span data-ttu-id="d9cd5-115">Exempel 2: Hämta alla logiska nätverk</span><span class="sxs-lookup"><span data-stu-id="d9cd5-115">Example 2: Get all logical networks</span></span>
```
PS C:\> Get-WAPackLogicalNetwork
```

<span data-ttu-id="d9cd5-116">Det här kommandot får alla logiska nätverk.</span><span class="sxs-lookup"><span data-stu-id="d9cd5-116">This command gets all logical networks.</span></span>

## <span data-ttu-id="d9cd5-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9cd5-117">PARAMETERS</span></span>

### <span data-ttu-id="d9cd5-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="d9cd5-118">-Name</span></span>
<span data-ttu-id="d9cd5-119">Anger namnet på ett logiskt nätverk.</span><span class="sxs-lookup"><span data-stu-id="d9cd5-119">Specifies the name of a logical network.</span></span>

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

### <span data-ttu-id="d9cd5-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="d9cd5-120">-Profile</span></span>
<span data-ttu-id="d9cd5-121">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="d9cd5-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d9cd5-122">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="d9cd5-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d9cd5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9cd5-123">CommonParameters</span></span>
<span data-ttu-id="d9cd5-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9cd5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9cd5-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9cd5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9cd5-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9cd5-126">INPUTS</span></span>

## <span data-ttu-id="d9cd5-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9cd5-127">OUTPUTS</span></span>

## <span data-ttu-id="d9cd5-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9cd5-128">NOTES</span></span>

## <span data-ttu-id="d9cd5-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9cd5-129">RELATED LINKS</span></span>

