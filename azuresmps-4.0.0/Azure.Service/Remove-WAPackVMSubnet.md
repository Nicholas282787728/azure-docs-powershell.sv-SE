---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7766E3D-D8C2-42F1-840A-8EA633E98500
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8a85934deb617b4f0d8e85ee3162222f16dd294
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100637"
---
# <span data-ttu-id="af47d-101">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="af47d-101">Remove-WAPackVMSubnet</span></span>

## <span data-ttu-id="af47d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af47d-102">SYNOPSIS</span></span>
<span data-ttu-id="af47d-103">Tar bort undernät för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="af47d-103">Removes virtual machine subnet objects.</span></span>

## <span data-ttu-id="af47d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af47d-104">SYNTAX</span></span>

```
Remove-WAPackVMSubnet -VMSubnet <VMSubnet> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="af47d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af47d-105">DESCRIPTION</span></span>
<span data-ttu-id="af47d-106">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="af47d-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="af47d-107">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="af47d-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="af47d-108">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="af47d-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="af47d-109">Cmdleten **Remove-WAPackVMSubnet** tar bort undernät för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="af47d-109">The **Remove-WAPackVMSubnet** cmdlet removes virtual machine subnet objects.</span></span>

## <span data-ttu-id="af47d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af47d-110">EXAMPLES</span></span>

### <span data-ttu-id="af47d-111">Exempel 1: ta bort ett undernät för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="af47d-111">Example 1: Remove a virtual machine subnet</span></span>
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet01"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet
```

<span data-ttu-id="af47d-112">Det första kommandot hämtar det virtuella dator under nätet med namnet ContosoVMSubnet01 med cmdleten **Get-WAPackVMSubnet** och lagrar sedan objektet i variabeln $VMSubnet.</span><span class="sxs-lookup"><span data-stu-id="af47d-112">The first command gets the virtual machine subnet named ContosoVMSubnet01 by using the **Get-WAPackVMSubnet** cmdlet, and then stores that object in the $VMSubnet variable.</span></span>

<span data-ttu-id="af47d-113">Det andra kommandot tar bort det virtuella dator under nätet som lagras i $VMSubnet.</span><span class="sxs-lookup"><span data-stu-id="af47d-113">The second command removes the virtual machine subnet stored in $VMSubnet.</span></span>
<span data-ttu-id="af47d-114">Med kommandot uppmanas du att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="af47d-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="af47d-115">Exempel 2: ta bort en virtuell dator utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="af47d-115">Example 2: Remove a virtual machine without confirmation</span></span>
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet02"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet -Force
```

<span data-ttu-id="af47d-116">Det första kommandot får moln tjänsten med namnet ContosoVMSubnet02 med hjälp av cmdleten **Get-WAPackVMSubnet** och lagrar sedan objektet i variabeln $VMSubnet.</span><span class="sxs-lookup"><span data-stu-id="af47d-116">The first command gets the cloud service named ContosoVMSubnet02 by using the **Get-WAPackVMSubnet** cmdlet, and then stores that object in the $VMSubnet variable.</span></span>

<span data-ttu-id="af47d-117">Det andra kommandot tar bort det virtuella dator under nätet som lagras i $VMSubnet.</span><span class="sxs-lookup"><span data-stu-id="af47d-117">The second command removes the virtual machine subnet stored in $VMSubnet.</span></span>
<span data-ttu-id="af47d-118">Det här kommandot innehåller parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="af47d-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="af47d-119">Du uppmanas inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="af47d-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="af47d-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af47d-120">PARAMETERS</span></span>

### <span data-ttu-id="af47d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="af47d-121">-Force</span></span>
<span data-ttu-id="af47d-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="af47d-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="af47d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af47d-123">-PassThru</span></span>
<span data-ttu-id="af47d-124">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="af47d-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="af47d-125">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="af47d-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="af47d-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="af47d-126">-Profile</span></span>
<span data-ttu-id="af47d-127">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="af47d-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="af47d-128">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="af47d-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="af47d-129">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="af47d-129">-VMSubnet</span></span>
<span data-ttu-id="af47d-130">Anger ett undernät för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="af47d-130">Specifies a virtual machine subnet.</span></span>
<span data-ttu-id="af47d-131">Använd cmdleten **Get-WAPackVMSubnet** för att få en virtuell dator under nät.</span><span class="sxs-lookup"><span data-stu-id="af47d-131">To obtain a virtual machine subnet, use the **Get-WAPackVMSubnet** cmdlet.</span></span>

```yaml
Type: VMSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af47d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af47d-132">CommonParameters</span></span>
<span data-ttu-id="af47d-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af47d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af47d-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af47d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af47d-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af47d-135">INPUTS</span></span>

## <span data-ttu-id="af47d-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af47d-136">OUTPUTS</span></span>

## <span data-ttu-id="af47d-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af47d-137">NOTES</span></span>

## <span data-ttu-id="af47d-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af47d-138">RELATED LINKS</span></span>

[<span data-ttu-id="af47d-139">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="af47d-139">Get-WAPackVMSubnet</span></span>](./Get-WAPackVMSubnet.md)

[<span data-ttu-id="af47d-140">New-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="af47d-140">New-WAPackVMSubnet</span></span>](./New-WAPackVMSubnet.md)


