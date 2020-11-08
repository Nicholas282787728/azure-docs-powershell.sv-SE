---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: A5419F76-B85E-445D-84EA-CC695B175C8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1364cf1bbec1fdca2a8c9901556d38de0b620358
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093359"
---
# <span data-ttu-id="ab1d1-101">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="ab1d1-101">Get-AzurePublishSettingsFile</span></span>

## <span data-ttu-id="ab1d1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab1d1-102">SYNOPSIS</span></span>
<span data-ttu-id="ab1d1-103">Laddar ned filen för publicerings inställningar för en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-103">Downloads the publish settings file for an Azure subscription.</span></span>

## <span data-ttu-id="ab1d1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab1d1-104">SYNTAX</span></span>

```
Get-AzurePublishSettingsFile [-Environment <String>] [-Realm <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab1d1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab1d1-105">DESCRIPTION</span></span>
<span data-ttu-id="ab1d1-106">Cmdleten **Get-AzurePublishSettingsFile** laddar ned en fil för publicerings inställningar för en prenumeration på ditt konto.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-106">The **Get-AzurePublishSettingsFile** cmdlet downloads a publish settings file for a subscription in your account.</span></span>
<span data-ttu-id="ab1d1-107">När kommandot är klart kan du använda cmdleten **import-PublishSettingsFile** för att göra inställningarna i filen tillgängliga för Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-107">When the command completes, you can use the **Import-PublishSettingsFile** cmdlet to make the settings in the file available to Windows PowerShell.</span></span>

<span data-ttu-id="ab1d1-108">Om du vill göra ditt Azure-konto tillgängligt för Windows PowerShell kan du använda en fil för publicerings inställningar eller cmdleten **Add-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="ab1d1-108">To make your Azure account available to Windows PowerShell, you can use a publish settings file or the **Add-AzureAccount** cmdlet.</span></span>
<span data-ttu-id="ab1d1-109">Med publicerings inställningar kan du förbereda sessionen i förväg så att skript och bakgrunds jobb inte körs.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-109">Publish settings files let you prepare the session in advance so you can run scripts and background jobs unattended.</span></span>
<span data-ttu-id="ab1d1-110">Men alla tjänster stöder inte publicerings inställningar.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-110">However, not all services support publish settings files.</span></span>
<span data-ttu-id="ab1d1-111">**AzureResourceManager** -modulen stöder till exempel inte publicerings inställningar.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-111">For example, the **AzureResourceManager** module does not support publish settings files.</span></span>

<span data-ttu-id="ab1d1-112">När du kör **Get-AzurePublishSettingsFile** öppnas standard webbläsaren och du uppmanas att logga in på ditt Azure-konto, välja ett abonnemang och välja en plats för fil system för publicerings inställnings filen.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-112">When you run **Get-AzurePublishSettingsFile** , it opens your default browser and prompts you to sign into your Azure account, select a subscription, and select a file system location for the publish settings file.</span></span>
<span data-ttu-id="ab1d1-113">Sedan hämtas filen för publicerings inställningar för ditt abonnemang till den valda filen.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-113">Then, it downloads the publish settings file for your subscription into the file that you selected.</span></span>

<span data-ttu-id="ab1d1-114">En "publicerings inställnings fil" är en XML-fil med fil namns tillägget. publishsettings.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-114">A "publish settings file" is an XML file with a .publishsettings file name extension.</span></span>
<span data-ttu-id="ab1d1-115">Filen innehåller ett kodat certifikat som innehåller administratörsautentiseringsuppgifter för dina Azure-prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-115">The file contains an encoded certificate that provides management credentials for your Azure subscriptions.</span></span>

<span data-ttu-id="ab1d1-116">**Säkerhets meddelande:** Publicering Settings innehåller autentiseringsuppgifter som används för att administrera dina Azure-abonnemang och-tjänster.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-116">**Security Note:** Publish settings files contains credentials that are used to administer your Azure subscriptions and services.</span></span>
<span data-ttu-id="ab1d1-117">Om illvilliga användare kommer åt filen för publicerings inställningar kan de redigera, skapa och ta bort dina Azure-tjänster.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-117">If  malicious users access your publish settings file,  they can edit, create, and delete your Azure services.</span></span>
<span data-ttu-id="ab1d1-118">Av säkerhets skäl bör du spara filen på en plats i mappen Hämtade filer eller dokument och sedan ta bort den när du har använt cmdleten **import-AzurePublishSettingsFile** för att importera inställningarna.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-118">As a security best practice, save the file to a location in your Downloads or Documents folder and then delete it after using **Import-AzurePublishSettingsFile** cmdlet to import the settings.</span></span>

<span data-ttu-id="ab1d1-119">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-119">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ab1d1-120">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ab1d1-120">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="ab1d1-121">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab1d1-121">EXAMPLES</span></span>

### <span data-ttu-id="ab1d1-122">Exempel 1: Ladda ned en fil för publicerings inställningar</span><span class="sxs-lookup"><span data-stu-id="ab1d1-122">Example 1: Download a publish settings file</span></span>
```
PS C:\> Get-AzurePublishSettingsFile
```

<span data-ttu-id="ab1d1-123">Det här kommandot öppnar standard webbläsaren, ansluter till ditt Windows Azure-konto och laddar sedan ned. publishsettings-filen för ditt konto.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-123">This command opens your default browser, connects to your Windows Azure account, and then downloads the .publishsettings file for your account.</span></span>

### <span data-ttu-id="ab1d1-124">Exempel 2: Ange en sfär</span><span class="sxs-lookup"><span data-stu-id="ab1d1-124">Example 2: Specify a realm</span></span>
```
PS C:\> Get-AzurePublishSettingsFile -Realm contoso.com -Passthru
```

<span data-ttu-id="ab1d1-125">Det här kommandot laddar ned filen för publicerings inställningar för ett konto i contoso.com-domänen.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-125">This command downloads the publish settings file for an account in the contoso.com domain.</span></span>
<span data-ttu-id="ab1d1-126">Använd ett kommando med parametern **Realm** när du loggar in på Azure med ett organisations konto i stället för ett Microsoft-konto.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-126">Use a command with the **Realm** parameter when you sign into Azure with an organizational account, instead of a Microsoft account.</span></span>

## <span data-ttu-id="ab1d1-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab1d1-127">PARAMETERS</span></span>

### <span data-ttu-id="ab1d1-128">-Miljö</span><span class="sxs-lookup"><span data-stu-id="ab1d1-128">-Environment</span></span>
<span data-ttu-id="ab1d1-129">Anger en Azure-miljö.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-129">Specifies an Azure environment.</span></span>

<span data-ttu-id="ab1d1-130">En Azure-miljö en oberoende distribution av Microsoft Azure, till exempel AzureCloud för globala Azure-och AzureChinaCloud för Azure som drivs av 21Vianet i Kina.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-130">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="ab1d1-131">Du kan också skapa lokala Azure-miljöer med Azure Pack och WAPack cmdlets.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-131">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="ab1d1-132">Mer information finns i [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ab1d1-132">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="ab1d1-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab1d1-133">-PassThru</span></span>
<span data-ttu-id="ab1d1-134">Returnerar $True om kommandot lyckas och $False om det inte fungerar.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-134">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="ab1d1-135">Denna cmdlet returnerar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-135">By default, this cmdlet does not return any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab1d1-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="ab1d1-136">-Profile</span></span>
<span data-ttu-id="ab1d1-137">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-137">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="ab1d1-138">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ab1d1-139">-Realm</span><span class="sxs-lookup"><span data-stu-id="ab1d1-139">-Realm</span></span>
<span data-ttu-id="ab1d1-140">Anger organisationen i ett organisations-ID.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-140">Specifies the organization in an organizational ID.</span></span>
<span data-ttu-id="ab1d1-141">Om du till exempel loggar in på Azure as admin@contoso.com är värdet för parametern **Realm** contoso.com.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-141">For example, if you sign into Azure as admin@contoso.com, the value of the **Realm** parameter is contoso.com.</span></span>
<span data-ttu-id="ab1d1-142">Använd den här parametern när du loggar in på Azure-portalen med ett organisations-ID.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-142">Use this parameter when you use an organizational ID to sign into the Azure portal.</span></span>
<span data-ttu-id="ab1d1-143">Denna parameter behövs inte när du använder ett Microsoft-konto, till exempel ett outlook.com-eller live.com-konto.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-143">This parameter is not required when you use a Microsoft account, such as an outlook.com or live.com account.</span></span>

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

### <span data-ttu-id="ab1d1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab1d1-144">CommonParameters</span></span>
<span data-ttu-id="ab1d1-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab1d1-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab1d1-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab1d1-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab1d1-147">INPUTS</span></span>

### <span data-ttu-id="ab1d1-148">Ingen</span><span class="sxs-lookup"><span data-stu-id="ab1d1-148">None</span></span>
<span data-ttu-id="ab1d1-149">Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-149">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="ab1d1-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab1d1-150">OUTPUTS</span></span>

### <span data-ttu-id="ab1d1-151">Ingen eller system. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab1d1-151">None or System.Boolean</span></span>
<span data-ttu-id="ab1d1-152">När du använder parametern *Passthru* returnerar denna cmdlet ett Boolean-värde.</span><span class="sxs-lookup"><span data-stu-id="ab1d1-152">When you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="ab1d1-153">Annars returnerar denna cmdlet inte något utdata</span><span class="sxs-lookup"><span data-stu-id="ab1d1-153">Otherwise, this cmdlet does not return any output</span></span>

## <span data-ttu-id="ab1d1-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab1d1-154">NOTES</span></span>

## <span data-ttu-id="ab1d1-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab1d1-155">RELATED LINKS</span></span>

[<span data-ttu-id="ab1d1-156">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="ab1d1-156">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="ab1d1-157">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="ab1d1-157">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)


