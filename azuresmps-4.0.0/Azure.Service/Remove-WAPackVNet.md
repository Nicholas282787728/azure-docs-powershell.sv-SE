---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 42042533-9F84-4189-8C9F-01FD62F89DC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: db14b17e42d23e481468f563768b606d8baa2802
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100636"
---
# <span data-ttu-id="36565-101">Remove-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="36565-101">Remove-WAPackVNet</span></span>

## <span data-ttu-id="36565-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36565-102">SYNOPSIS</span></span>
<span data-ttu-id="36565-103">Tar bort virtuella nätverks objekt.</span><span class="sxs-lookup"><span data-stu-id="36565-103">Removes virtual network objects.</span></span>

## <span data-ttu-id="36565-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36565-104">SYNTAX</span></span>

```
Remove-WAPackVNet -VNet <VMNetwork> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="36565-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36565-105">DESCRIPTION</span></span>
<span data-ttu-id="36565-106">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="36565-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="36565-107">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="36565-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="36565-108">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="36565-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="36565-109">Cmdleten **Remove-WAPackVNet** tar bort virtuella nätverks objekt.</span><span class="sxs-lookup"><span data-stu-id="36565-109">The **Remove-WAPackVNet** cmdlet removes virtual network objects.</span></span>

## <span data-ttu-id="36565-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36565-110">EXAMPLES</span></span>

### <span data-ttu-id="36565-111">Exempel 1: ta bort ett virtualiserat nätverk</span><span class="sxs-lookup"><span data-stu-id="36565-111">Example 1: Remove a virtualized network</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Remove-WAPackVM -VNet $VNet
```

<span data-ttu-id="36565-112">Det första kommandot får det virtualiserade nätverket som heter ContosoVNet01 med hjälp av cmdleten **Get-WAPackVNet** och lagrar sedan objektet i variabeln $VNet.</span><span class="sxs-lookup"><span data-stu-id="36565-112">The first command gets the virtualized network named ContosoVNet01 by using the **Get-WAPackVNet** cmdlet, and then stores that object in the $VNet variable.</span></span>
<span data-ttu-id="36565-113">Det andra kommandot tar bort det virtualiserade nätverket som lagras i $VNet.</span><span class="sxs-lookup"><span data-stu-id="36565-113">The second command removes the virtualized network stored in $VNet.</span></span>
<span data-ttu-id="36565-114">Med kommandot uppmanas du att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="36565-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="36565-115">Exempel 2: ta bort ett virtualiserat nätverk utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="36565-115">Example 2: Remove a virtualized network without confirmation</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet02"
PS C:\> Remove-WAPackVNet -VNet $VNet -Force
```

<span data-ttu-id="36565-116">Det första kommandot får moln tjänsten med namnet ContosoVNet02 med hjälp av cmdleten **Get-WAPackVNet** och lagrar sedan objektet i variabeln $VNet.</span><span class="sxs-lookup"><span data-stu-id="36565-116">The first command gets the cloud service named ContosoVNet02 by using the **Get-WAPackVNet** cmdlet, and then stores that object in the $VNet variable.</span></span>
<span data-ttu-id="36565-117">Det andra kommandot tar bort det virtualiserade nätverket som lagras i $VNet.</span><span class="sxs-lookup"><span data-stu-id="36565-117">The second command removes the virtualized network stored in $VNet.</span></span>
<span data-ttu-id="36565-118">Det här kommandot innehåller parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="36565-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="36565-119">Du uppmanas inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="36565-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="36565-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36565-120">PARAMETERS</span></span>

### <span data-ttu-id="36565-121">-Force</span><span class="sxs-lookup"><span data-stu-id="36565-121">-Force</span></span>
<span data-ttu-id="36565-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="36565-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="36565-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36565-123">-PassThru</span></span>
<span data-ttu-id="36565-124">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="36565-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="36565-125">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="36565-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="36565-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="36565-126">-Profile</span></span>
<span data-ttu-id="36565-127">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="36565-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="36565-128">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="36565-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="36565-129">-VNet</span><span class="sxs-lookup"><span data-stu-id="36565-129">-VNet</span></span>
<span data-ttu-id="36565-130">Anger ett virtualiserat nätverk.</span><span class="sxs-lookup"><span data-stu-id="36565-130">Specifies a virtualized network.</span></span>
<span data-ttu-id="36565-131">Använd cmdleten **Get-WAPackVNet** för att få ett virtualiserat nätverk.</span><span class="sxs-lookup"><span data-stu-id="36565-131">To obtain a virtualized network, use the **Get-WAPackVNet** cmdlet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36565-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36565-132">CommonParameters</span></span>
<span data-ttu-id="36565-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36565-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36565-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36565-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36565-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36565-135">INPUTS</span></span>

## <span data-ttu-id="36565-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36565-136">OUTPUTS</span></span>

## <span data-ttu-id="36565-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36565-137">NOTES</span></span>

## <span data-ttu-id="36565-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36565-138">RELATED LINKS</span></span>

[<span data-ttu-id="36565-139">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="36565-139">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="36565-140">New-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="36565-140">New-WAPackVNet</span></span>](./New-WAPackVNet.md)


