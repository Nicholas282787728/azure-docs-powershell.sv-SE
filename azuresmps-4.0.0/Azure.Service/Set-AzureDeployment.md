---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7F51F534-6C64-4983-A08F-4732A39C2E7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c62f3d29b4cd2c87fd5606ca013eb03958fb62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099294"
---
# <span data-ttu-id="e620e-101">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="e620e-101">Set-AzureDeployment</span></span>

## <span data-ttu-id="e620e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e620e-102">SYNOPSIS</span></span>
<span data-ttu-id="e620e-103">Ändrar status, konfigurations inställningar eller uppgraderings läge för en distribution.</span><span class="sxs-lookup"><span data-stu-id="e620e-103">Modifies the status, configuration settings, or upgrade mode of a deployment.</span></span>

## <span data-ttu-id="e620e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e620e-104">SYNTAX</span></span>

### <span data-ttu-id="e620e-105">Grader</span><span class="sxs-lookup"><span data-stu-id="e620e-105">Upgrade</span></span>
```
Set-AzureDeployment [-Upgrade] [-ServiceName] <String> [-Package] <String> [-Configuration] <String>
 [-Slot] <String> [[-Mode] <String>] [[-Label] <String>] [[-RoleName] <String>] [-Force]
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e620e-106">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="e620e-106">Config</span></span>
```
Set-AzureDeployment [-Config] [-ServiceName] <String> [-Configuration] <String> [-Slot] <String>
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e620e-107">Status</span><span class="sxs-lookup"><span data-stu-id="e620e-107">Status</span></span>
```
Set-AzureDeployment [-Status] [-ServiceName] <String> [-Slot] <String> [-NewStatus] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="e620e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e620e-108">DESCRIPTION</span></span>
<span data-ttu-id="e620e-109">Cmdleten **set-AzureDeployment** ändrar status, konfigurations inställningar eller uppgraderings läge för en Azure-distribution.</span><span class="sxs-lookup"><span data-stu-id="e620e-109">The **Set-AzureDeployment** cmdlet modifies the status, configuration settings, or upgrade mode of an Azure deployment.</span></span>
<span data-ttu-id="e620e-110">Du kan ändra status för distributionen till antingen igång eller inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="e620e-110">You can change the status of the deployment to either Running or Suspended.</span></span>
<span data-ttu-id="e620e-111">Du kan ändra. cscfg-filen för distributionen.</span><span class="sxs-lookup"><span data-stu-id="e620e-111">You can change the .cscfg file for the deployment.</span></span>
<span data-ttu-id="e620e-112">Du kan ställa in uppgraderings läget och uppdatera konfigurationsfilerna.</span><span class="sxs-lookup"><span data-stu-id="e620e-112">You can set the upgrade mode and update configuration files.</span></span>
<span data-ttu-id="e620e-113">Använd cmdleten **set-AzureWalkUpgradeDomain** för att starta en uppgradering.</span><span class="sxs-lookup"><span data-stu-id="e620e-113">Use the **Set-AzureWalkUpgradeDomain** cmdlet to initiate an upgrade.</span></span>

## <span data-ttu-id="e620e-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e620e-114">EXAMPLES</span></span>

### <span data-ttu-id="e620e-115">Exempel 1: ändra status för en distribution</span><span class="sxs-lookup"><span data-stu-id="e620e-115">Example 1: Change the status of a deployment</span></span>
```
PS C:\> Set-AzureDeployment -Status -ServiceName "ContosoService" -Slot "Production" -NewStatus "Running"
```

<span data-ttu-id="e620e-116">Det här kommandot anger statusen för distributionen för tjänsten som heter ContosoService i produktions miljön för att köra.</span><span class="sxs-lookup"><span data-stu-id="e620e-116">This command sets the status of the deployment for the service named ContosoService in the production environment to Running.</span></span>

### <span data-ttu-id="e620e-117">Exempel 2: tilldela en annan konfigurations fil till en distribution</span><span class="sxs-lookup"><span data-stu-id="e620e-117">Example 2: Assign a different configuration file to a deployment</span></span>
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Slot "Staging" -Configuration "C:\Temp\MyServiceConfig.Cloud.csfg"
```

<span data-ttu-id="e620e-118">Det här kommandot tilldelar en annan konfigurations fil för distributionen för tjänsten som heter ContosoService i utvecklings miljön.</span><span class="sxs-lookup"><span data-stu-id="e620e-118">This command assigns a different configuration file for the deployment for the service named ContosoService in the staging environment.</span></span>

