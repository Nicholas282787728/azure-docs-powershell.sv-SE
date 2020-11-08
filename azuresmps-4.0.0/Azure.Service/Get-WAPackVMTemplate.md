---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 37C788AC-B369-432B-8276-27FFB0B4CF10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d2913877a9f68621bb5c1c930443a46e91e5935
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100621"
---
# <span data-ttu-id="14415-101">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="14415-101">Get-WAPackVMTemplate</span></span>

## <span data-ttu-id="14415-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14415-102">SYNOPSIS</span></span>
<span data-ttu-id="14415-103">Hämtar mallar för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="14415-103">Gets virtual machine templates.</span></span>

## <span data-ttu-id="14415-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14415-104">SYNTAX</span></span>

### <span data-ttu-id="14415-105">Tom (standard)</span><span class="sxs-lookup"><span data-stu-id="14415-105">Empty (Default)</span></span>
```
Get-WAPackVMTemplate [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="14415-106">FromId</span><span class="sxs-lookup"><span data-stu-id="14415-106">FromId</span></span>
```
Get-WAPackVMTemplate [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="14415-107">FromName</span><span class="sxs-lookup"><span data-stu-id="14415-107">FromName</span></span>
```
Get-WAPackVMTemplate [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="14415-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14415-108">DESCRIPTION</span></span>
<span data-ttu-id="14415-109">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="14415-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="14415-110">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="14415-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="14415-111">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="14415-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="14415-112">Cmdleten **Get-WAPackVMTemplate** hämtar mallar för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="14415-112">The **Get-WAPackVMTemplate** cmdlet gets virtual machine templates.</span></span>

## <span data-ttu-id="14415-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14415-113">EXAMPLES</span></span>

### <span data-ttu-id="14415-114">Exempel 1: Hämta en virtuell dator-mall genom att använda ett namn</span><span class="sxs-lookup"><span data-stu-id="14415-114">Example 1: Get a virtual machine template by using a name</span></span>
```
PS C:\> Get-WAPackVMTemplate -Name "ContosoTemplate04"
```

<span data-ttu-id="14415-115">Det här kommandot hämtar mallen för virtuell dator med namnet ContosoTemplate04.</span><span class="sxs-lookup"><span data-stu-id="14415-115">This command gets the virtual machine template named ContosoTemplate04.</span></span>

### <span data-ttu-id="14415-116">Exempel 2: Hämta en virtuell dator-mall genom att använda ett ID</span><span class="sxs-lookup"><span data-stu-id="14415-116">Example 2: Get a virtual machine template by using an ID</span></span>
```
PS C:\> Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="14415-117">Det här kommandot hämtar mallen för virtuell dator med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="14415-117">This command gets the virtual machine template that has the specified ID.</span></span>

### <span data-ttu-id="14415-118">Exempel 3: Hämta alla mallar för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="14415-118">Example 3: Get all virtual machine templates</span></span>
```
PS C:\> Get-WAPackVMTemplate
```

<span data-ttu-id="14415-119">Det här kommandot får alla mallar för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="14415-119">This command gets all the virtual machine templates.</span></span>

## <span data-ttu-id="14415-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14415-120">PARAMETERS</span></span>

### <span data-ttu-id="14415-121">-ID</span><span class="sxs-lookup"><span data-stu-id="14415-121">-ID</span></span>
<span data-ttu-id="14415-122">Anger ett unikt ID för en mall.</span><span class="sxs-lookup"><span data-stu-id="14415-122">Specifies the unique ID of a template.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14415-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="14415-123">-Name</span></span>
<span data-ttu-id="14415-124">Anger namnet på en mall.</span><span class="sxs-lookup"><span data-stu-id="14415-124">Specifies the name of a template.</span></span>

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

### <span data-ttu-id="14415-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="14415-125">-Profile</span></span>
<span data-ttu-id="14415-126">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="14415-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="14415-127">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="14415-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="14415-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14415-128">CommonParameters</span></span>
<span data-ttu-id="14415-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14415-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14415-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14415-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14415-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14415-131">INPUTS</span></span>

## <span data-ttu-id="14415-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14415-132">OUTPUTS</span></span>

## <span data-ttu-id="14415-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14415-133">NOTES</span></span>

## <span data-ttu-id="14415-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14415-134">RELATED LINKS</span></span>

[<span data-ttu-id="14415-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="14415-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


