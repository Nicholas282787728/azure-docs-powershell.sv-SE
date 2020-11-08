---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CE618AD2-7E28-4012-BF3C-B932B95FFDD5
online version: ''
schema: 2.0.0
ms.openlocfilehash: a07358c37bf30e8d5fc3040cdfd174b800df96e4
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100642"
---
# <span data-ttu-id="f0ffd-101">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="f0ffd-101">Remove-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="f0ffd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f0ffd-102">SYNOPSIS</span></span>
<span data-ttu-id="f0ffd-103">Tar bort objekt för statisk IP-adresspool.</span><span class="sxs-lookup"><span data-stu-id="f0ffd-103">Removes static IP address pool objects.</span></span>

## <span data-ttu-id="f0ffd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f0ffd-104">SYNTAX</span></span>

```
Remove-WAPackStaticIPAddressPool -StaticIPAddressPool <StaticIPAddressPool> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f0ffd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f0ffd-105">DESCRIPTION</span></span>
<span data-ttu-id="f0ffd-106">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="f0ffd-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="f0ffd-107">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="f0ffd-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f0ffd-108">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f0ffd-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f0ffd-109">Cmdleten **Remove-WAPackStaticIPAddressPool** tar bort statiska IP-adresspooler.</span><span class="sxs-lookup"><span data-stu-id="f0ffd-109">The **Remove-WAPackStaticIPAddressPool** cmdlet removes static IP address pool objects.</span></span>

## <span data-ttu-id="f0ffd-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f0ffd-110">EXAMPLES</span></span>

### <span data-ttu-id="f0ffd-111">Exempel 1: ta bort en statisk IP-adresspool</span><span class="sxs-lookup"><span data-stu-id="f0ffd-111">Example 1: Remove a static IP address pool</span></span>
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool01"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool
```

<span data-ttu-id="f0ffd-112">Det första kommandot får den statiska IP-adresspoolen som heter ContosoStaticIPAddressPool01 med hjälp av cmdleten **Get-WAPackStaticIPAddressPool** och lagrar sedan objektet i variabeln $StaticIPAddressPool.</span><span class="sxs-lookup"><span data-stu-id="f0ffd-112">The first command gets the static IP address pool named ContosoStaticIPAddressPool01 by using the **Get-WAPackStaticIPAddressPool** cmdlet, and then stores that object in the $StaticIPAddressPool variable.</span></span>

<span data-ttu-id="f0ffd-113">Det andra kommandot tar bort den statiska IP-adresspoolen som lagras i $StaticIPAddressPool.</span><span class="sxs-lookup"><span data-stu-id="f0ffd-113">The second command removes the static IP address pool stored in $StaticIPAddressPool.</span></span>
<span data-ttu-id="f0ffd-114">Med kommandot uppmanas du att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="f0ffd-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="f0ffd-115">Exempel 2: ta bort en statisk IP-adresspool utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="f0ffd-115">Example 2: Remove a static IP address pool without confirmation</span></span>
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool02"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool -Force
```

<span data-ttu-id="f0ffd-116">Det första kommandot får den statiska IP-adresspoolen som heter ContosoStaticIPAddressPool02 med hjälp av cmdleten **Get-WAPackStaticIPAddressPool** och lagrar sedan objektet i variabeln $ StaticIPAddressPool.</span><span class="sxs-lookup"><span data-stu-id="f0ffd-116">The first command gets the static IP address pool named ContosoStaticIPAddressPool02 by using the **Get-WAPackStaticIPAddressPool** cmdlet, and then stores that object in the $ StaticIPAddressPool variable.</span></span>

<span data-ttu-id="f0ffd-117">Det andra kommandot tar bort den statiska IP-adresspoolen som lagras i $StaticIPAddressPool.</span><span class="sxs-lookup"><span data-stu-id="f0ffd-117">The second command removes the static IP address pool stored in $StaticIPAddressPool.</span></span>
<span data-ttu-id="f0ffd-118">Det här kommandot innehåller parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="f0ffd-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="f0ffd-119">Du uppmanas inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="f0ffd-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f0ffd-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f0ffd-120">PARAMETERS</span></span>

### <span data-ttu-id="f0ffd-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f0ffd-121">-Force</span></span>
<span data-ttu-id="f0ffd-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f0ffd-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f0ffd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0ffd-123">-PassThru</span></span>
<span data-ttu-id="f0ffd-124">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="f0ffd-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f0ffd-125">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="f0ffd-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f0ffd-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="f0ffd-126">-Profile</span></span>
<span data-ttu-id="f0ffd-127">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f0ffd-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f0ffd-128">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="f0ffd-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f0ffd-129">-StaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="f0ffd-129">-StaticIPAddressPool</span></span>
<span data-ttu-id="f0ffd-130">Anger en StaticIPAddressPool.</span><span class="sxs-lookup"><span data-stu-id="f0ffd-130">Specifies a StaticIPAddressPool.</span></span>
<span data-ttu-id="f0ffd-131">Använd cmdleten **Get-WAPackStaticIPAddressPool** för att få en statisk IP-adresspool.</span><span class="sxs-lookup"><span data-stu-id="f0ffd-131">To obtain a static IP address pool, use the **Get-WAPackStaticIPAddressPool** cmdlet.</span></span>

```yaml
Type: StaticIPAddressPool
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ffd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0ffd-132">CommonParameters</span></span>
<span data-ttu-id="f0ffd-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0ffd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0ffd-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0ffd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0ffd-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f0ffd-135">INPUTS</span></span>

## <span data-ttu-id="f0ffd-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f0ffd-136">OUTPUTS</span></span>

## <span data-ttu-id="f0ffd-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f0ffd-137">NOTES</span></span>

## <span data-ttu-id="f0ffd-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f0ffd-138">RELATED LINKS</span></span>

[<span data-ttu-id="f0ffd-139">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="f0ffd-139">Get-WAPackStaticIPAddressPool</span></span>](./Get-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="f0ffd-140">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="f0ffd-140">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


