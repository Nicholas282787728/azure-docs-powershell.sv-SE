---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 03EAFFB2-EA64-4227-A33B-D24EB4A75F71
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac88bc2494bad975c6169262edd05c7b821061bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099626"
---
# <span data-ttu-id="bacbd-101">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="bacbd-101">Add-AzureAccount</span></span>

## <span data-ttu-id="bacbd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bacbd-102">SYNOPSIS</span></span>
<span data-ttu-id="bacbd-103">Lägger till Azure-kontot till Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bacbd-103">Adds the Azure account to Windows PowerShell.</span></span>

## <span data-ttu-id="bacbd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bacbd-104">SYNTAX</span></span>

### <span data-ttu-id="bacbd-105">Användare (standard)</span><span class="sxs-lookup"><span data-stu-id="bacbd-105">User (Default)</span></span>
```
Add-AzureAccount [-Environment <String>] [-Credential <PSCredential>] [-Tenant <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bacbd-106">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bacbd-106">ServicePrincipal</span></span>
```
Add-AzureAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bacbd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bacbd-107">DESCRIPTION</span></span>
<span data-ttu-id="bacbd-108">Med cmdleten **Add-AzureAccount** blir ditt Azure-konto och dess abonnemang tillgängliga i Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bacbd-108">The **Add-AzureAccount** cmdlet makes your Azure account and its subscriptions available in Windows PowerShell.</span></span>
<span data-ttu-id="bacbd-109">Det är som att logga in på ditt Azure-konto i Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bacbd-109">It's like logging into your Azure account in Windows PowerShell.</span></span>
<span data-ttu-id="bacbd-110">Använd cmdleten **Remove-AzureAccount** för att logga ut från kontot.</span><span class="sxs-lookup"><span data-stu-id="bacbd-110">To log out of the account, use the **Remove-AzureAccount** cmdlet.</span></span>

<span data-ttu-id="bacbd-111">**AzureAccount** laddar ned information om ditt Azure-konto och sparar det i en prenumerations data fil i din centrala användar profil.</span><span class="sxs-lookup"><span data-stu-id="bacbd-111">**Add-AzureAccount** downloads information about your Azure account and saves it in a subscription data file in your roaming user profile.</span></span>
<span data-ttu-id="bacbd-112">Den får också en åtkomsttoken som gör att Windows PowerShell får åtkomst till ditt Azure-konto åt dig.</span><span class="sxs-lookup"><span data-stu-id="bacbd-112">It also gets an access token that allows Windows PowerShell to access your Azure account on your behalf.</span></span>
<span data-ttu-id="bacbd-113">När kommandot är klart kan du hantera ditt Azure-konto i Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bacbd-113">When the command completes, you can manage your Azure account in Windows PowerShell.</span></span>

