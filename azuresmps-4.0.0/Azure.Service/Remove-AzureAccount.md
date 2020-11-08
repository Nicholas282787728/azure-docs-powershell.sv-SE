---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 3CD1A989-902C-48B3-81E9-7B78EDA5F880
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7003abf263fd4c669956f65c990246295cf7158d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099100"
---
# <span data-ttu-id="a177e-101">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="a177e-101">Remove-AzureAccount</span></span>

## <span data-ttu-id="a177e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a177e-102">SYNOPSIS</span></span>
<span data-ttu-id="a177e-103">Tar bort ett Azure-konto från Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a177e-103">Deletes an Azure account from Windows PowerShell.</span></span>

## <span data-ttu-id="a177e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a177e-104">SYNTAX</span></span>

```
Remove-AzureAccount -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a177e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a177e-105">DESCRIPTION</span></span>
<span data-ttu-id="a177e-106">Med cmdleten **Remove-AzureAccount** tar du bort ett Azure-konto och dess abonnemang från filen med den centrala användar profilen.</span><span class="sxs-lookup"><span data-stu-id="a177e-106">The **Remove-AzureAccount** cmdlet deletes an Azure account and its subscriptions from the subscription data file in your roaming user profile.</span></span>
<span data-ttu-id="a177e-107">Kontot tas inte bort från Microsoft Azure eller så kan du inte ändra det faktiska kontot på något sätt.</span><span class="sxs-lookup"><span data-stu-id="a177e-107">It does not delete the account from Microsoft Azure, or change the actual account in any way.</span></span>

<span data-ttu-id="a177e-108">Att använda denna cmdlet är mycket som att logga ut från ditt Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="a177e-108">Using this cmdlet is a lot like logging out of your Azure account.</span></span>
<span data-ttu-id="a177e-109">Om du vill logga in på kontot igen använder du **AzureAccount** eller **import-AzurePublishSettingsFile** för att lägga till kontot i Windows PowerShell igen.</span><span class="sxs-lookup"><span data-stu-id="a177e-109">And, if you want to log into the account again, use the **Add-AzureAccount** or **Import-AzurePublishSettingsFile** to add the account to Windows PowerShell again.</span></span>

<span data-ttu-id="a177e-110">Du kan också använda cmdleten **Remove-AzureAccount** för att ändra hur Azure PowerShell-cmdlet loggar in på ditt Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="a177e-110">You can also use **Remove-AzureAccount** cmdlet to change the way the Azure PowerShell cmdlets sign into your Azure account.</span></span>
<span data-ttu-id="a177e-111">Om ditt konto har både ett Management-certifikat från **import-AzurePublishSettingsFile** och en åtkomsttoken från **Add-AzureAccount** använder Azure PowerShell-cmdletar bara åtkomsttoken; de ignorerar hanterings certifikatet.</span><span class="sxs-lookup"><span data-stu-id="a177e-111">If your account has both a management certificate from **Import-AzurePublishSettingsFile** and an access token from **Add-AzureAccount** , the Azure PowerShell cmdlets use only the access token; they ignore the management certificate.</span></span>
<span data-ttu-id="a177e-112">Kör **Remove-AzureAccount** om du vill använda hanterings certifikatet.</span><span class="sxs-lookup"><span data-stu-id="a177e-112">To use the management certificate, run **Remove-AzureAccount**.</span></span>
<span data-ttu-id="a177e-113">När **AzureAccount** hittar både ett hanterings certifikat och en åtkomsttoken tar det bara bort åtkomsttoken i stället för att ta bort kontot.</span><span class="sxs-lookup"><span data-stu-id="a177e-113">When **Remove-AzureAccount** finds both a management certificate and an access token, it deletes only the access token, instead of deleting the account.</span></span>
<span data-ttu-id="a177e-114">Hanterings certifikatet är fortfarande där, så kontot är fortfarande tillgängligt för Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a177e-114">The management certificate is still there, so account is still available to Windows PowerShell.</span></span>

<span data-ttu-id="a177e-115">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="a177e-115">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a177e-116">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a177e-116">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="a177e-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a177e-117">EXAMPLES</span></span>

### <span data-ttu-id="a177e-118">Exempel 1: ta bort ett konto</span><span class="sxs-lookup"><span data-stu-id="a177e-118">Example 1: Remove an account</span></span>
```
PS C:\> Remove-AzureAccount -Name admin@contoso.com
```

<span data-ttu-id="a177e-119">Det här kommandot tar bort admin@contoso.com från din prenumerations data fil.</span><span class="sxs-lookup"><span data-stu-id="a177e-119">This command removes the admin@contoso.com from your subscription data file.</span></span>
<span data-ttu-id="a177e-120">När kommandot är klart är kontot inte längre tillgängligt för Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a177e-120">When the command completes, the account is no longer available to Windows PowerShell.</span></span>

## <span data-ttu-id="a177e-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a177e-121">PARAMETERS</span></span>

### <span data-ttu-id="a177e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a177e-122">-Force</span></span>
<span data-ttu-id="a177e-123">Inaktiverar uppmaningen om att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="a177e-123">Suppresses the confirmation prompt.</span></span>
<span data-ttu-id="a177e-124">Som standard uppmaningar AzureAccount om att **ta** bort kontot från Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a177e-124">By default, **Remove-AzureAccount** prompts you before removing the account from Windows PowerShell.</span></span>

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

### <span data-ttu-id="a177e-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="a177e-125">-Name</span></span>
<span data-ttu-id="a177e-126">Anger namnet på kontot som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="a177e-126">Specifies the name of the account to remove.</span></span>
<span data-ttu-id="a177e-127">Parametervärdet är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="a177e-127">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="a177e-128">Jokertecken stöds inte.</span><span class="sxs-lookup"><span data-stu-id="a177e-128">Wildcard characters are not supported.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a177e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a177e-129">-PassThru</span></span>
<span data-ttu-id="a177e-130">Returnerar $True om kommandot lyckas och $False om det inte fungerar.</span><span class="sxs-lookup"><span data-stu-id="a177e-130">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="a177e-131">Denna cmdlet returnerar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="a177e-131">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="a177e-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="a177e-132">-Profile</span></span>
<span data-ttu-id="a177e-133">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="a177e-133">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a177e-134">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="a177e-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a177e-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a177e-135">-Confirm</span></span>
<span data-ttu-id="a177e-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a177e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a177e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a177e-137">-WhatIf</span></span>
<span data-ttu-id="a177e-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a177e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a177e-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a177e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a177e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a177e-140">CommonParameters</span></span>
<span data-ttu-id="a177e-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a177e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a177e-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a177e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a177e-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a177e-143">INPUTS</span></span>

### <span data-ttu-id="a177e-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="a177e-144">None</span></span>
<span data-ttu-id="a177e-145">Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="a177e-145">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="a177e-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a177e-146">OUTPUTS</span></span>

### <span data-ttu-id="a177e-147">Ingen eller system. Boolean</span><span class="sxs-lookup"><span data-stu-id="a177e-147">None or System.Boolean</span></span>
<span data-ttu-id="a177e-148">Om du använder parametern *Passthru* returnerar denna cmdlet ett Boolean-värde.</span><span class="sxs-lookup"><span data-stu-id="a177e-148">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="a177e-149">Annars returnerar den inte några resultat.</span><span class="sxs-lookup"><span data-stu-id="a177e-149">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="a177e-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a177e-150">NOTES</span></span>

## <span data-ttu-id="a177e-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a177e-151">RELATED LINKS</span></span>

[<span data-ttu-id="a177e-152">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="a177e-152">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="a177e-153">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="a177e-153">Get-AzureAccount</span></span>](./Get-AzureAccount.md)


