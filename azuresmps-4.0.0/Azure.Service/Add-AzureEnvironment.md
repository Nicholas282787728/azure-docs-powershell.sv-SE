---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6C435518-06EA-41B7-9585-44107B026FF1
online version: ''
schema: 2.0.0
ms.openlocfilehash: b04ceff5c4c49fe0e03e1e2c3da94c118323d653
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093456"
---
# <span data-ttu-id="28026-101">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="28026-101">Add-AzureEnvironment</span></span>

## <span data-ttu-id="28026-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="28026-102">SYNOPSIS</span></span>
<span data-ttu-id="28026-103">Skapar en Azure-miljö.</span><span class="sxs-lookup"><span data-stu-id="28026-103">Creates an Azure environment.</span></span>

## <span data-ttu-id="28026-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="28026-104">SYNTAX</span></span>

```
Add-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="28026-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="28026-105">DESCRIPTION</span></span>
<span data-ttu-id="28026-106">Cmdleten **Add-AzureEnvironment** skapar en ny anpassad Azure-domänmiljö och sparar den i din centrala användar profil.</span><span class="sxs-lookup"><span data-stu-id="28026-106">The **Add-AzureEnvironment** cmdlet creates a new custom Azure account environment and saves it in your roaming user profile.</span></span>
<span data-ttu-id="28026-107">Cmdleten returnerar ett objekt som representerar den nya miljön.</span><span class="sxs-lookup"><span data-stu-id="28026-107">The cmdlet returns an object that represents the new environment.</span></span>
<span data-ttu-id="28026-108">När kommandot är klart kan du använda miljön i Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="28026-108">When the command completes, you can use the environment in Windows PowerShell.</span></span>

<span data-ttu-id="28026-109">En Azure-miljö en oberoende distribution av Microsoft Azure, till exempel AzureCloud för globala Azure-och AzureChinaCloud för Azure som drivs av 21Vianet i Kina.</span><span class="sxs-lookup"><span data-stu-id="28026-109">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="28026-110">Du kan också skapa lokala Azure-miljöer med Azure Pack och WAPack cmdlets.</span><span class="sxs-lookup"><span data-stu-id="28026-110">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="28026-111">Mer information finns i [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="28026-111">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="28026-112">Endast parametern **Name** för denna cmdlet är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="28026-112">Only the **Name** parameter of this cmdlet is mandatory.</span></span>
<span data-ttu-id="28026-113">Om du utelämnar en parameter är dess värde null ($Null) och tjänsten som använder slut punkten kanske inte fungerar korrekt.</span><span class="sxs-lookup"><span data-stu-id="28026-113">If you omit a parameter, its value is null ($Null), and the service that uses that endpoint might not function properly.</span></span>
<span data-ttu-id="28026-114">Använd cmdleten **set-AzureEnvironment** för att lägga till eller ändra värdet för en miljö egenskap.</span><span class="sxs-lookup"><span data-stu-id="28026-114">To add or change the value of an environment property, use the **Set-AzureEnvironment** cmdlet.</span></span>

<span data-ttu-id="28026-115">Obs! Om du ändrar din miljö kan det leda till att ditt konto inte fungerar.</span><span class="sxs-lookup"><span data-stu-id="28026-115">NOTE: Changing your environment can cause your account to fail.</span></span>
<span data-ttu-id="28026-116">Miljöer läggs ofta till för testning eller fel sökning.</span><span class="sxs-lookup"><span data-stu-id="28026-116">Typically, environments are added only for testing or troubleshooting.</span></span>

<span data-ttu-id="28026-117">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="28026-117">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="28026-118">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="28026-118">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="28026-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="28026-119">EXAMPLES</span></span>

### <span data-ttu-id="28026-120">Exempel 1: lägga till en Azure-miljö</span><span class="sxs-lookup"><span data-stu-id="28026-120">Example 1: Add an Azure environment</span></span>
```
PS C:\> Add-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl https://contoso.com/fwlink/?LinkID=101 -ServiceEndpoint https://contoso.com/fwlink/?LinkID=102

Name                          : ContosoEnv

PublishSettingsFileUrl        : https://contoso.com/fwlink/?LinkID=101

ServiceEndpoint               : https://contoso.com/fwlink/?LinkID=102

ResourceManagerEndpoint       : 

ManagementPortalUrl           : 

ActiveDirectoryEndpoint       : 

ActiveDirectoryCommonTenantId : 

StorageEndpointSuffix         : 

StorageBlobEndpointFormat     : 

StorageQueueEndpointFormat    : 

StorageTableEndpointFormat    : 

