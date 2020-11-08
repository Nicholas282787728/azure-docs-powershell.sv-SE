---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 7A45DCAD-88DC-40F0-BBF7-0F531A571CA6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48b941691366c3af821e3a4cdaa7b07c5e958e16
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093171"
---
# <span data-ttu-id="0836e-101">Select-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="0836e-101">Select-AzureSubscription</span></span>

## <span data-ttu-id="0836e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0836e-102">SYNOPSIS</span></span>
<span data-ttu-id="0836e-103">Ändrar nuvarande och vanliga Azure-prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="0836e-103">Changes the current and default Azure subscriptions.</span></span>

## <span data-ttu-id="0836e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0836e-104">SYNTAX</span></span>

### <span data-ttu-id="0836e-105">SelectSubscriptionByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0836e-105">SelectSubscriptionByNameParameterSet (Default)</span></span>
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0836e-106">SelectDefaultSubscriptionByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0836e-106">SelectDefaultSubscriptionByNameParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0836e-107">SelectSubscriptionByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0836e-107">SelectSubscriptionByIdParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0836e-108">SelectDefaultSubscriptionByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0836e-108">SelectDefaultSubscriptionByIdParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0836e-109">NoCurrentSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0836e-109">NoCurrentSubscriptionParameterSet</span></span>
```
Select-AzureSubscription [-Account <String>] [-NoCurrent] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="0836e-110">NoDefaultSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0836e-110">NoDefaultSubscriptionParameterSet</span></span>
```
Select-AzureSubscription [-Account <String>] [-NoDefault] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0836e-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0836e-111">DESCRIPTION</span></span>
<span data-ttu-id="0836e-112">Cmdleten **Select-AzureSubscription** och rensar aktuella och vanliga Azure-prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="0836e-112">The **Select-AzureSubscription** cmdlet sets and clears the current and default Azure subscriptions.</span></span>

<span data-ttu-id="0836e-113">"Aktuell prenumeration" är den prenumeration som används som standard i den aktuella Windows PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="0836e-113">The "current subscription" is the subscription that is used by default in the current Windows PowerShell session.</span></span>
<span data-ttu-id="0836e-114">"Standard abonnemang" används som standard i alla Windows PowerShell-sessioner.</span><span class="sxs-lookup"><span data-stu-id="0836e-114">The "default subscription" is used by default in all Windows PowerShell sessions.</span></span>
<span data-ttu-id="0836e-115">Med etiketten "aktuell prenumeration" kan du ange att ett annat abonnemang ska användas för den aktuella sessionen utan att ändra "standard prenumerationen" för alla andra sessioner.</span><span class="sxs-lookup"><span data-stu-id="0836e-115">The "current subscription" label lets you specify a different subscription to be used by default for the current session without changing the "default subscription" for all other sessions.</span></span>

<span data-ttu-id="0836e-116">Prenumerations beteckningen "standard" sparas i din prenumerations data fil.</span><span class="sxs-lookup"><span data-stu-id="0836e-116">The "default" subscription designation is saved in your subscription data file.</span></span>
<span data-ttu-id="0836e-117">Den sessionsbaserade "nuvarande"-beteckningen sparas inte.</span><span class="sxs-lookup"><span data-stu-id="0836e-117">The session-specific "current" designation is not saved.</span></span>

<span data-ttu-id="0836e-118">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="0836e-118">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0836e-119">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0836e-119">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="0836e-120">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0836e-120">EXAMPLES</span></span>

### <span data-ttu-id="0836e-121">Exempel 1: Ange aktuellt abonnemang</span><span class="sxs-lookup"><span data-stu-id="0836e-121">Example 1: Set the current subscription</span></span>
```
C:\PS> Select-AzureSubscription -Current -SubscriptionName ContosoEngineering
```

<span data-ttu-id="0836e-122">Det här kommandot gör "ContosoEngineering" till det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="0836e-122">This command makes "ContosoEngineering" the current subscription.</span></span>

### <span data-ttu-id="0836e-123">Exempel 2: Ange standard abonnemang</span><span class="sxs-lookup"><span data-stu-id="0836e-123">Example 2: Set the default subscription</span></span>
```
C:\PS> Select-AzureSubscription -Default -SubscriptionName ContosoFinance -SubscriptionDataFile "C:\subs\MySubscriptions.xml"
```

<span data-ttu-id="0836e-124">Det här kommandot ändrar standard prenumerationen till "ContosoFinance".</span><span class="sxs-lookup"><span data-stu-id="0836e-124">This command changes the default subscription to "ContosoFinance."</span></span> <span data-ttu-id="0836e-125">Inställningen sparas i Subscriptions.xml-prenumerationens datafil i stället för standard filen för abonnemang.</span><span class="sxs-lookup"><span data-stu-id="0836e-125">It saves the setting in the Subscriptions.xml subscription data file, instead of the default subscription data file.</span></span>

## <span data-ttu-id="0836e-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0836e-126">PARAMETERS</span></span>

### <span data-ttu-id="0836e-127">-Konto</span><span class="sxs-lookup"><span data-stu-id="0836e-127">-Account</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0836e-128">-Aktuell</span><span class="sxs-lookup"><span data-stu-id="0836e-128">-Current</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectSubscriptionByIdParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0836e-129">-Standard</span><span class="sxs-lookup"><span data-stu-id="0836e-129">-Default</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: SelectDefaultSubscriptionByNameParameterSet, SelectDefaultSubscriptionByIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0836e-130">-Nocurrent</span><span class="sxs-lookup"><span data-stu-id="0836e-130">-NoCurrent</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: NoCurrentSubscriptionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0836e-131">-Nodefault</span><span class="sxs-lookup"><span data-stu-id="0836e-131">-NoDefault</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: NoDefaultSubscriptionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0836e-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0836e-132">-PassThru</span></span>
<span data-ttu-id="0836e-133">Returnerar $True om kommandot lyckas och $False om det inte fungerar.</span><span class="sxs-lookup"><span data-stu-id="0836e-133">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="0836e-134">Denna cmdlet returnerar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="0836e-134">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="0836e-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="0836e-135">-Profile</span></span>
<span data-ttu-id="0836e-136">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="0836e-136">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="0836e-137">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="0836e-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0836e-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0836e-138">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: SelectSubscriptionByIdParameterSet, SelectDefaultSubscriptionByIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0836e-139">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="0836e-139">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectDefaultSubscriptionByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0836e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0836e-140">CommonParameters</span></span>
<span data-ttu-id="0836e-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0836e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0836e-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0836e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0836e-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0836e-143">INPUTS</span></span>

### <span data-ttu-id="0836e-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="0836e-144">None</span></span>
<span data-ttu-id="0836e-145">Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="0836e-145">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="0836e-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0836e-146">OUTPUTS</span></span>

### <span data-ttu-id="0836e-147">Ingen eller system. Boolean</span><span class="sxs-lookup"><span data-stu-id="0836e-147">None or System.Boolean</span></span>
<span data-ttu-id="0836e-148">Om du använder parametern *Passthru* returnerar denna cmdlet ett Boolean-värde.</span><span class="sxs-lookup"><span data-stu-id="0836e-148">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="0836e-149">Den genererar inga utdata som standard.</span><span class="sxs-lookup"><span data-stu-id="0836e-149">By default, it does not generate any output.</span></span>

## <span data-ttu-id="0836e-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0836e-150">NOTES</span></span>

## <span data-ttu-id="0836e-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0836e-151">RELATED LINKS</span></span>

[<span data-ttu-id="0836e-152">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="0836e-152">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="0836e-153">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="0836e-153">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="0836e-154">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="0836e-154">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


