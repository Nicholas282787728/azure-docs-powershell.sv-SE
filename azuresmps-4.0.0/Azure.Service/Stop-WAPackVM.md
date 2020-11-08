---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4FB7096E-DDA1-474C-BF0C-D910681BE58D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e4ef4660761ab29e738050c0445534602accda6
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100626"
---
# <span data-ttu-id="8a6f3-101">Stop-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8a6f3-101">Stop-WAPackVM</span></span>

## <span data-ttu-id="8a6f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a6f3-102">SYNOPSIS</span></span>
<span data-ttu-id="8a6f3-103">Stoppar en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="8a6f3-103">Stops a virtual machine.</span></span>

## <span data-ttu-id="8a6f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a6f3-104">SYNTAX</span></span>

```
Stop-WAPackVM [-Shutdown] -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8a6f3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a6f3-105">DESCRIPTION</span></span>
<span data-ttu-id="8a6f3-106">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="8a6f3-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="8a6f3-107">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="8a6f3-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8a6f3-108">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="8a6f3-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8a6f3-109">Cmdleten **Stop-WAPackVM** stoppar en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="8a6f3-109">The **Stop-WAPackVM** cmdlet stops a virtual machine.</span></span>

## <span data-ttu-id="8a6f3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a6f3-110">EXAMPLES</span></span>

### <span data-ttu-id="8a6f3-111">Exempel 1: stoppa en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="8a6f3-111">Example 1: Stop a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Stop-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="8a6f3-112">Det första kommandot får den virtuella datorn som heter ContosoV126 med hjälp av cmdleten **Get-WAPackVM** och lagrar sedan objektet i variabeln $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="8a6f3-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="8a6f3-113">Det andra kommandot stoppar den virtuella datorn som är lagrad i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="8a6f3-113">The second command stops the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="8a6f3-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a6f3-114">PARAMETERS</span></span>

### <span data-ttu-id="8a6f3-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a6f3-115">-PassThru</span></span>
<span data-ttu-id="8a6f3-116">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="8a6f3-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8a6f3-117">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="8a6f3-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8a6f3-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="8a6f3-118">-Profile</span></span>
<span data-ttu-id="8a6f3-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="8a6f3-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8a6f3-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="8a6f3-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8a6f3-121">-Shutdown</span><span class="sxs-lookup"><span data-stu-id="8a6f3-121">-Shutdown</span></span>
<span data-ttu-id="8a6f3-122">Anger att cmdleten stänger av operativ systemet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="8a6f3-122">Indicates that the cmdlet shuts down the operating system of the virtual machine.</span></span>

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

### <span data-ttu-id="8a6f3-123">-VM</span><span class="sxs-lookup"><span data-stu-id="8a6f3-123">-VM</span></span>
<span data-ttu-id="8a6f3-124">Anger en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="8a6f3-124">Specifies a virtual machine.</span></span>
<span data-ttu-id="8a6f3-125">Använd cmdleten **Get-WAPackVM** för att få en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="8a6f3-125">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="8a6f3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a6f3-126">CommonParameters</span></span>
<span data-ttu-id="8a6f3-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a6f3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a6f3-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a6f3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a6f3-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a6f3-129">INPUTS</span></span>

## <span data-ttu-id="8a6f3-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a6f3-130">OUTPUTS</span></span>

## <span data-ttu-id="8a6f3-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a6f3-131">NOTES</span></span>

## <span data-ttu-id="8a6f3-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a6f3-132">RELATED LINKS</span></span>

[<span data-ttu-id="8a6f3-133">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8a6f3-133">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="8a6f3-134">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8a6f3-134">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="8a6f3-135">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8a6f3-135">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="8a6f3-136">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8a6f3-136">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="8a6f3-137">Resume-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8a6f3-137">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="8a6f3-138">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8a6f3-138">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="8a6f3-139">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8a6f3-139">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="8a6f3-140">Suspend-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8a6f3-140">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