GalleryEndpoint               :
```

<span data-ttu-id="28026-121">Det här kommandot skapar ContosoEnv Azure Environment.</span><span class="sxs-lookup"><span data-stu-id="28026-121">This command creates the ContosoEnv Azure environment.</span></span>

## <span data-ttu-id="28026-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="28026-122">PARAMETERS</span></span>

### <span data-ttu-id="28026-123">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="28026-123">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="28026-124">Anger slut punkten för Azure Active Directory-identifiering i den nya miljön.</span><span class="sxs-lookup"><span data-stu-id="28026-124">Specifies the endpoint for Azure Active Directory authentication in the new environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28026-125">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="28026-125">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="28026-126">Anger resurs-ID för ett Management API vars åtkomst hanteras av Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="28026-126">Specifies the resource ID of a management API whose access is managed by Azure Active Directory.</span></span>

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

### <span data-ttu-id="28026-127">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="28026-127">-AdTenant</span></span>
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

### <span data-ttu-id="28026-128">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="28026-128">-AzureKeyVaultDnsSuffix</span></span>
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

### <span data-ttu-id="28026-129">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="28026-129">-AzureKeyVaultServiceEndpointResourceId</span></span>
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

### <span data-ttu-id="28026-130">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="28026-130">-EnableAdfsAuthentication</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28026-131">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="28026-131">-GalleryEndpoint</span></span>
<span data-ttu-id="28026-132">Anger slut punkten för Azure Resource Manager-galleriet som lagrar mallar för resurs grupps gallerier.</span><span class="sxs-lookup"><span data-stu-id="28026-132">Specifies the endpoint for the Azure Resource Manager gallery, which stores resource group gallery templates.</span></span>
<span data-ttu-id="28026-133">Mer information om mallar för Azure-resursinformation och-gallerier finns i hjälp avsnittet för Get-AzureResourceGroupGalleryTemplate https://go.microsoft.com/fwlink/?LinkID=393052 .</span><span class="sxs-lookup"><span data-stu-id="28026-133">For more information about Azure resource groups and gallery templates, see the help topic for Get-AzureResourceGroupGalleryTemplatehttps://go.microsoft.com/fwlink/?LinkID=393052.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28026-134">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="28026-134">-GraphEndpoint</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28026-135">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="28026-135">-ManagementPortalUrl</span></span>
<span data-ttu-id="28026-136">Anger URL-adressen för Azure-hanteringskonsolen i den nya miljön.</span><span class="sxs-lookup"><span data-stu-id="28026-136">Specifies the URL of the Azure Management Portal in the new environment.</span></span>

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

### <span data-ttu-id="28026-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="28026-137">-Name</span></span>
<span data-ttu-id="28026-138">Anger ett namn för miljön.</span><span class="sxs-lookup"><span data-stu-id="28026-138">Specifies a name for the environment.</span></span>
<span data-ttu-id="28026-139">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="28026-139">This parameter is required.</span></span>
<span data-ttu-id="28026-140">Använd inte namnen på standard miljöerna, AzureCloud och AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="28026-140">Do not use the names of the default environments, AzureCloud and AzureChinaCloud.</span></span>

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

### <span data-ttu-id="28026-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="28026-141">-Profile</span></span>
<span data-ttu-id="28026-142">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="28026-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="28026-143">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="28026-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="28026-144">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="28026-144">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="28026-145">Anger URL-adressen till filerna för publicerings inställningar för ditt konto.</span><span class="sxs-lookup"><span data-stu-id="28026-145">Specifies the URL of the publish settings files for your account.</span></span>
<span data-ttu-id="28026-146">En fil för Azure publicerings inställningar är en XML-fil som innehåller information om ditt konto och ett hanterings certifikat som tillåter att Windows PowerShell loggar in på ditt Azure-konto åt dig.</span><span class="sxs-lookup"><span data-stu-id="28026-146">An Azure publish settings file is an XML file that contains information about your account and a management certificate that allows Windows PowerShell to sign into your Azure account on your behalf.</span></span>

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

### <span data-ttu-id="28026-147">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="28026-147">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="28026-148">Anger slut punkten för Azure Resource Manager-data, inklusive data om resurs grupper som är kopplade till kontot.</span><span class="sxs-lookup"><span data-stu-id="28026-148">Specifies the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="28026-149">Mer information om Azure Resource Manager finns i [Azure Resource Manager-cmdlet](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) och [med Windows PowerShell med Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  ( https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="28026-149">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28026-150">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="28026-150">-ServiceEndpoint</span></span>
<span data-ttu-id="28026-151">Anger URL-adressen för Azure-tjänstens slut punkt.</span><span class="sxs-lookup"><span data-stu-id="28026-151">Specifies the URL of the Azure service endpoint.</span></span>
<span data-ttu-id="28026-152">Azure-tjänstens slut punkt avgör om programmet hanteras av den globala Azure Platform, Azure som drivs av 21Vianet i Kina eller en privat Azure-installation.</span><span class="sxs-lookup"><span data-stu-id="28026-152">The Azure service endpoint determines whether your application is managed by the global Azure platform, Azure operated by 21Vianet in China, or a private Azure installation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28026-153">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="28026-153">-SqlDatabaseDnsSuffix</span></span>
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

### <span data-ttu-id="28026-154">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="28026-154">-StorageEndpoint</span></span>
<span data-ttu-id="28026-155">Anger standard slut punkten för lagrings tjänster i den nya miljön.</span><span class="sxs-lookup"><span data-stu-id="28026-155">Specifies the default endpoint of storage services in the new environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28026-156">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="28026-156">-TrafficManagerDnsSuffix</span></span>
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

### <span data-ttu-id="28026-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28026-157">CommonParameters</span></span>
<span data-ttu-id="28026-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28026-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28026-159">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28026-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28026-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="28026-160">INPUTS</span></span>

### <span data-ttu-id="28026-161">Ingen</span><span class="sxs-lookup"><span data-stu-id="28026-161">None</span></span>
<span data-ttu-id="28026-162">Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="28026-162">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="28026-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="28026-163">OUTPUTS</span></span>

### <span data-ttu-id="28026-164">Microsoft. WindowsAzure. commands. Utilitiess. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="28026-164">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>

## <span data-ttu-id="28026-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="28026-165">NOTES</span></span>

## <span data-ttu-id="28026-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="28026-166">RELATED LINKS</span></span>

[<span data-ttu-id="28026-167">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="28026-167">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="28026-168">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="28026-168">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)

[<span data-ttu-id="28026-169">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="28026-169">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


