---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: ABC303ED-8712-4958-B871-E95357012277
online version: ''
schema: 2.0.0
ms.openlocfilehash: 706c1dee2bc4bb21a8cf116d15bfa3e53daeed99
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099325"
---
# <span data-ttu-id="cdb61-101">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="cdb61-101">Remove-AzureSubscription</span></span>

## <span data-ttu-id="cdb61-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cdb61-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb61-103">Tar bort ett Azure-abonnemang från Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cdb61-103">Deletes an Azure subscription from Windows PowerShell.</span></span>

## <span data-ttu-id="cdb61-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cdb61-104">SYNTAX</span></span>

### <span data-ttu-id="cdb61-105">Namn (standard)</span><span class="sxs-lookup"><span data-stu-id="cdb61-105">Name (Default)</span></span>
```
Remove-AzureSubscription -SubscriptionName <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdb61-106">Et</span><span class="sxs-lookup"><span data-stu-id="cdb61-106">Id</span></span>
```
Remove-AzureSubscription -SubscriptionId <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdb61-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cdb61-107">DESCRIPTION</span></span>
<span data-ttu-id="cdb61-108">Cmdleten **Remove-AzureSubscription** tar bort en Azure-prenumeration från din prenumerations data fil så att det inte går att hitta den i Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cdb61-108">The **Remove-AzureSubscription** cmdlet deletes an Azure subscription from your subscription data file so Windows PowerShell can't find it.</span></span>
<span data-ttu-id="cdb61-109">Denna cmdlet tar inte bort abonnemanget från Microsoft Azure, eller så kan du inte ändra det faktiska abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="cdb61-109">This cmdlet does not delete the subscription from Microsoft Azure, or change the actual subscription in any way.</span></span>

<span data-ttu-id="cdb61-110">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="cdb61-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="cdb61-111">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="cdb61-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="cdb61-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cdb61-112">EXAMPLES</span></span>

### <span data-ttu-id="cdb61-113">Exempel 1: ta bort ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="cdb61-113">Example 1: Delete a subscription</span></span>
```
C:\PS> Remove-AzureSubscription -SubscriptionName Test

Confirm
Are you sure you want to perform this action?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="cdb61-114">Det här kommandot tar bort "test"-prenumerationen från standard filen för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="cdb61-114">This command deletes the "Test" subscription from the default subscription data file.</span></span>

### <span data-ttu-id="cdb61-115">Exempel 2: ta bort från en alternativ fil för abonnemang</span><span class="sxs-lookup"><span data-stu-id="cdb61-115">Example 2: Delete from an alternate subscription data file</span></span>
```
C:\PS> Remove-AzureSubscription -SubscriptionName Test -SubscriptionDataFile C:\Subs\MySubscriptions.xml -Force
```

<span data-ttu-id="cdb61-116">Det här kommandot tar bort test prenumerationen från MySubscriptions.xml-prenumerationens datafil.</span><span class="sxs-lookup"><span data-stu-id="cdb61-116">This command deletes the Test subscription from the MySubscriptions.xml subscription data file.</span></span>
<span data-ttu-id="cdb61-117">Kommandot använder parametern *Force* för att inte bekräfta uppmaningen.</span><span class="sxs-lookup"><span data-stu-id="cdb61-117">The command uses the *Force* parameter to suppress the confirmation prompt.</span></span>

### <span data-ttu-id="cdb61-118">Exempel 3: ta bort ett abonnemang i ett skript</span><span class="sxs-lookup"><span data-stu-id="cdb61-118">Example 3: Delete a subscription in a script</span></span>
```
C:\PS> ...if (Remove-AzureSubscription -SubscriptionName Test -PassThru) {...}
```

<span data-ttu-id="cdb61-119">Det här kommandot använder kommandot **Remove-AzureSubscription** i en **IF** -sats.</span><span class="sxs-lookup"><span data-stu-id="cdb61-119">This command uses the **Remove-AzureSubscription** command in an **If** statement.</span></span>
<span data-ttu-id="cdb61-120">Parametern *Passthru* används, som returnerar ett booleskt värde, för att avgöra om skript blocket i **IF** -instruktionen körs.</span><span class="sxs-lookup"><span data-stu-id="cdb61-120">It uses the *PassThru* parameter, which returns a Boolean value, to determine whether the script block in the **If** statement is executed.</span></span>

## <span data-ttu-id="cdb61-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cdb61-121">PARAMETERS</span></span>

### <span data-ttu-id="cdb61-122">-Force</span><span class="sxs-lookup"><span data-stu-id="cdb61-122">-Force</span></span>
<span data-ttu-id="cdb61-123">Inaktiverar uppmaningen om att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="cdb61-123">Suppresses the confirmation prompt.</span></span>

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

### <span data-ttu-id="cdb61-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cdb61-124">-PassThru</span></span>
<span data-ttu-id="cdb61-125">Returnerar $True om kommandot lyckas och $False om det inte fungerar.</span><span class="sxs-lookup"><span data-stu-id="cdb61-125">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="cdb61-126">Denna cmdlet returnerar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="cdb61-126">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="cdb61-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="cdb61-127">-Profile</span></span>
<span data-ttu-id="cdb61-128">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="cdb61-128">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="cdb61-129">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="cdb61-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cdb61-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cdb61-130">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: Id
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb61-131">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="cdb61-131">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: Name
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb61-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cdb61-132">-Confirm</span></span>
<span data-ttu-id="cdb61-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cdb61-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdb61-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdb61-134">-WhatIf</span></span>
<span data-ttu-id="cdb61-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cdb61-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdb61-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cdb61-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdb61-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb61-137">CommonParameters</span></span>
<span data-ttu-id="cdb61-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdb61-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb61-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdb61-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb61-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cdb61-140">INPUTS</span></span>

### <span data-ttu-id="cdb61-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="cdb61-141">None</span></span>
<span data-ttu-id="cdb61-142">Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="cdb61-142">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="cdb61-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cdb61-143">OUTPUTS</span></span>

### <span data-ttu-id="cdb61-144">Ingen eller system. Boolean</span><span class="sxs-lookup"><span data-stu-id="cdb61-144">None or System.Boolean</span></span>
<span data-ttu-id="cdb61-145">Om du använder parametern *Passthru* returnerar denna cmdlet ett Boolean-värde.</span><span class="sxs-lookup"><span data-stu-id="cdb61-145">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="cdb61-146">Annars returnerar den inte några resultat.</span><span class="sxs-lookup"><span data-stu-id="cdb61-146">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="cdb61-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cdb61-147">NOTES</span></span>

## <span data-ttu-id="cdb61-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cdb61-148">RELATED LINKS</span></span>

[<span data-ttu-id="cdb61-149">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="cdb61-149">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="cdb61-150">Select-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="cdb61-150">Select-AzureSubscription</span></span>](./Select-AzureSubscription.md)

[<span data-ttu-id="cdb61-151">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="cdb61-151">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


