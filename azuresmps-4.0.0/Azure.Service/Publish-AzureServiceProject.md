---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CF7E7C62-88FC-48CA-940F-9A6C7442BEF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8166cd3faa951171dd3ac865b17b8a03bcefdd45
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099113"
---
# <span data-ttu-id="f85b4-101">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="f85b4-101">Publish-AzureServiceProject</span></span>

## <span data-ttu-id="f85b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f85b4-102">SYNOPSIS</span></span>
<span data-ttu-id="f85b4-103">Publicera den aktuella tjänsten till Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="f85b4-103">Publish the current service to Windows Azure.</span></span>

## <span data-ttu-id="f85b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f85b4-104">SYNTAX</span></span>

### <span data-ttu-id="f85b4-105">PublishFromServiceDefinition (standard)</span><span class="sxs-lookup"><span data-stu-id="f85b4-105">PublishFromServiceDefinition (Default)</span></span>
```
Publish-AzureServiceProject [-ServiceName <String>] [-StorageAccountName <String>] [-Location <String>]
 [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>] [-ForceUpgrade]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f85b4-106">PublishFromPackage</span><span class="sxs-lookup"><span data-stu-id="f85b4-106">PublishFromPackage</span></span>
```
Publish-AzureServiceProject [-Package <String>] -Configuration <String> [-StorageAccountName <String>]
 [-Location <String>] [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>]
 [-ForceUpgrade] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f85b4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f85b4-107">DESCRIPTION</span></span>
<span data-ttu-id="f85b4-108">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="f85b4-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f85b4-109">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f85b4-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f85b4-110">Cmdleten **Publishing-AzureServiceProject** publicerar den aktuella tjänsten till molnet.</span><span class="sxs-lookup"><span data-stu-id="f85b4-110">The **Publish-AzureServiceProject** cmdlet publishes the current service to the cloud.</span></span>
<span data-ttu-id="f85b4-111">Du kan ange publicerings konfiguration (till exempel **prenumeration** , **StorageAccountName** , **plats** , **fack** ) på kommando raden eller i lokala inställningar via cmdleten **set-AzureServiceProject** .</span><span class="sxs-lookup"><span data-stu-id="f85b4-111">You can specify publishing configuration (such as **Subscription** , **StorageAccountName** , **Location** , **Slot** ) on the command line, or in local settings through the **Set-AzureServiceProject** cmdlet.</span></span>

## <span data-ttu-id="f85b4-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f85b4-112">EXAMPLES</span></span>

### <span data-ttu-id="f85b4-113">Exempel 1: publicera ett service projekt med standardvärden</span><span class="sxs-lookup"><span data-stu-id="f85b4-113">Example 1: Publish a service project with default values</span></span>
```
PS C:\> Publish-AzureServiceProject
```

<span data-ttu-id="f85b4-114">Det här exemplet publicerar den aktuella tjänsten med de aktuella tjänst inställningarna och den aktuella Azure-publicerings profilen.</span><span class="sxs-lookup"><span data-stu-id="f85b4-114">This example publishes the current service, using the current service settings and the current Azure publish profile.</span></span>

### <span data-ttu-id="f85b4-115">Exempel 2: skapa ett distributions paket</span><span class="sxs-lookup"><span data-stu-id="f85b4-115">Example 2: Create a deployment package</span></span>
```
PS C:\> Publish-AzureServiceProject -PackageOnly
```

<span data-ttu-id="f85b4-116">I det här exemplet skapas en cspkg-fil (...) i tjänst katalogen och publiceras inte till Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="f85b4-116">This example creates a deployment package (.cspkg) file in the service directory and does not publish to Windows Azure.</span></span>

## <span data-ttu-id="f85b4-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f85b4-117">PARAMETERS</span></span>

