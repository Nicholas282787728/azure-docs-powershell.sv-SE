---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 79D64D7C-6671-4F03-8776-70A716F36512
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bc0525ee7238de421842b74f52f7dd4fa59df1a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099491"
---
# <span data-ttu-id="01d04-101">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="01d04-101">Import-AzurePublishSettingsFile</span></span>

## <span data-ttu-id="01d04-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="01d04-102">SYNOPSIS</span></span>
<span data-ttu-id="01d04-103">Importerar en fil för publicerings inställningar som låter dig hantera dina Azure-konton i Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="01d04-103">Imports a publish settings file that lets you manage your Azure accounts in Windows PowerShell.</span></span>

## <span data-ttu-id="01d04-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="01d04-104">SYNTAX</span></span>

```
Import-AzurePublishSettingsFile -PublishSettingsFile <String> [-Environment <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="01d04-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="01d04-105">DESCRIPTION</span></span>
<span data-ttu-id="01d04-106">Cmdleten **import-AzurePublishSettingsFile** importerar en fil för publicerings inställningar (\*. publishsettings) som innehåller information om dina Azure-konton och sparar en prenumerations data fil på datorn.</span><span class="sxs-lookup"><span data-stu-id="01d04-106">The **Import-AzurePublishSettingsFile** cmdlet imports a publish settings file (\*.publishsettings) that contains information about your Azure accounts and saves a subscription data file on your computer.</span></span>
<span data-ttu-id="01d04-107">När cmdleten är slutförd kan du hantera dina Azure-konton i Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="01d04-107">When the cmdlet completes, you can manage your Azure accounts in Windows PowerShell.</span></span>

<span data-ttu-id="01d04-108">Innan du kör **import-AzurePublishSettingsFile** kör du **Get-AzurePublishSettingsFile** , som laddar ned och sparar filen publicerings inställningar så att du kan importera den.</span><span class="sxs-lookup"><span data-stu-id="01d04-108">Before running **Import-AzurePublishSettingsFile** , run **Get-AzurePublishSettingsFile** , which downloads and saves the publish settings file so you can import it.</span></span>

<span data-ttu-id="01d04-109">Om du vill göra ditt Azure-konto tillgängligt för Windows PowerShell kan du använda en fil för publicerings inställningar eller cmdleten **Add-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="01d04-109">To make your Azure account available to Windows PowerShell, you can use a publish settings file or the **Add-AzureAccount** cmdlet.</span></span>
<span data-ttu-id="01d04-110">Med publicerings inställningar kan du förbereda sessionen i förväg så att skript och bakgrunds jobb inte körs.</span><span class="sxs-lookup"><span data-stu-id="01d04-110">Publish settings files let you prepare the session in advance so you can run scripts and background jobs unattended.</span></span>
<span data-ttu-id="01d04-111">Men alla tjänster stöder inte publicerings inställningar.</span><span class="sxs-lookup"><span data-stu-id="01d04-111">However, not all services support publish settings files.</span></span>
<span data-ttu-id="01d04-112">**AzureResourceManager** -modulen stöder till exempel inte publicerings inställningar.</span><span class="sxs-lookup"><span data-stu-id="01d04-112">For example, the **AzureResourceManager** module does not support publish settings files.</span></span>

<span data-ttu-id="01d04-113">**Säkerhets meddelande:** Filer för publicerings inställningar innehåller ett Management-certifikat som är kodat, men inte krypterade.</span><span class="sxs-lookup"><span data-stu-id="01d04-113">**Security Note:** Publish settings files contain a management certificate that is encoded, but not encrypted.</span></span>
<span data-ttu-id="01d04-114">Om illvilliga användare kommer åt filen för publicerings inställningar kan de kunna redigera, skapa och ta bort dina Azure-tjänster.</span><span class="sxs-lookup"><span data-stu-id="01d04-114">If  malicious users access your publish settings file,  they might be able to edit, create, and delete your Azure services.</span></span>
<span data-ttu-id="01d04-115">Av säkerhets skäl bör du spara filen på en plats i mappen Hämtade filer eller dokument och sedan ta bort den när du har använt cmdleten **import-AzurePublishSettingsFile** för att importera inställningarna.</span><span class="sxs-lookup"><span data-stu-id="01d04-115">As a security best practice, save the file to a location in your Downloads or Documents folder and then delete it after using **Import-AzurePublishSettingsFile** cmdlet to import the settings.</span></span>

## <span data-ttu-id="01d04-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="01d04-116">EXAMPLES</span></span>

### <span data-ttu-id="01d04-117">Exempel 1: importera en fil</span><span class="sxs-lookup"><span data-stu-id="01d04-117">Example 1: Import a file</span></span>
```
PS C:\> Import-AzurePublishSettingsFile -PublishSettingsFile C:\Temp\MyAccount.publishsettings
```

<span data-ttu-id="01d04-118">Det här kommandot importerar "C:\Temp\MyAccount.publishsettings"-filen.</span><span class="sxs-lookup"><span data-stu-id="01d04-118">This command imports the "C:\Temp\MyAccount.publishsettings" file.</span></span>

## <span data-ttu-id="01d04-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="01d04-119">PARAMETERS</span></span>

### <span data-ttu-id="01d04-120">-Miljö</span><span class="sxs-lookup"><span data-stu-id="01d04-120">-Environment</span></span>
<span data-ttu-id="01d04-121">Anger en Azure-miljö.</span><span class="sxs-lookup"><span data-stu-id="01d04-121">Specifies an Azure environment.</span></span>

<span data-ttu-id="01d04-122">En Azure-miljö en oberoende distribution av Microsoft Azure, till exempel AzureCloud för globala Azure-och AzureChinaCloud för Azure som drivs av 21Vianet i Kina.</span><span class="sxs-lookup"><span data-stu-id="01d04-122">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="01d04-123">Du kan också skapa lokala Azure-miljöer med Azure Pack och WAPack cmdlets.</span><span class="sxs-lookup"><span data-stu-id="01d04-123">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="01d04-124">Mer information finns i [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="01d04-124">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="01d04-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="01d04-125">-Profile</span></span>
<span data-ttu-id="01d04-126">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="01d04-126">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="01d04-127">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="01d04-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="01d04-128">-PublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="01d04-128">-PublishSettingsFile</span></span>
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

### <span data-ttu-id="01d04-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01d04-129">CommonParameters</span></span>
<span data-ttu-id="01d04-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01d04-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01d04-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01d04-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01d04-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="01d04-132">INPUTS</span></span>

### <span data-ttu-id="01d04-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="01d04-133">None</span></span>
<span data-ttu-id="01d04-134">Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="01d04-134">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="01d04-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="01d04-135">OUTPUTS</span></span>

### <span data-ttu-id="01d04-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="01d04-136">None</span></span>
<span data-ttu-id="01d04-137">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="01d04-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="01d04-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="01d04-138">NOTES</span></span>
* <span data-ttu-id="01d04-139">En "publicerings inställnings fil" är en XML-fil med fil namns tillägget. publishsettings.</span><span class="sxs-lookup"><span data-stu-id="01d04-139">A "publish settings file" is an XML file with a .publishsettings file name extension.</span></span> <span data-ttu-id="01d04-140">Filen innehåller ett kodat certifikat som innehåller administratörsautentiseringsuppgifter för dina Azure-prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="01d04-140">The file contains an encoded certificate that provides management credentials for your Azure subscriptions.</span></span> <span data-ttu-id="01d04-141">När du har importerat filen tar du bort den för att undvika säkerhets risker.</span><span class="sxs-lookup"><span data-stu-id="01d04-141">After you import this file, delete it to avoid security risks.</span></span>
* <span data-ttu-id="01d04-142">En "prenumerations data fil" är en XML-fil som kan sparas på ett säkert sätt på din dator.</span><span class="sxs-lookup"><span data-stu-id="01d04-142">A "subscription data file" is an XML file that can be saved on your computer safely.</span></span> <span data-ttu-id="01d04-143">Den sparas som standard i din centrala användar profil ($home/AppData/Roaming).</span><span class="sxs-lookup"><span data-stu-id="01d04-143">By default, it's saved in your roaming user profile ($home/AppData/Roaming).</span></span>

## <span data-ttu-id="01d04-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="01d04-144">RELATED LINKS</span></span>

[<span data-ttu-id="01d04-145">Installera och konfigurera Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="01d04-145">How to Install and Configure Azure PowerShell</span></span>](https://azure.microsoft.com/documentation/articles/install-configure-powershell/)

[<span data-ttu-id="01d04-146">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="01d04-146">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="01d04-147">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="01d04-147">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)