<span data-ttu-id="bacbd-114">Det finns två sätt att göra ditt Azure-konto tillgängligt för Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bacbd-114">There are two different ways to make your Azure account available to Windows PowerShell.</span></span>
<span data-ttu-id="bacbd-115">Du kan använda cmdleten **Add-AzureAccount** , som använder ett Management-token i Azure Active Directory (Azure AD)-autentiseringstoken eller **import-AzurePublishSettingsFile**.</span><span class="sxs-lookup"><span data-stu-id="bacbd-115">You can use the **Add-AzureAccount** cmdlet, which uses Azure Active Directory (Azure AD) authentication access tokens, or **Import-AzurePublishSettingsFile** , which uses a management certificate.</span></span>
<span data-ttu-id="bacbd-116">Råd om vilken metod som ska användas finns i [så här ansluter du till prenumerationen](https://azure.microsoft.com/documentation/articles/install-configure-powershell) ( https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect) .</span><span class="sxs-lookup"><span data-stu-id="bacbd-116">For guidance on which method to use, see [How to: Connect to your subscription](https://azure.microsoft.com/documentation/articles/install-configure-powershell) (https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect).</span></span>

<span data-ttu-id="bacbd-117">När du kör **Add-AzureAccount** visas ett interaktivt fönster där du uppmanas att logga in på ditt Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="bacbd-117">When you run **Add-AzureAccount** , it displays an interactive window that prompts you to sign into your Azure account.</span></span>
<span data-ttu-id="bacbd-118">Denna inloggning är giltig tills åtkomst-token upphör.</span><span class="sxs-lookup"><span data-stu-id="bacbd-118">This sign-in is valid until the access token expires.</span></span>
<span data-ttu-id="bacbd-119">När den upphör kan du använda cmdletar som kräver åtkomst till ditt konto för att köra **Add-AzureAccount** igen.</span><span class="sxs-lookup"><span data-stu-id="bacbd-119">When it expires, cmdlets that require access to your account prompt you to run **Add-AzureAccount** again.</span></span>

<span data-ttu-id="bacbd-120">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="bacbd-120">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="bacbd-121">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="bacbd-121">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="bacbd-122">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bacbd-122">EXAMPLES</span></span>

### <span data-ttu-id="bacbd-123">Exempel 1: Lägg till ett konto</span><span class="sxs-lookup"><span data-stu-id="bacbd-123">Example 1: Add an account</span></span>
```
PS C:\> Add-AzureAccount
```

<span data-ttu-id="bacbd-124">Det här kommandot lägger till ett Azure-konto i Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bacbd-124">This command adds an Azure account to Windows PowerShell.</span></span>
<span data-ttu-id="bacbd-125">När du kör kommandot öppnas ett fönster där du kan begära användar namn och lösen ord för kontot.</span><span class="sxs-lookup"><span data-stu-id="bacbd-125">When you run the command, a windows pops up to request the user name and password of the account.</span></span>

### <span data-ttu-id="bacbd-126">Exempel 2: använda en alternativ fil för abonnemang</span><span class="sxs-lookup"><span data-stu-id="bacbd-126">Example 2: Use an alternate subscription data file</span></span>
```
PS C:\> Add-AzureAccount -SubscriptionDataFile C:\Testing\SDF.xml
```

<span data-ttu-id="bacbd-127">Det här kommandot använder parametern **SubscriptionDataFile** till att **lägga till AzureAccount** för att lagra konto data i C:\Testing\SDF.xml filen i stället för standard filen.</span><span class="sxs-lookup"><span data-stu-id="bacbd-127">This command uses the **SubscriptionDataFile** parameter to direct **Add-AzureAccount** to store the account data in the C:\Testing\SDF.xml file, instead of the default file.</span></span>

## <span data-ttu-id="bacbd-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bacbd-128">PARAMETERS</span></span>

### <span data-ttu-id="bacbd-129">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="bacbd-129">-Credential</span></span>
```yaml
Type: PSCredential
Parameter Sets: User
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bacbd-130">-Miljö</span><span class="sxs-lookup"><span data-stu-id="bacbd-130">-Environment</span></span>
<span data-ttu-id="bacbd-131">Anger en Azure-miljö.</span><span class="sxs-lookup"><span data-stu-id="bacbd-131">Specifies an Azure environment.</span></span>

<span data-ttu-id="bacbd-132">En Azure-miljö en oberoende distribution av Microsoft Azure, till exempel AzureCloud för globala Azure-och AzureChinaCloud för Azure som drivs av 21Vianet i Kina.</span><span class="sxs-lookup"><span data-stu-id="bacbd-132">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="bacbd-133">Du kan också skapa lokala Azure-miljöer med Azure Pack och WAPack cmdlets.</span><span class="sxs-lookup"><span data-stu-id="bacbd-133">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="bacbd-134">Mer information finns i [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="bacbd-134">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bacbd-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="bacbd-135">-Profile</span></span>
<span data-ttu-id="bacbd-136">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="bacbd-136">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="bacbd-137">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="bacbd-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bacbd-138">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bacbd-138">-ServicePrincipal</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bacbd-139">-Klient organisationen</span><span class="sxs-lookup"><span data-stu-id="bacbd-139">-Tenant</span></span>
```yaml
Type: String
Parameter Sets: User
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bacbd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bacbd-140">CommonParameters</span></span>
<span data-ttu-id="bacbd-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bacbd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bacbd-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bacbd-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bacbd-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bacbd-143">INPUTS</span></span>

### <span data-ttu-id="bacbd-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="bacbd-144">None</span></span>
<span data-ttu-id="bacbd-145">Det går inte att pipe in i denna cmdlet</span><span class="sxs-lookup"><span data-stu-id="bacbd-145">You cannot pipe input to this cmdlet</span></span>

## <span data-ttu-id="bacbd-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bacbd-146">OUTPUTS</span></span>

### <span data-ttu-id="bacbd-147">Ingen</span><span class="sxs-lookup"><span data-stu-id="bacbd-147">None</span></span>
<span data-ttu-id="bacbd-148">Denna cmdlet returnerar inte några utdata.</span><span class="sxs-lookup"><span data-stu-id="bacbd-148">This cmdlet does not return any output.</span></span>

## <span data-ttu-id="bacbd-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bacbd-149">NOTES</span></span>
* <span data-ttu-id="bacbd-150">**Add-AzureAccount** (och Azure AD-autentiseringsmetoden) har högre prioritet än **import-AzurePublishSettings** (och hanterings certifikat).</span><span class="sxs-lookup"><span data-stu-id="bacbd-150">**Add-AzureAccount** (and the Azure AD authentication method) takes precedence over **Import-AzurePublishSettings** (and the management certificate method).</span></span> <span data-ttu-id="bacbd-151">Om du använder **Add-AzureAccount** även en gång på ditt konto används AUTENTISERINGSMETODEN Azure AD och hanterings certifikatet ignoreras.</span><span class="sxs-lookup"><span data-stu-id="bacbd-151">If you use **Add-AzureAccount** even once on your account, the Azure AD authentication method is used and the management certificate is ignored.</span></span> <span data-ttu-id="bacbd-152">Använd cmdleten **Remove-AzureAccount** om du vill ta bort Azure AD-token och återställa hanterings certifikat metoden.</span><span class="sxs-lookup"><span data-stu-id="bacbd-152">To remove the Azure AD token and restore the management certificate method, use the **Remove-AzureAccount** cmdlet.</span></span> <span data-ttu-id="bacbd-153">Om du vill ha mer information skriver du: **Get-Help Remove-AzureAccount**.</span><span class="sxs-lookup"><span data-stu-id="bacbd-153">For more information, type: **Get-Help Remove-AzureAccount**.</span></span>
* <span data-ttu-id="bacbd-154">Felet "dina uppgifter har upphört att gälla.</span><span class="sxs-lookup"><span data-stu-id="bacbd-154">The error, "Your credentials have expired.</span></span> <span data-ttu-id="bacbd-155">Använd Add-AzureAccount för att logga in igen. "</span><span class="sxs-lookup"><span data-stu-id="bacbd-155">Please use Add-AzureAccount to log in again."</span></span> <span data-ttu-id="bacbd-156">anger att din åtkomsttoken har upphört att gälla och Windows PowerShell inte kan komma åt ditt Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="bacbd-156">indicates that your access token is expired and Windows PowerShell cannot access your Azure account.</span></span> <span data-ttu-id="bacbd-157">Återställ åtkomst till kontot genom att köra **Add-AzureAccount** igen.</span><span class="sxs-lookup"><span data-stu-id="bacbd-157">To restore access to your account, run **Add-AzureAccount** again.</span></span>
* <span data-ttu-id="bacbd-158">Azure PowerShell-konto och prenumerations-cmdlets hämtar data från data filen för abonnemang, inte från det aktiva Azure-kontot.</span><span class="sxs-lookup"><span data-stu-id="bacbd-158">The Azure PowerShell account and subscription cmdlets get their data from the  subscription data file, not from the live Azure account.</span></span> <span data-ttu-id="bacbd-159">Om du ändrar ditt konto eller dina prenumerationer utanför Windows PowerShell, till exempel med Azure Management Portal, kör du **Add-AzureAccount** igen för att uppdatera prenumerations data filen.</span><span class="sxs-lookup"><span data-stu-id="bacbd-159">If you change your account or subscriptions outside of Windows PowerShell, such as by using the Azure Management Portal, run **Add-AzureAccount** again to refresh the subscription data file.</span></span>

## <span data-ttu-id="bacbd-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bacbd-160">RELATED LINKS</span></span>

[<span data-ttu-id="bacbd-161">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="bacbd-161">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="bacbd-162">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="bacbd-162">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="bacbd-163">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="bacbd-163">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="bacbd-164">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="bacbd-164">Get-AzureAccount</span></span>](./Get-AzureAccount.md)

[<span data-ttu-id="bacbd-165">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="bacbd-165">Remove-AzureAccount</span></span>](./Remove-AzureAccount.md)