### <span data-ttu-id="f85b4-118">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="f85b4-118">-AffinityGroup</span></span>
<span data-ttu-id="f85b4-119">Anger den tillhörighets grupp som du vill att tjänsten ska använda.</span><span class="sxs-lookup"><span data-stu-id="f85b4-119">Specifies the affinity group that you want the service to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f85b4-120">-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="f85b4-120">-Configuration</span></span>
<span data-ttu-id="f85b4-121">Anger tjänstens konfigurations fil.</span><span class="sxs-lookup"><span data-stu-id="f85b4-121">Specifies the service configuration file.</span></span>
<span data-ttu-id="f85b4-122">Om du anger den här parametern anger du *paketet* .</span><span class="sxs-lookup"><span data-stu-id="f85b4-122">If you specify this parameter, specify the *Package* parameter.</span></span>

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: cc

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f85b4-123">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="f85b4-123">-DeploymentName</span></span>
<span data-ttu-id="f85b4-124">Anger distributions namnet.</span><span class="sxs-lookup"><span data-stu-id="f85b4-124">Specifies the deployment name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: dn

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f85b4-125">-ForceUpgrade</span><span class="sxs-lookup"><span data-stu-id="f85b4-125">-ForceUpgrade</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: f

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85b4-126">-Lansera</span><span class="sxs-lookup"><span data-stu-id="f85b4-126">-Launch</span></span>
<span data-ttu-id="f85b4-127">Öppnar ett webbläsarfönster så att du kan se programmet när det har distribuerats.</span><span class="sxs-lookup"><span data-stu-id="f85b4-127">Opens a browser window so you can view the application after it is deployed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f85b4-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="f85b4-128">-Location</span></span>
<span data-ttu-id="f85b4-129">Den region där programmet ska hanteras.</span><span class="sxs-lookup"><span data-stu-id="f85b4-129">The region in which the application will be hosted.</span></span>
<span data-ttu-id="f85b4-130">Möjliga värden är:</span><span class="sxs-lookup"><span data-stu-id="f85b4-130">Possible values are:</span></span> 
  
- <span data-ttu-id="f85b4-131">Världen över</span><span class="sxs-lookup"><span data-stu-id="f85b4-131">Anywhere Asia</span></span>
- <span data-ttu-id="f85b4-132">Överallt i Europa</span><span class="sxs-lookup"><span data-stu-id="f85b4-132">Anywhere Europe</span></span>
- <span data-ttu-id="f85b4-133">Var du än är</span><span class="sxs-lookup"><span data-stu-id="f85b4-133">Anywhere US</span></span>
- <span data-ttu-id="f85b4-134">Östasien</span><span class="sxs-lookup"><span data-stu-id="f85b4-134">East Asia</span></span>
- <span data-ttu-id="f85b4-135">Östra USA</span><span class="sxs-lookup"><span data-stu-id="f85b4-135">East US</span></span>
- <span data-ttu-id="f85b4-136">Norra Central USA</span><span class="sxs-lookup"><span data-stu-id="f85b4-136">North Central US</span></span>
- <span data-ttu-id="f85b4-137">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="f85b4-137">North Europe</span></span>
- <span data-ttu-id="f85b4-138">Södra centrala USA</span><span class="sxs-lookup"><span data-stu-id="f85b4-138">South Central US</span></span>
- <span data-ttu-id="f85b4-139">Sydostasien</span><span class="sxs-lookup"><span data-stu-id="f85b4-139">Southeast Asia</span></span>
- <span data-ttu-id="f85b4-140">Västeuropa</span><span class="sxs-lookup"><span data-stu-id="f85b4-140">West Europe</span></span>
- <span data-ttu-id="f85b4-141">Västra USA</span><span class="sxs-lookup"><span data-stu-id="f85b4-141">West US</span></span>
 