### <span data-ttu-id="e620e-119">Exempel 3: Ange uppgraderings läget till Auto</span><span class="sxs-lookup"><span data-stu-id="e620e-119">Example 3: Set the upgrade mode to Auto</span></span>
```
PS C:\> Set-AzureDeployment -Upgrade -ServiceName "ContosoService" -Mode Auto -Package "C:\packages\ContosoApp.cspkg" -Configuration "C:\Config\ContosoServiceConfig.Cloud.csfg"
```

<span data-ttu-id="e620e-120">Det här kommandot anger uppgraderings läget till Auto och anger ett uppgraderings paket och en ny konfigurations fil.</span><span class="sxs-lookup"><span data-stu-id="e620e-120">This command sets the upgrade mode to Auto, and specifies an upgrade package and a new configuration file.</span></span>

### <span data-ttu-id="e620e-121">Exempel 4: installera tilläggs konfiguration i en tjänst</span><span class="sxs-lookup"><span data-stu-id="e620e-121">Example 4: Install extension configuration in a service</span></span>
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Mode "Automatic" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Slot "Production" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

<span data-ttu-id="e620e-122">Det här kommandot installerar konfigurations tillägget i den angivna moln tjänsten och tillämpar dem på roller.</span><span class="sxs-lookup"><span data-stu-id="e620e-122">This command installs the extension configuration in the specified Cloud Service and applies them on roles.</span></span>

## <span data-ttu-id="e620e-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e620e-123">PARAMETERS</span></span>

### <span data-ttu-id="e620e-124">-Config</span><span class="sxs-lookup"><span data-stu-id="e620e-124">-Config</span></span>
<span data-ttu-id="e620e-125">Anger att den här cmdleten ändrar konfigurationen för distributionen.</span><span class="sxs-lookup"><span data-stu-id="e620e-125">Specifies that this cmdlet modifies the configuration of the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Config
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e620e-126">-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="e620e-126">-Configuration</span></span>
<span data-ttu-id="e620e-127">Anger den fullständiga sökvägen till en. cscfg-konfigurationsfil.</span><span class="sxs-lookup"><span data-stu-id="e620e-127">Specifies the full path of a .cscfg configuration file.</span></span>
<span data-ttu-id="e620e-128">Du kan ange en konfigurations fil för en uppgradering eller konfigurations ändring.</span><span class="sxs-lookup"><span data-stu-id="e620e-128">You can specify a configuration file for an upgrade or configuration change.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade, Config
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e620e-129">-ExtensionConfiguration</span><span class="sxs-lookup"><span data-stu-id="e620e-129">-ExtensionConfiguration</span></span>
<span data-ttu-id="e620e-130">Anger en matris med tilläggs konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="e620e-130">Specifies an array of extension configuration objects.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: Upgrade, Config
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e620e-131">-Force</span><span class="sxs-lookup"><span data-stu-id="e620e-131">-Force</span></span>
<span data-ttu-id="e620e-132">Anger att cmdleten utför en framtvingad uppgradering.</span><span class="sxs-lookup"><span data-stu-id="e620e-132">Indicates that cmdlet performs a forced upgrade.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e620e-133">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e620e-133">-InformationAction</span></span>
<span data-ttu-id="e620e-134">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="e620e-134">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e620e-135">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e620e-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e620e-136">Vidare</span><span class="sxs-lookup"><span data-stu-id="e620e-136">Continue</span></span>
- <span data-ttu-id="e620e-137">Över</span><span class="sxs-lookup"><span data-stu-id="e620e-137">Ignore</span></span>
- <span data-ttu-id="e620e-138">Inquire</span><span class="sxs-lookup"><span data-stu-id="e620e-138">Inquire</span></span>
- <span data-ttu-id="e620e-139">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e620e-139">SilentlyContinue</span></span>
- <span data-ttu-id="e620e-140">Stanna</span><span class="sxs-lookup"><span data-stu-id="e620e-140">Stop</span></span>
- <span data-ttu-id="e620e-141">Avbryt</span><span class="sxs-lookup"><span data-stu-id="e620e-141">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e620e-142">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e620e-142">-InformationVariable</span></span>
<span data-ttu-id="e620e-143">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="e620e-143">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e620e-144">-Etikett</span><span class="sxs-lookup"><span data-stu-id="e620e-144">-Label</span></span>
<span data-ttu-id="e620e-145">Anger en etikett för den uppgraderade distributionen.</span><span class="sxs-lookup"><span data-stu-id="e620e-145">Specifies a label for the upgraded deployment.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e620e-146">-Mode</span><span class="sxs-lookup"><span data-stu-id="e620e-146">-Mode</span></span>
<span data-ttu-id="e620e-147">Anger uppgraderings läget.</span><span class="sxs-lookup"><span data-stu-id="e620e-147">Specifies the mode of upgrade.</span></span>
<span data-ttu-id="e620e-148">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="e620e-148">Valid values are:</span></span> 

