---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 1094497D-2CBE-41DF-9ED1-8E7D3F14B05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82bd806d35f36a07958f2bdeeeda42853cd453b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099197"
---
# <span data-ttu-id="c9d2b-101">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="c9d2b-101">Set-AzureEnvironment</span></span>

## <span data-ttu-id="c9d2b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c9d2b-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d2b-103">Ändrar egenskaperna för en Azure-miljö.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-103">Changes the properties of an Azure environment.</span></span>

## <span data-ttu-id="c9d2b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c9d2b-104">SYNTAX</span></span>

```
Set-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c9d2b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c9d2b-105">DESCRIPTION</span></span>
<span data-ttu-id="c9d2b-106">Cmdleten **set-AzureEnvironment** ändrar egenskaperna för en Azure-miljö.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-106">The **Set-AzureEnvironment** cmdlet changes the properties of an Azure environment.</span></span>
<span data-ttu-id="c9d2b-107">Den returnerar ett objekt som representerar miljön med dess nya egenskaps värden.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-107">It returns an object that represents the environment with its new property values.</span></span>
<span data-ttu-id="c9d2b-108">Använd parametern **namn** för att identifiera miljön och andra parametrar för att ändra egenskaps värden.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-108">Use the **Name** parameter to identify the environment and the other parameters to change property values.</span></span>
<span data-ttu-id="c9d2b-109">Du kan inte använda **set-AzureEnvironment** för att ändra namnet på en Azure-miljö.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-109">You cannot use **Set-AzureEnvironment** to change the name of an Azure environment.</span></span>

<span data-ttu-id="c9d2b-110">En Azure-miljö en oberoende distribution av Microsoft Azure, till exempel AzureCloud för globala Azure-och AzureChinaCloud för Azure som drivs av 21Vianet i Kina.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-110">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="c9d2b-111">Du kan också skapa lokala Azure-miljöer med Azure Pack och WAPack cmdlets.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-111">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="c9d2b-112">Mer information finns i [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c9d2b-112">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="c9d2b-113">Obs! ändra inte egenskaperna för AzureCloud-eller AzureChinaCloud-miljöerna.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-113">NOTE:  Do not change the properties of the AzureCloud or AzureChinaCloud environments.</span></span>
<span data-ttu-id="c9d2b-114">Använd denna cmdlet för att ändra värdena för privata miljöer som du skapar.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-114">Use this cmdlet to change the values of private environments that you create.</span></span>

## <span data-ttu-id="c9d2b-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c9d2b-115">EXAMPLES</span></span>

### <span data-ttu-id="c9d2b-116">Exempel 1: ändra miljö egenskaper</span><span class="sxs-lookup"><span data-stu-id="c9d2b-116">Example 1: Change environment properties</span></span>
```
PS C:\> Set-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl "https://contoso.com" -StorageEndpoint "contoso.com"
```

<span data-ttu-id="c9d2b-117">Det här kommandot ändrar värdena för egenskaperna **PublishSettingsFileUrl** och **StorageEndpoint** för ContosoEnv-miljön.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-117">This command changes the values of the **PublishSettingsFileUrl** and **StorageEndpoint** properties of the ContosoEnv environment.</span></span>

## <span data-ttu-id="c9d2b-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c9d2b-118">PARAMETERS</span></span>

### <span data-ttu-id="c9d2b-119">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9d2b-119">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="c9d2b-120">Ändrar slut punkten för Azure Active Directory-verifikation till det angivna värdet.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-120">Changes the endpoint for Azure Active Directory authentication to the specified value.</span></span>

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

### <span data-ttu-id="c9d2b-121">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c9d2b-121">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="c9d2b-122">Anger resurs-ID för ett Management API vars åtkomst hanteras av Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-122">Specifies the resource ID of a management API whose access is managed by Azure Active Directory.</span></span>

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

### <span data-ttu-id="c9d2b-123">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="c9d2b-123">-AdTenant</span></span>
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

### <span data-ttu-id="c9d2b-124">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="c9d2b-124">-AzureKeyVaultDnsSuffix</span></span>
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

### <span data-ttu-id="c9d2b-125">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c9d2b-125">-AzureKeyVaultServiceEndpointResourceId</span></span>
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

### <span data-ttu-id="c9d2b-126">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="c9d2b-126">-EnableAdfsAuthentication</span></span>
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

### <span data-ttu-id="c9d2b-127">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9d2b-127">-GalleryEndpoint</span></span>
<span data-ttu-id="c9d2b-128">Ändrar slut punkten för Azure Resource Manager-galleriet till det angivna värdet.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-128">Changes the endpoint for the Azure Resource Manager gallery to the specified value.</span></span>
<span data-ttu-id="c9d2b-129">Galleriets slut punkt är placeringen av mallarna i resurs mal len.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-129">The gallery endpoint is the location for resource group gallery templates.</span></span>
<span data-ttu-id="c9d2b-130">Mer information om mallar för Azure-resursinformation och-gallerier finns i hjälp avsnittet för [Get-AzureResourceGroupGalleryTemplate](https://go.microsoft.com/fwlink/?LinkID=393052).</span><span class="sxs-lookup"><span data-stu-id="c9d2b-130">For more information about Azure resource groups and gallery templates, see the help topic for [Get-AzureResourceGroupGalleryTemplate](https://go.microsoft.com/fwlink/?LinkID=393052).</span></span>

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

### <span data-ttu-id="c9d2b-131">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9d2b-131">-GraphEndpoint</span></span>
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

### <span data-ttu-id="c9d2b-132">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="c9d2b-132">-ManagementPortalUrl</span></span>
<span data-ttu-id="c9d2b-133">Ändrar URL-adressen för Azure-hanteringskonsolen till det angivna värdet.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-133">Changes the URL of the Azure Management Portal to the specified value.</span></span>

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

### <span data-ttu-id="c9d2b-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="c9d2b-134">-Name</span></span>
<span data-ttu-id="c9d2b-135">Identifierar miljön som ändras.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-135">Identifies the environment that is being changed.</span></span>
<span data-ttu-id="c9d2b-136">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-136">This parameter is required.</span></span>
<span data-ttu-id="c9d2b-137">Parametervärdet är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-137">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="c9d2b-138">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-138">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="c9d2b-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="c9d2b-139">-Profile</span></span>
<span data-ttu-id="c9d2b-140">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-140">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c9d2b-141">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c9d2b-142">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="c9d2b-142">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="c9d2b-143">Ändrar URL-adressen för publicering Settings-filer i den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-143">Changes the URL for publish settings files in the specified environment.</span></span>
<span data-ttu-id="c9d2b-144">En fil för Azure publicerings inställningar är en XML-fil som innehåller information om ditt konto och ett hanterings certifikat som tillåter att Windows PowerShell loggar in på ditt Azure-konto åt dig.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-144">An Azure publish settings file is an XML file that contains information about your account and a management certificate that allows Windows PowerShell to sign into your Azure account on your behalf.</span></span>

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

### <span data-ttu-id="c9d2b-145">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9d2b-145">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="c9d2b-146">Ändrar slut punkten för Azure Resource Manager-data, inklusive data om resurs grupper som är kopplade till kontot.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-146">Changes the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="c9d2b-147">Mer information om Azure Resource Manager finns i [Azure Resource Manager-cmdlet](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) och [med Windows PowerShell med Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  ( https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="c9d2b-147">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

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

### <span data-ttu-id="c9d2b-148">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9d2b-148">-ServiceEndpoint</span></span>
<span data-ttu-id="c9d2b-149">Ändrar URL-adressen för Azure-tjänstens slut punkt i den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-149">Changes the URL of the Azure service endpoint in the specified environment.</span></span>
<span data-ttu-id="c9d2b-150">Azure-tjänstens slut punkt avgör om programmet hanteras av den globala Azure Platform, Azure som drivs av 21Vianet i Kina eller en privat Azure-installation.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-150">The Azure service endpoint determines whether your application is managed by the global Azure platform, Azure operated by 21Vianet in China, or a private Azure installation.</span></span>

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

### <span data-ttu-id="c9d2b-151">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="c9d2b-151">-SqlDatabaseDnsSuffix</span></span>
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

### <span data-ttu-id="c9d2b-152">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9d2b-152">-StorageEndpoint</span></span>
<span data-ttu-id="c9d2b-153">Ändrar standard slut punkten för lagrings tjänster i den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-153">Changes the default endpoint of storage services in the specified environment.</span></span>

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

### <span data-ttu-id="c9d2b-154">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="c9d2b-154">-TrafficManagerDnsSuffix</span></span>
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

### <span data-ttu-id="c9d2b-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d2b-155">CommonParameters</span></span>
<span data-ttu-id="c9d2b-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d2b-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9d2b-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d2b-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c9d2b-158">INPUTS</span></span>

### <span data-ttu-id="c9d2b-159">Ingen</span><span class="sxs-lookup"><span data-stu-id="c9d2b-159">None</span></span>
<span data-ttu-id="c9d2b-160">Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="c9d2b-160">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="c9d2b-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c9d2b-161">OUTPUTS</span></span>

### <span data-ttu-id="c9d2b-162">Microsoft. WindowsAzure. commands. Utilitiess. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="c9d2b-162">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>

## <span data-ttu-id="c9d2b-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c9d2b-163">NOTES</span></span>

## <span data-ttu-id="c9d2b-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c9d2b-164">RELATED LINKS</span></span>

[<span data-ttu-id="c9d2b-165">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="c9d2b-165">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="c9d2b-166">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="c9d2b-166">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="c9d2b-167">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="c9d2b-167">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)


