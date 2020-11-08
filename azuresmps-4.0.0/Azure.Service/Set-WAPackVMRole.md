---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 69FBF1E7-E69A-42B5-AC17-C7CF8CAB3C9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da323d5284de94aaadfc92abdf819f861695335
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100613"
---
# <span data-ttu-id="0d105-101">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="0d105-101">Set-WAPackVMRole</span></span>

## <span data-ttu-id="0d105-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0d105-102">SYNOPSIS</span></span>
<span data-ttu-id="0d105-103">Ändrar egenskapen instance Count för en virtuell dator roll.</span><span class="sxs-lookup"><span data-stu-id="0d105-103">Changes the instance count property of a virtual machine role.</span></span>

## <span data-ttu-id="0d105-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0d105-104">SYNTAX</span></span>

```
Set-WAPackVMRole -VMRole <VMRole> -InstanceCount <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d105-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0d105-105">DESCRIPTION</span></span>
<span data-ttu-id="0d105-106">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="0d105-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="0d105-107">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="0d105-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0d105-108">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0d105-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0d105-109">Cmdleten **set-WAPackVMRole** ändrar egenskapen instance Count för en virtuell dator roll.</span><span class="sxs-lookup"><span data-stu-id="0d105-109">The **Set-WAPackVMRole** cmdlet changes the instance count property of a virtual machine role.</span></span>

## <span data-ttu-id="0d105-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0d105-110">EXAMPLES</span></span>

### <span data-ttu-id="0d105-111">Exempel 1: Ange antalet instanser för en virtuell dator roll</span><span class="sxs-lookup"><span data-stu-id="0d105-111">Example 1: Specify the instance count for a virtual machine role</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Set-WAPackVMRole -VMRole $VMRole -InstanceCount 3
```

<span data-ttu-id="0d105-112">Det första kommandot får rollen virtuell dator med namnet ContosoVMRole01 med hjälp av cmdleten **Get-WAPackVMRole** och lagrar sedan objektet i variabeln $VMRole.</span><span class="sxs-lookup"><span data-stu-id="0d105-112">The first command gets the virtual machine role named ContosoVMRole01 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="0d105-113">Det andra och sista kommandot anger det nya antalet förekomster av den virtuella dator rollen som lagras i $VMRole till 3.</span><span class="sxs-lookup"><span data-stu-id="0d105-113">The second and final command sets the new instance count of the virtual machine role stored in $VMRole to 3.</span></span>

## <span data-ttu-id="0d105-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0d105-114">PARAMETERS</span></span>

### <span data-ttu-id="0d105-115">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="0d105-115">-InstanceCount</span></span>
<span data-ttu-id="0d105-116">Anger antalet instanser för en virtuell dator roll.</span><span class="sxs-lookup"><span data-stu-id="0d105-116">Specifies the instance count for a virtual machine role.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d105-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d105-117">-PassThru</span></span>
<span data-ttu-id="0d105-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="0d105-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0d105-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="0d105-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0d105-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="0d105-120">-Profile</span></span>
<span data-ttu-id="0d105-121">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="0d105-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0d105-122">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="0d105-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0d105-123">-VMRole</span><span class="sxs-lookup"><span data-stu-id="0d105-123">-VMRole</span></span>
<span data-ttu-id="0d105-124">Anger en virtuell dator roll.</span><span class="sxs-lookup"><span data-stu-id="0d105-124">Specifies a virtual machine role.</span></span>
<span data-ttu-id="0d105-125">Använd cmdleten **Get-WAPackVMRole** för att få en virtuell dator roll.</span><span class="sxs-lookup"><span data-stu-id="0d105-125">To obtain a virtual machine role, use the **Get-WAPackVMRole** cmdlet.</span></span>

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d105-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d105-126">CommonParameters</span></span>
<span data-ttu-id="0d105-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d105-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d105-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d105-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d105-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0d105-129">INPUTS</span></span>

## <span data-ttu-id="0d105-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0d105-130">OUTPUTS</span></span>

## <span data-ttu-id="0d105-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0d105-131">NOTES</span></span>

## <span data-ttu-id="0d105-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0d105-132">RELATED LINKS</span></span>

[<span data-ttu-id="0d105-133">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="0d105-133">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="0d105-134">New-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="0d105-134">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="0d105-135">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="0d105-135">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)