- <span data-ttu-id="e620e-149">Pass</span><span class="sxs-lookup"><span data-stu-id="e620e-149">Auto</span></span> 
- <span data-ttu-id="e620e-150">Manövrer</span><span class="sxs-lookup"><span data-stu-id="e620e-150">Manual</span></span> 
- <span data-ttu-id="e620e-151">Upphäv</span><span class="sxs-lookup"><span data-stu-id="e620e-151">Simultaneous</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e620e-152">-NewStatus</span><span class="sxs-lookup"><span data-stu-id="e620e-152">-NewStatus</span></span>
<span data-ttu-id="e620e-153">Anger distributionens mål status.</span><span class="sxs-lookup"><span data-stu-id="e620e-153">Specifies the target status for the deployment.</span></span>
<span data-ttu-id="e620e-154">Giltiga värden är: igång och inaktiverade.</span><span class="sxs-lookup"><span data-stu-id="e620e-154">Valid values are: Running and Suspended.</span></span>

```yaml
Type: String
Parameter Sets: Status
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e620e-155">-Paketera</span><span class="sxs-lookup"><span data-stu-id="e620e-155">-Package</span></span>
<span data-ttu-id="e620e-156">Anger den fullständiga sökvägen till en uppgraderings paket fil.</span><span class="sxs-lookup"><span data-stu-id="e620e-156">Specifies the full path of an upgrade package file.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e620e-157">-Profil</span><span class="sxs-lookup"><span data-stu-id="e620e-157">-Profile</span></span>
<span data-ttu-id="e620e-158">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e620e-158">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e620e-159">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e620e-159">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e620e-160">-RoleName</span><span class="sxs-lookup"><span data-stu-id="e620e-160">-RoleName</span></span>
<span data-ttu-id="e620e-161">Anger namnet på den roll som ska uppgraderas.</span><span class="sxs-lookup"><span data-stu-id="e620e-161">Specifies the name of the role to upgrade.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e620e-162">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e620e-162">-ServiceName</span></span>
<span data-ttu-id="e620e-163">Anger namnet på Azure-tjänsten för distributionen.</span><span class="sxs-lookup"><span data-stu-id="e620e-163">Specifies the name of the Azure service of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e620e-164">-Plats</span><span class="sxs-lookup"><span data-stu-id="e620e-164">-Slot</span></span>
<span data-ttu-id="e620e-165">Anger miljön för distributionen som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="e620e-165">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="e620e-166">Giltiga värden är: produktion och mellanlagring.</span><span class="sxs-lookup"><span data-stu-id="e620e-166">Valid values are: Production and Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e620e-167">-Status</span><span class="sxs-lookup"><span data-stu-id="e620e-167">-Status</span></span>
<span data-ttu-id="e620e-168">Anger att denna cmdlet ändrar distributionens status.</span><span class="sxs-lookup"><span data-stu-id="e620e-168">Specifies that this cmdlet changes the status of the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Status
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e620e-169">-Uppgradera</span><span class="sxs-lookup"><span data-stu-id="e620e-169">-Upgrade</span></span>
<span data-ttu-id="e620e-170">Anger att denna cmdlet uppgraderar distributionen.</span><span class="sxs-lookup"><span data-stu-id="e620e-170">Specifies that this cmdlet upgrades the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e620e-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e620e-171">CommonParameters</span></span>
<span data-ttu-id="e620e-172">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e620e-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e620e-173">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e620e-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e620e-174">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e620e-174">INPUTS</span></span>

## <span data-ttu-id="e620e-175">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e620e-175">OUTPUTS</span></span>

## <span data-ttu-id="e620e-176">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e620e-176">NOTES</span></span>

## <span data-ttu-id="e620e-177">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e620e-177">RELATED LINKS</span></span>

[<span data-ttu-id="e620e-178">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="e620e-178">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="e620e-179">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="e620e-179">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="e620e-180">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="e620e-180">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="e620e-181">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="e620e-181">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="e620e-182">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="e620e-182">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="e620e-183">Set-AzureWalkUpgradeDomain</span><span class="sxs-lookup"><span data-stu-id="e620e-183">Set-AzureWalkUpgradeDomain</span></span>](./Set-AzureWalkUpgradeDomain.md)