<span data-ttu-id="f85b4-142">Om ingen plats anges används platsen i det senaste samtalet till **set-AzureServiceProject** .</span><span class="sxs-lookup"><span data-stu-id="f85b4-142">If no Location is specified, the location specified in the last call to **Set-AzureServiceProject** will be used.</span></span> <span data-ttu-id="f85b4-143">Om du inte har angett någon plats väljs den slumpmässigt från "norra Central amerikanska" och "Syd Central amerikanska" platser.</span><span class="sxs-lookup"><span data-stu-id="f85b4-143">If no Location was ever specified, the Location will be randomly chosen from 'North Central US' and 'South Central US' locations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f85b4-144">-Paketera</span><span class="sxs-lookup"><span data-stu-id="f85b4-144">-Package</span></span>
<span data-ttu-id="f85b4-145">Anger vilken paket fil som ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="f85b4-145">Specifies the package file to deploy.</span></span>
<span data-ttu-id="f85b4-146">Ange antingen en lokal fil som har fil namns tillägget. cspkg eller en URI för en blob som innehåller paketet.</span><span class="sxs-lookup"><span data-stu-id="f85b4-146">Specify either a local file that has the .cspkg file name extension or a URI of a blob that contains the package.</span></span>
<span data-ttu-id="f85b4-147">Om du anger den här parametern ska du inte ange *ServiceName* -parametern.</span><span class="sxs-lookup"><span data-stu-id="f85b4-147">If you specify this parameter, do not specify the *ServiceName* parameter.</span></span>

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: sp

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f85b4-148">-Profil</span><span class="sxs-lookup"><span data-stu-id="f85b4-148">-Profile</span></span>
<span data-ttu-id="f85b4-149">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f85b4-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f85b4-150">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="f85b4-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f85b4-151">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f85b4-151">-ServiceName</span></span>
<span data-ttu-id="f85b4-152">Anger det namn som ska användas för tjänsten när du publicerar till Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="f85b4-152">Specifies the name to be used for the service when publishing to Windows Azure.</span></span>
<span data-ttu-id="f85b4-153">Namnet bestämmer en del av etiketten i cloudapp.net-underdomänen som används för att adressera tjänsten när den hanteras i Windows Azure (det vill säga **namn**. cloudapp.net).</span><span class="sxs-lookup"><span data-stu-id="f85b4-153">The name determines part of the label in the cloudapp.net subdomain that is used to address the service when hosted in Windows Azure (that is, **name**.cloudapp.net).</span></span>
<span data-ttu-id="f85b4-154">Alla namn som anges när tjänsten publiceras åsidosätter namnet som angavs när tjänsten skapades.</span><span class="sxs-lookup"><span data-stu-id="f85b4-154">Any name specified while publishing the service overrides the name given when the service was created.</span></span>
<span data-ttu-id="f85b4-155">(Se cmdleten **New-AzureServiceProject** .</span><span class="sxs-lookup"><span data-stu-id="f85b4-155">(See the **New-AzureServiceProject** cmdlet).</span></span>

```yaml
Type: String
Parameter Sets: PublishFromServiceDefinition
Aliases: sv

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f85b4-156">-Plats</span><span class="sxs-lookup"><span data-stu-id="f85b4-156">-Slot</span></span>
<span data-ttu-id="f85b4-157">Distributions fack för den här tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f85b4-157">The deployment slot to be used for this service.</span></span>
<span data-ttu-id="f85b4-158">Möjliga värden är ' produktion ' och ' produktion '.</span><span class="sxs-lookup"><span data-stu-id="f85b4-158">Possible values are 'Staging' and 'Production'.</span></span>
<span data-ttu-id="f85b4-159">Om du inte anger någon plats används facket i det senaste samtalet till Set-AzureDeploymentSlot.</span><span class="sxs-lookup"><span data-stu-id="f85b4-159">If no slot is specified, the slot provided in the last call to Set-AzureDeploymentSlot is used.</span></span>
<span data-ttu-id="f85b4-160">Om ingen kort plats har angetts används "produktion"-facket.</span><span class="sxs-lookup"><span data-stu-id="f85b4-160">If no slot has ever been specified, the 'Production' slot is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: sl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f85b4-161">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f85b4-161">-StorageAccountName</span></span>
<span data-ttu-id="f85b4-162">Anger namnet på Windows Azure Storage-kontot som ska användas när tjänsten publiceras.</span><span class="sxs-lookup"><span data-stu-id="f85b4-162">Specifies the Windows Azure storage account name to be used while publishing the service.</span></span>
<span data-ttu-id="f85b4-163">Det här värdet används inte förrän tjänsten har publicerats.</span><span class="sxs-lookup"><span data-stu-id="f85b4-163">This value is not used until the service is published.</span></span>
<span data-ttu-id="f85b4-164">När den här parametern inte anges hämtas värdet från det senaste **set-AzureServiceProject-** kommandot.</span><span class="sxs-lookup"><span data-stu-id="f85b4-164">When this parameter is not specified, the value is obtained from the last **Set-AzureServiceProject** command.</span></span>
<span data-ttu-id="f85b4-165">Om inget lagrings konto har angetts används ett lagrings konto som matchar namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f85b4-165">If no storage account was ever specified, a storage account matching the name of the service will be used.</span></span>
<span data-ttu-id="f85b4-166">Om det inte finns något sådant lagrings konto försöker cmdleten skapa ett nytt.</span><span class="sxs-lookup"><span data-stu-id="f85b4-166">If no such storage account exists, the cmdlet attempts to create a new one.</span></span>
<span data-ttu-id="f85b4-167">Men det går inte att pröva om ett lagrings konto som matchar tjänstens namn finns i en annan prenumeration.</span><span class="sxs-lookup"><span data-stu-id="f85b4-167">However, the attempt may fail if a storage account matching the service name exists in another subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: st

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f85b4-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f85b4-168">CommonParameters</span></span>
<span data-ttu-id="f85b4-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f85b4-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f85b4-170">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f85b4-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f85b4-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f85b4-171">INPUTS</span></span>

## <span data-ttu-id="f85b4-172">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f85b4-172">OUTPUTS</span></span>

## <span data-ttu-id="f85b4-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f85b4-173">NOTES</span></span>

## <span data-ttu-id="f85b4-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f85b4-174">RELATED LINKS</span></span>

[<span data-ttu-id="f85b4-175">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="f85b4-175">Enable-AzureServiceProjectRemoteDesktop</span></span>](./Enable-AzureServiceProjectRemoteDesktop.md)

[<span data-ttu-id="f85b4-176">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="f85b4-176">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


