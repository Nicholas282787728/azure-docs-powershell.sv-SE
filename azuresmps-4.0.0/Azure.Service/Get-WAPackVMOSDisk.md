---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E6E40D1B-A5BC-4B38-9D22-F06A8E4DABDF
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1360f45b751088bd899282cee2e64ce965d11fb
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100582"
---
# <span data-ttu-id="82d04-101">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="82d04-101">Get-WAPackVMOSDisk</span></span>

## <span data-ttu-id="82d04-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82d04-102">SYNOPSIS</span></span>
<span data-ttu-id="82d04-103">Hämtar disk objekt för operativ system för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="82d04-103">Gets operating system disk objects for virtual machines.</span></span>

## <span data-ttu-id="82d04-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82d04-104">SYNTAX</span></span>

### <span data-ttu-id="82d04-105">Tom (standard)</span><span class="sxs-lookup"><span data-stu-id="82d04-105">Empty (Default)</span></span>
```
Get-WAPackVMOSDisk [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="82d04-106">FromId</span><span class="sxs-lookup"><span data-stu-id="82d04-106">FromId</span></span>
```
Get-WAPackVMOSDisk [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="82d04-107">FromName</span><span class="sxs-lookup"><span data-stu-id="82d04-107">FromName</span></span>
```
Get-WAPackVMOSDisk [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="82d04-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82d04-108">DESCRIPTION</span></span>
<span data-ttu-id="82d04-109">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="82d04-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="82d04-110">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="82d04-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="82d04-111">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="82d04-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="82d04-112">Cmdleten **Get-WAPackVMOSDisk** hämtar disk objekt för operativ systemet för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="82d04-112">The **Get-WAPackVMOSDisk** cmdlet gets operating system disk objects for virtual machines.</span></span>

## <span data-ttu-id="82d04-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82d04-113">EXAMPLES</span></span>

### <span data-ttu-id="82d04-114">Exempel 1: skaffa en operativ Systems diskett med hjälp av ett namn</span><span class="sxs-lookup"><span data-stu-id="82d04-114">Example 1: Get an operating system disk by using a name</span></span>
```
PS C:\> Get-WAPackVMOSDisk -Name "ContosoOSDisk"
```

<span data-ttu-id="82d04-115">Det här kommandot får en operativ system disk med namnet ContosoOSDisk.</span><span class="sxs-lookup"><span data-stu-id="82d04-115">This command gets an operating system disk named ContosoOSDisk.</span></span>

### <span data-ttu-id="82d04-116">Exempel 2: skaffa en operativ Systems diskett med hjälp av ett ID</span><span class="sxs-lookup"><span data-stu-id="82d04-116">Example 2: Get an operating system disk by using an ID</span></span>
```
PS C:\> Get-WAPackVMOSDisk -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="82d04-117">Det här kommandot får operativ system disken med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="82d04-117">This command gets the operating system disk that has the specified ID.</span></span>

### <span data-ttu-id="82d04-118">Exempel 3: Hämta alla operativ system diskar</span><span class="sxs-lookup"><span data-stu-id="82d04-118">Example 3: Get all operating system disks</span></span>
```
PS C:\> Get-WAPackVMOSDisk
```

<span data-ttu-id="82d04-119">Det här kommandot får alla operativ system diskar.</span><span class="sxs-lookup"><span data-stu-id="82d04-119">This command gets all operating system disks.</span></span>

## <span data-ttu-id="82d04-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82d04-120">PARAMETERS</span></span>

### <span data-ttu-id="82d04-121">-ID</span><span class="sxs-lookup"><span data-stu-id="82d04-121">-ID</span></span>
<span data-ttu-id="82d04-122">Anger unikt ID för en operativ system disk.</span><span class="sxs-lookup"><span data-stu-id="82d04-122">Specifies the unique ID of an operating system disk.</span></span>

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

### <span data-ttu-id="82d04-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="82d04-123">-Name</span></span>
<span data-ttu-id="82d04-124">Anger namnet på en operativ system disk.</span><span class="sxs-lookup"><span data-stu-id="82d04-124">Specifies the name of an operating system disk.</span></span>

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

### <span data-ttu-id="82d04-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="82d04-125">-Profile</span></span>
<span data-ttu-id="82d04-126">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="82d04-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="82d04-127">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="82d04-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="82d04-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82d04-128">CommonParameters</span></span>
<span data-ttu-id="82d04-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82d04-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82d04-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82d04-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82d04-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82d04-131">INPUTS</span></span>

## <span data-ttu-id="82d04-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82d04-132">OUTPUTS</span></span>

## <span data-ttu-id="82d04-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82d04-133">NOTES</span></span>

## <span data-ttu-id="82d04-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82d04-134">RELATED LINKS</span></span>

[<span data-ttu-id="82d04-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="82d04-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


