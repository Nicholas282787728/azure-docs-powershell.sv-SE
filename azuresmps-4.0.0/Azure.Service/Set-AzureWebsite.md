---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9D821623-DEF9-49E4-9C44-10643A92A2E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f6690aa45125a0d1b3383b08443234f47a1f7e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093159"
---
# <span data-ttu-id="793af-101">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="793af-101">Set-AzureWebsite</span></span>

## <span data-ttu-id="793af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="793af-102">SYNOPSIS</span></span>
<span data-ttu-id="793af-103">Konfigurerar en webbplats som körs i Azure.</span><span class="sxs-lookup"><span data-stu-id="793af-103">Configures a website running in Azure.</span></span>

## <span data-ttu-id="793af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="793af-104">SYNTAX</span></span>

```
Set-AzureWebsite [-NumberOfWorkers <Int32>] [-DefaultDocuments <String[]>] [-NetFrameworkVersion <String>]
 [-PhpVersion <String>] [-RequestTracingEnabled <Boolean>] [-HttpLoggingEnabled <Boolean>]
 [-DetailedErrorLoggingEnabled <Boolean>] [-HostNames <String[]>] [-AppSettings <Hashtable>]
 [-Metadata <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.NameValuePair]>]
 [-ConnectionStrings <ConnStringPropertyBag>] [-HandlerMappings <HandlerMapping[]>]
 [-SiteWithConfig <SiteWithConfig>] [-PassThru] [-ManagedPipelineMode <ManagedPipelineMode>]
 [-WebSocketsEnabled <Boolean>]
 [-RoutingRules <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.RoutingRule]>]
 [-Use32BitWorkerProcess <Boolean>] [-AutoSwapSlotName <String>]
 [-SlotStickyAppSettingNames <System.Collections.Generic.List`1[System.String]>]
 [-SlotStickyConnectionStringNames <System.Collections.Generic.List`1[System.String]>] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="793af-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="793af-105">DESCRIPTION</span></span>
<span data-ttu-id="793af-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="793af-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="793af-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="793af-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="793af-108">Cmdleten **set-AzureWebsite** konfigurerar en webbplats som körs i Azure.</span><span class="sxs-lookup"><span data-stu-id="793af-108">The **Set-AzureWebsite** cmdlet configures a website running in Azure.</span></span>

## <span data-ttu-id="793af-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="793af-109">EXAMPLES</span></span>

### <span data-ttu-id="793af-110">Exempel 1: Aktivera HTTP-loggning för en webbplats</span><span class="sxs-lookup"><span data-stu-id="793af-110">Example 1: Enable HTTP logging for a website</span></span>
```
PS C:\> Set-AzureWebsite -HttpLoggingEnabled 1
```

<span data-ttu-id="793af-111">Det här exemplet aktiverar HTTP-loggning.</span><span class="sxs-lookup"><span data-stu-id="793af-111">This example enables HTTP logging.</span></span>

### <span data-ttu-id="793af-112">Exempel 2: ange autentiseringsuppgifter för lagring för en webbplats</span><span class="sxs-lookup"><span data-stu-id="793af-112">Example 2: Set storage credentials for a website</span></span>
```
PS C:\> $settings = New-Object Hashtable$settings["AZURE_STORAGE_ACCOUNT"= myaccountname$settings["AZURE_STORAGE_ACCESS_KEY"] = myaccesskeySet-AzureWebsite -AppSettings $settings myWebsite
```

<span data-ttu-id="793af-113">I det här exemplet anges autentiseringsuppgifter för lagring på en webbplats som heter min webbplats med miljövariabler för AZURE_STORAGE_ACCOUNT och AZURE_STORAGE_ACCESS_KEY.</span><span class="sxs-lookup"><span data-stu-id="793af-113">This example sets storage credentials in a website named myWebsite with environment variables for AZURE_STORAGE_ACCOUNT and AZURE_STORAGE_ACCESS_KEY.</span></span>

## <span data-ttu-id="793af-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="793af-114">PARAMETERS</span></span>

### <span data-ttu-id="793af-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="793af-115">-AppSettings</span></span>
<span data-ttu-id="793af-116">Anger de miljövariabler som ska användas av webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="793af-116">Specifies the environment variables that will be used by the website.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="793af-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="793af-117">-AutoSwapSlotName</span></span>
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

### <span data-ttu-id="793af-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="793af-118">-ConnectionStrings</span></span>
<span data-ttu-id="793af-119">Anger de anslutnings strängar som används av webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="793af-119">Specifies the connection strings used by the website.</span></span>

```yaml
Type: ConnStringPropertyBag
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="793af-120">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="793af-120">-DefaultDocuments</span></span>
<span data-ttu-id="793af-121">Anger de dokument som visas automatiskt när du bläddrar på webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="793af-121">Specifies the documents that are automatically displayed when browsing the website.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="793af-122">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="793af-122">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="793af-123">Avgör om detaljerade IIS-fel loggas för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="793af-123">Determines whether detailed IIS errors are logged for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="793af-124">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="793af-124">-HandlerMappings</span></span>
<span data-ttu-id="793af-125">Anger den hanterarmappning som används av webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="793af-125">Specifies the handler mappings used by the website.</span></span>

```yaml
Type: HandlerMapping[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="793af-126">-Värdnamn</span><span class="sxs-lookup"><span data-stu-id="793af-126">-HostNames</span></span>
<span data-ttu-id="793af-127">Anger de fullkvalificerade värd namnen som kan användas för att komma åt webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="793af-127">Specifies the fully qualified host names that can be used to access the website.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="793af-128">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="793af-128">-HttpLoggingEnabled</span></span>
<span data-ttu-id="793af-129">Bestämmer om http-loggning är aktiverat för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="793af-129">Determines whether http logging is enabled for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="793af-130">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="793af-130">-ManagedPipelineMode</span></span>
<span data-ttu-id="793af-131">Anger hanterat pipeline-läge.</span><span class="sxs-lookup"><span data-stu-id="793af-131">Specifies the managed pipeline mode.</span></span>

```yaml
Type: ManagedPipelineMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="793af-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="793af-132">-Metadata</span></span>
<span data-ttu-id="793af-133">Anger webbplatsens metadata.</span><span class="sxs-lookup"><span data-stu-id="793af-133">Specifies the metadata for the website.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.NameValuePair]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="793af-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="793af-134">-Name</span></span>
<span data-ttu-id="793af-135">Anger namnet på webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="793af-135">Specifies the name of the website.</span></span>

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

### <span data-ttu-id="793af-136">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="793af-136">-NetFrameworkVersion</span></span>
<span data-ttu-id="793af-137">Anger vilken version av .NET Framework som behövs för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="793af-137">Specifies the version of the .Net Framework required by the website.</span></span>

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

### <span data-ttu-id="793af-138">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="793af-138">-NumberOfWorkers</span></span>
<span data-ttu-id="793af-139">Anger antalet arbets processer som körs på webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="793af-139">Specifies the number of worker processes running the website.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="793af-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="793af-140">-PassThru</span></span>
<span data-ttu-id="793af-141">Anger att den här cmdleten returnerar ett **booleskt** värde.</span><span class="sxs-lookup"><span data-stu-id="793af-141">Indicates that this cmdlet returns a **Boolean** value.</span></span>

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

### <span data-ttu-id="793af-142">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="793af-142">-PhpVersion</span></span>
<span data-ttu-id="793af-143">Anger vilken PHP-version som krävs av webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="793af-143">Specifies the PHP version required by the website.</span></span>

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

### <span data-ttu-id="793af-144">-Profil</span><span class="sxs-lookup"><span data-stu-id="793af-144">-Profile</span></span>
<span data-ttu-id="793af-145">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="793af-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="793af-146">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="793af-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="793af-147">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="793af-147">-RequestTracingEnabled</span></span>
<span data-ttu-id="793af-148">Avgör om begärans spårning är aktiverat för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="793af-148">Determines whether request tracing is enabled for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="793af-149">-RoutingRules</span><span class="sxs-lookup"><span data-stu-id="793af-149">-RoutingRules</span></span>
<span data-ttu-id="793af-150">Anger de routningsregler som ska användas för testning i produktion.</span><span class="sxs-lookup"><span data-stu-id="793af-150">Specifies the routing rules to use for testing in production.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.RoutingRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="793af-151">-SiteWithConfig</span><span class="sxs-lookup"><span data-stu-id="793af-151">-SiteWithConfig</span></span>
<span data-ttu-id="793af-152">Anger vilken konfiguration som används av webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="793af-152">Specifies the configuration used by the website.</span></span>

```yaml
Type: SiteWithConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="793af-153">-Plats</span><span class="sxs-lookup"><span data-stu-id="793af-153">-Slot</span></span>
<span data-ttu-id="793af-154">Anger webbplatsens namn.</span><span class="sxs-lookup"><span data-stu-id="793af-154">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="793af-155">-SlotStickyAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="793af-155">-SlotStickyAppSettingNames</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="793af-156">-SlotStickyConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="793af-156">-SlotStickyConnectionStringNames</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="793af-157">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="793af-157">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="793af-158">Anger om 32-bitars läget ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="793af-158">Specifies whether to enable 32-bit mode.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="793af-159">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="793af-159">-WebSocketsEnabled</span></span>
<span data-ttu-id="793af-160">Anger om du vill aktivera WebSockets.</span><span class="sxs-lookup"><span data-stu-id="793af-160">Specifies whether to enable WebSockets.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="793af-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="793af-161">CommonParameters</span></span>
<span data-ttu-id="793af-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="793af-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="793af-163">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="793af-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="793af-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="793af-164">INPUTS</span></span>

## <span data-ttu-id="793af-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="793af-165">OUTPUTS</span></span>

## <span data-ttu-id="793af-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="793af-166">NOTES</span></span>

## <span data-ttu-id="793af-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="793af-167">RELATED LINKS</span></span>

[<span data-ttu-id="793af-168">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="793af-168">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="793af-169">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="793af-169">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="793af-170">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="793af-170">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)


