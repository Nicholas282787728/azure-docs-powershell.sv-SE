---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D04D79CE-F183-4A8D-B925-F640D89377BD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d7c4e6bd9365ccf45b730024b5841e4356f556a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100638"
---
# <span data-ttu-id="4f154-101">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4f154-101">Remove-WAPackVM</span></span>

## <span data-ttu-id="4f154-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f154-102">SYNOPSIS</span></span>
<span data-ttu-id="4f154-103">Tar bort objekt från virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="4f154-103">Removes virtual machine objects.</span></span>

## <span data-ttu-id="4f154-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f154-104">SYNTAX</span></span>

```
Remove-WAPackVM -VM <VirtualMachine> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4f154-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f154-105">DESCRIPTION</span></span>
<span data-ttu-id="4f154-106">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="4f154-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="4f154-107">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="4f154-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="4f154-108">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="4f154-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="4f154-109">Cmdleten **Remove-WAPackVM** tar bort objekt på virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="4f154-109">The **Remove-WAPackVM** cmdlet removes virtual machine objects.</span></span>

## <span data-ttu-id="4f154-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f154-110">EXAMPLES</span></span>

### <span data-ttu-id="4f154-111">Exempel 1: ta bort en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="4f154-111">Example 1: Remove a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Remove-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="4f154-112">Det första kommandot får den virtuella datorn som heter ContosoV126 med hjälp av cmdleten **Get-WAPackVM** och lagrar sedan objektet i variabeln $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4f154-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="4f154-113">Det andra kommandot tar bort den virtuella datorn som är lagrad i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4f154-113">The second command removes the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="4f154-114">Med kommandot uppmanas du att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="4f154-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="4f154-115">Exempel 2: ta bort en virtuell dator utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="4f154-115">Example 2: Remove a virtual machine without confirmation</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Remove-WAPackVM -VM $VirtualMachine -Force
```

<span data-ttu-id="4f154-116">Det första kommandot får den virtuella datorn som heter ContosoV126 med hjälp av cmdleten **Get-WAPackVM** och lagrar sedan objektet i variabeln $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4f154-116">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="4f154-117">Det andra kommandot tar bort den virtuella datorn som är lagrad i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4f154-117">The second command removes the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="4f154-118">Det här kommandot innehåller parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="4f154-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="4f154-119">Du uppmanas inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="4f154-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="4f154-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f154-120">PARAMETERS</span></span>

### <span data-ttu-id="4f154-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4f154-121">-Force</span></span>
<span data-ttu-id="4f154-122">Anger att cmdleten tar bort en virtuell dator utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="4f154-122">Indicates that the cmdlet removes a virtual machine without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="4f154-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f154-123">-PassThru</span></span>
<span data-ttu-id="4f154-124">Anger att cmdleten returnerar ett booleskt värde.</span><span class="sxs-lookup"><span data-stu-id="4f154-124">Indicates that the cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="4f154-125">Om åtgärden lyckas returnerar cmdleten ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="4f154-125">If the operation succeeds, the cmdlet returns a value of $True.</span></span>
<span data-ttu-id="4f154-126">Annars returneras värdet $False.</span><span class="sxs-lookup"><span data-stu-id="4f154-126">Otherwise, it returns a value of $False.</span></span>
<span data-ttu-id="4f154-127">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="4f154-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4f154-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="4f154-128">-Profile</span></span>
<span data-ttu-id="4f154-129">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="4f154-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4f154-130">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="4f154-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4f154-131">-VM</span><span class="sxs-lookup"><span data-stu-id="4f154-131">-VM</span></span>
<span data-ttu-id="4f154-132">Anger en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="4f154-132">Specifies a virtual machine.</span></span>
<span data-ttu-id="4f154-133">Använd cmdleten **Get-WAPackVM** för att få en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="4f154-133">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="4f154-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4f154-134">-Confirm</span></span>
<span data-ttu-id="4f154-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4f154-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f154-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f154-136">-WhatIf</span></span>
<span data-ttu-id="4f154-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4f154-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f154-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4f154-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f154-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f154-139">CommonParameters</span></span>
<span data-ttu-id="4f154-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f154-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f154-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f154-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f154-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f154-142">INPUTS</span></span>

## <span data-ttu-id="4f154-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f154-143">OUTPUTS</span></span>

## <span data-ttu-id="4f154-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f154-144">NOTES</span></span>

## <span data-ttu-id="4f154-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f154-145">RELATED LINKS</span></span>

[<span data-ttu-id="4f154-146">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4f154-146">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="4f154-147">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4f154-147">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="4f154-148">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4f154-148">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="4f154-149">Resume-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4f154-149">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="4f154-150">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4f154-150">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="4f154-151">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4f154-151">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="4f154-152">Stopp-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4f154-152">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="4f154-153">Suspend-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4f154-153">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


