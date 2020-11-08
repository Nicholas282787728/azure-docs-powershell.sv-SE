---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5E85F58B-7C70-4F4A-B218-08F9AF512B76
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8aba9c72e3911f59db88e9be4262ee90ea460a5c
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100625"
---
# <span data-ttu-id="9633b-101">Resume-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9633b-101">Resume-WAPackVM</span></span>

## <span data-ttu-id="9633b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9633b-102">SYNOPSIS</span></span>
<span data-ttu-id="9633b-103">Återupptar pausade virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="9633b-103">Resumes paused virtual machines.</span></span>

## <span data-ttu-id="9633b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9633b-104">SYNTAX</span></span>

```
Resume-WAPackVM -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9633b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9633b-105">DESCRIPTION</span></span>
<span data-ttu-id="9633b-106">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="9633b-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="9633b-107">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="9633b-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9633b-108">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9633b-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9633b-109">Cmdleten **Resume-WAPackVM** återupptar pausade virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="9633b-109">The **Resume-WAPackVM** cmdlet resumes paused virtual machines.</span></span>

## <span data-ttu-id="9633b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9633b-110">EXAMPLES</span></span>

### <span data-ttu-id="9633b-111">Exempel 1: återuppta en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="9633b-111">Example 1: Resume a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Resume-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="9633b-112">Det första kommandot får den virtuella datorn som heter ContosoV126 med hjälp av cmdleten **Get-WAPackVM** och lagrar sedan objektet i variabeln $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="9633b-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="9633b-113">Det andra kommandot återupptar den virtuella datorn som är lagrad i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="9633b-113">The second command resumes the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="9633b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9633b-114">PARAMETERS</span></span>

### <span data-ttu-id="9633b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9633b-115">-PassThru</span></span>
<span data-ttu-id="9633b-116">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="9633b-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9633b-117">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="9633b-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9633b-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="9633b-118">-Profile</span></span>
<span data-ttu-id="9633b-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="9633b-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9633b-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="9633b-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9633b-121">-VM</span><span class="sxs-lookup"><span data-stu-id="9633b-121">-VM</span></span>
<span data-ttu-id="9633b-122">Anger en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="9633b-122">Specifies a virtual machine.</span></span>
<span data-ttu-id="9633b-123">Använd cmdleten **Get-WAPackVM** för att få en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="9633b-123">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

```yaml
Type: VirtualMachine
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9633b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9633b-124">CommonParameters</span></span>
<span data-ttu-id="9633b-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9633b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9633b-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9633b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9633b-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9633b-127">INPUTS</span></span>

## <span data-ttu-id="9633b-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9633b-128">OUTPUTS</span></span>

## <span data-ttu-id="9633b-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9633b-129">NOTES</span></span>

## <span data-ttu-id="9633b-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9633b-130">RELATED LINKS</span></span>

[<span data-ttu-id="9633b-131">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9633b-131">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="9633b-132">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9633b-132">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="9633b-133">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9633b-133">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="9633b-134">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9633b-134">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="9633b-135">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9633b-135">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="9633b-136">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9633b-136">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="9633b-137">Stopp-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9633b-137">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="9633b-138">Suspend-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9633b-138">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

