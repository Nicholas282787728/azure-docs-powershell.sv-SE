---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 53BD6ED4-EA66-448B-8B18-F078C0738AF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90f02a261dc804f46a7ef503879a8ce9f43fad35
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100630"
---
# <span data-ttu-id="d3852-101">New-WAPackQuickVM</span><span class="sxs-lookup"><span data-stu-id="d3852-101">New-WAPackQuickVM</span></span>

## <span data-ttu-id="d3852-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3852-102">SYNOPSIS</span></span>
<span data-ttu-id="d3852-103">Skapar en virtuell dator baserad på en mall.</span><span class="sxs-lookup"><span data-stu-id="d3852-103">Creates a virtual machine based on a template.</span></span>

## <span data-ttu-id="d3852-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3852-104">SYNTAX</span></span>

```
New-WAPackQuickVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d3852-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3852-105">DESCRIPTION</span></span>
<span data-ttu-id="d3852-106">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="d3852-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="d3852-107">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="d3852-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d3852-108">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d3852-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d3852-109">Cmdleten **New-WAPackQuickVM** skapar en virtuell dator baserad på en mall.</span><span class="sxs-lookup"><span data-stu-id="d3852-109">The **New-WAPackQuickVM** cmdlet creates a virtual machine based on a template.</span></span>

## <span data-ttu-id="d3852-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3852-110">EXAMPLES</span></span>

### <span data-ttu-id="d3852-111">Exempel 1: skapa en virtuell dator baserad på en mall</span><span class="sxs-lookup"><span data-stu-id="d3852-111">Example 1: Create a virtual machine based on a template</span></span>
```
PS C:\> $Credentials = Get-Credential
PS C:\> $TemplateId = Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
PS C:\> New-WAPackQuickVM -Name "VirtualMachine023" -Template $TemplateId -VMCredential $Credentials
```

<span data-ttu-id="d3852-112">Det första kommandot skapar ett **PSCredential** -objekt och lagrar det sedan i $credentials variabel.</span><span class="sxs-lookup"><span data-stu-id="d3852-112">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>
<span data-ttu-id="d3852-113">Du uppmanas att ange ett konto och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="d3852-113">The cmdlet prompts you for an account and password.</span></span>
<span data-ttu-id="d3852-114">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="d3852-114">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="d3852-115">Det andra kommandot får en mall med cmdleten **Get-WAPackVMTemplate** .</span><span class="sxs-lookup"><span data-stu-id="d3852-115">The second command gets a template by using the **Get-WAPackVMTemplate** cmdlet.</span></span>
<span data-ttu-id="d3852-116">Kommandot anger ID för en mall.</span><span class="sxs-lookup"><span data-stu-id="d3852-116">The command specifies the ID of a template.</span></span>
<span data-ttu-id="d3852-117">Kommandot lagrar mallnamnet i $TemplateID variabel.</span><span class="sxs-lookup"><span data-stu-id="d3852-117">The command stores the template object in the $TemplateID variable.</span></span>

<span data-ttu-id="d3852-118">Med kommandot slut skapas en virtuell dator med namnet VirtualMachine023.</span><span class="sxs-lookup"><span data-stu-id="d3852-118">The final command creates a virtual machine named VirtualMachine023.</span></span>
<span data-ttu-id="d3852-119">Kommandot baserar den virtuella datorn på mallen som lagras i $TemplateId.</span><span class="sxs-lookup"><span data-stu-id="d3852-119">The command bases the virtual machine on the template stored in $TemplateId.</span></span>

## <span data-ttu-id="d3852-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3852-120">PARAMETERS</span></span>

### <span data-ttu-id="d3852-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="d3852-121">-Name</span></span>
<span data-ttu-id="d3852-122">Anger ett namn för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="d3852-122">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="d3852-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="d3852-123">-Profile</span></span>
<span data-ttu-id="d3852-124">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="d3852-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d3852-125">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="d3852-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d3852-126">-Mall</span><span class="sxs-lookup"><span data-stu-id="d3852-126">-Template</span></span>
<span data-ttu-id="d3852-127">Anger en mall.</span><span class="sxs-lookup"><span data-stu-id="d3852-127">Specifies a template.</span></span>
<span data-ttu-id="d3852-128">Cmdleten skapar en virtuell dator utifrån den mall som du anger.</span><span class="sxs-lookup"><span data-stu-id="d3852-128">The cmdlet creates a virtual machine based on the template that you specify.</span></span>
<span data-ttu-id="d3852-129">Använd cmdleten **Get-WAPackVMTemplate** för att få ett Template-objekt.</span><span class="sxs-lookup"><span data-stu-id="d3852-129">To obtain a template object, use the **Get-WAPackVMTemplate** cmdlet.</span></span>

```yaml
Type: VMTemplate
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3852-130">-VMCredential</span><span class="sxs-lookup"><span data-stu-id="d3852-130">-VMCredential</span></span>
<span data-ttu-id="d3852-131">Anger autentiseringsuppgifter för det lokala administratörs kontot.</span><span class="sxs-lookup"><span data-stu-id="d3852-131">Specifies the credential for the local Administrator account.</span></span>
<span data-ttu-id="d3852-132">Om du vill hämta ett **PSCredential** -objekt använder du cmdleten **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="d3852-132">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="d3852-133">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="d3852-133">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3852-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3852-134">CommonParameters</span></span>
<span data-ttu-id="d3852-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3852-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3852-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3852-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3852-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3852-137">INPUTS</span></span>

## <span data-ttu-id="d3852-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3852-138">OUTPUTS</span></span>

## <span data-ttu-id="d3852-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3852-139">NOTES</span></span>

## <span data-ttu-id="d3852-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3852-140">RELATED LINKS</span></span>

[<span data-ttu-id="d3852-141">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="d3852-141">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="d3852-142">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="d3852-142">Get-WAPackVMTemplate</span></span>](./Get-WAPackVMTemplate.md)


