---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 047C5FBD-CB0D-47BF-AE03-4DF32B4FAD87
online version: ''
schema: 2.0.0
ms.openlocfilehash: a546c9fdb066aaf1203055fd62d8eb01258569c8
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100586"
---
# <span data-ttu-id="61c05-101">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="61c05-101">Get-WAPackVM</span></span>

## <span data-ttu-id="61c05-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="61c05-102">SYNOPSIS</span></span>
<span data-ttu-id="61c05-103">Hämtar virtuella dator objekt.</span><span class="sxs-lookup"><span data-stu-id="61c05-103">Gets virtual machine objects.</span></span>

## <span data-ttu-id="61c05-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="61c05-104">SYNTAX</span></span>

### <span data-ttu-id="61c05-105">Tom (standard)</span><span class="sxs-lookup"><span data-stu-id="61c05-105">Empty (Default)</span></span>
```
Get-WAPackVM [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="61c05-106">FromName</span><span class="sxs-lookup"><span data-stu-id="61c05-106">FromName</span></span>
```
Get-WAPackVM [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="61c05-107">FromId</span><span class="sxs-lookup"><span data-stu-id="61c05-107">FromId</span></span>
```
Get-WAPackVM [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="61c05-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="61c05-108">DESCRIPTION</span></span>
<span data-ttu-id="61c05-109">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="61c05-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="61c05-110">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="61c05-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="61c05-111">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="61c05-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="61c05-112">Cmdleten **Get-WAPackVM** får virtuella dator objekt.</span><span class="sxs-lookup"><span data-stu-id="61c05-112">The **Get-WAPackVM** cmdlet gets virtual machine objects.</span></span>

## <span data-ttu-id="61c05-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="61c05-113">EXAMPLES</span></span>

### <span data-ttu-id="61c05-114">Exempel 1: skaffa en virtuell dator genom att använda ett namn</span><span class="sxs-lookup"><span data-stu-id="61c05-114">Example 1: Get a virtual machine by using a name</span></span>
```
PS C:\> Get-WAPackVM -Name "ContosoV126"
```

<span data-ttu-id="61c05-115">Det här kommandot får den virtuella datorn med namnet ContosoV126.</span><span class="sxs-lookup"><span data-stu-id="61c05-115">This command gets the virtual machine named ContosoV126.</span></span>

### <span data-ttu-id="61c05-116">Exempel 2: skaffa en virtuell dator med hjälp av ett ID</span><span class="sxs-lookup"><span data-stu-id="61c05-116">Example 2: Get a virtual machine by using an ID</span></span>
```
PS C:\> Get-WAPackVM -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="61c05-117">Med det här kommandot får den virtuella datorn ett angivet ID.</span><span class="sxs-lookup"><span data-stu-id="61c05-117">This command gets the virtual machine that has the specified ID.</span></span>

### <span data-ttu-id="61c05-118">Exempel 3: Hämta alla virtuella datorer</span><span class="sxs-lookup"><span data-stu-id="61c05-118">Example 3: Get all virtual machines</span></span>
```
PS C:\> Get-WAPackVM
```

<span data-ttu-id="61c05-119">Det här kommandot får alla virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="61c05-119">This command gets all virtual machines.</span></span>

## <span data-ttu-id="61c05-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="61c05-120">PARAMETERS</span></span>

### <span data-ttu-id="61c05-121">-ID</span><span class="sxs-lookup"><span data-stu-id="61c05-121">-ID</span></span>
<span data-ttu-id="61c05-122">Anger unikt ID för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="61c05-122">Specifies the unique ID of a virtual machine.</span></span>

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

### <span data-ttu-id="61c05-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="61c05-123">-Name</span></span>
<span data-ttu-id="61c05-124">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="61c05-124">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="61c05-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="61c05-125">-Profile</span></span>
<span data-ttu-id="61c05-126">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="61c05-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="61c05-127">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="61c05-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="61c05-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61c05-128">CommonParameters</span></span>
<span data-ttu-id="61c05-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61c05-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61c05-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61c05-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61c05-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="61c05-131">INPUTS</span></span>

## <span data-ttu-id="61c05-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="61c05-132">OUTPUTS</span></span>

## <span data-ttu-id="61c05-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="61c05-133">NOTES</span></span>

## <span data-ttu-id="61c05-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="61c05-134">RELATED LINKS</span></span>

[<span data-ttu-id="61c05-135">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="61c05-135">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="61c05-136">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="61c05-136">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="61c05-137">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="61c05-137">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="61c05-138">Resume-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="61c05-138">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="61c05-139">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="61c05-139">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="61c05-140">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="61c05-140">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="61c05-141">Stopp-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="61c05-141">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="61c05-142">Suspend-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="61c05-142">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="61c05-143">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="61c05-143">Get-WAPackVMOSDisk</span></span>](./Get-WAPackVMOSDisk.md)


