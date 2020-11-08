---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2BDB255A-EFB3-4580-BE95-187008DB208C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21195f6d3ed938844717789f8a0df16f49fbd85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099159"
---
# <span data-ttu-id="f83ea-101">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="f83ea-101">New-AzureDeployment</span></span>

## <span data-ttu-id="f83ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f83ea-102">SYNOPSIS</span></span>
<span data-ttu-id="f83ea-103">Skapar en distribution från en tjänst.</span><span class="sxs-lookup"><span data-stu-id="f83ea-103">Creates a deployment from a service.</span></span>

## <span data-ttu-id="f83ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f83ea-104">SYNTAX</span></span>

```
New-AzureDeployment [-ServiceName] <String> [-Package] <String> [-Configuration] <String> [-Slot] <String>
 [[-Label] <String>] [[-Name] <String>] [-DoNotStart] [-TreatWarningsAsError]
 [-ExtensionConfiguration <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f83ea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f83ea-105">DESCRIPTION</span></span>
<span data-ttu-id="f83ea-106">Cmdleten **New-AzureDeployment** skapar en Azure-distribution från en tjänst som omfattar webb roller och arbets roller.</span><span class="sxs-lookup"><span data-stu-id="f83ea-106">The **New-AzureDeployment** cmdlet creates an Azure deployment from a service that comprises web roles and worker roles.</span></span>
<span data-ttu-id="f83ea-107">Denna cmdlet skapar en distribution baserad på en paketfil (. cspkg) och en tjänst konfigurations fil (. cscfg).</span><span class="sxs-lookup"><span data-stu-id="f83ea-107">This cmdlet creates a deployment based on a package file (.cspkg) and a service configuration file (.cscfg).</span></span>
<span data-ttu-id="f83ea-108">Ange ett namn som är unikt i distributions miljö.</span><span class="sxs-lookup"><span data-stu-id="f83ea-108">Specify a name that is unique within deployment environment.</span></span>

<span data-ttu-id="f83ea-109">Använd cmdleten **New-AzureVM** för att skapa en distribution som baseras på virtuella Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="f83ea-109">Use the **New-AzureVM** cmdlet to create a deployment based on Azure virtual machines.</span></span>

## <span data-ttu-id="f83ea-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f83ea-110">EXAMPLES</span></span>

### <span data-ttu-id="f83ea-111">Exempel 1: skapa en distribution</span><span class="sxs-lookup"><span data-stu-id="f83ea-111">Example 1: Create a deployment</span></span>
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Label "ContosoDeployment"
```

<span data-ttu-id="f83ea-112">Det här kommandot skapar en produktions distribution baserat på ett paket med namnet ContosoPackage. cspkg och en konfiguration med namnet ContosoConfiguration. cscfg.</span><span class="sxs-lookup"><span data-stu-id="f83ea-112">This command creates a production deployment based on a package named ContosoPackage.cspkg and a configuration named ContosoConfiguration.cscfg.</span></span>
<span data-ttu-id="f83ea-113">Kommandot anger en etikett för distributionen.</span><span class="sxs-lookup"><span data-stu-id="f83ea-113">The command specifies a label for the deployment.</span></span>
<span data-ttu-id="f83ea-114">Inget namn anges.</span><span class="sxs-lookup"><span data-stu-id="f83ea-114">It does not specify a name.</span></span>
<span data-ttu-id="f83ea-115">Denna cmdlet skapar ett GUID som namn.</span><span class="sxs-lookup"><span data-stu-id="f83ea-115">This cmdlet creates a GUID as the name.</span></span>

### <span data-ttu-id="f83ea-116">Exempel 2: skapa en distribution utifrån en tilläggs konfiguration</span><span class="sxs-lookup"><span data-stu-id="f83ea-116">Example 2: Create a deployment based on an extension configuration</span></span>
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

<span data-ttu-id="f83ea-117">Det här kommandot skapar en produktions distribution baserat på ett paket och en konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f83ea-117">This command creates a production deployment based on a package and configuration.</span></span>
<span data-ttu-id="f83ea-118">Kommandot anger en tilläggs konfiguration som heter ContosoExtensionConfig. cscfg.</span><span class="sxs-lookup"><span data-stu-id="f83ea-118">The command specifies an extension configuration named ContosoExtensionConfig.cscfg.</span></span>
<span data-ttu-id="f83ea-119">Denna cmdlet skapar GUID-namn och etikett.</span><span class="sxs-lookup"><span data-stu-id="f83ea-119">This cmdlet creates GUIDs as the name and the label.</span></span>

## <span data-ttu-id="f83ea-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f83ea-120">PARAMETERS</span></span>

### <span data-ttu-id="f83ea-121">-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="f83ea-121">-Configuration</span></span>
<span data-ttu-id="f83ea-122">Anger den fullständiga sökvägen till en tjänst konfigurations fil.</span><span class="sxs-lookup"><span data-stu-id="f83ea-122">Specifies the full path of a service configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83ea-123">-DoNotStart</span><span class="sxs-lookup"><span data-stu-id="f83ea-123">-DoNotStart</span></span>
<span data-ttu-id="f83ea-124">Anger att det inte går att starta distributionen med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f83ea-124">Specifies that this cmdlet does not start the deployment.</span></span>

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

### <span data-ttu-id="f83ea-125">-ExtensionConfiguration</span><span class="sxs-lookup"><span data-stu-id="f83ea-125">-ExtensionConfiguration</span></span>
<span data-ttu-id="f83ea-126">Anger en matris med tilläggs konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="f83ea-126">Specifies an array of extension configuration objects.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f83ea-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f83ea-127">-InformationAction</span></span>
<span data-ttu-id="f83ea-128">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="f83ea-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f83ea-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f83ea-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f83ea-130">Vidare</span><span class="sxs-lookup"><span data-stu-id="f83ea-130">Continue</span></span>
- <span data-ttu-id="f83ea-131">Över</span><span class="sxs-lookup"><span data-stu-id="f83ea-131">Ignore</span></span>
- <span data-ttu-id="f83ea-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="f83ea-132">Inquire</span></span>
- <span data-ttu-id="f83ea-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f83ea-133">SilentlyContinue</span></span>
- <span data-ttu-id="f83ea-134">Stanna</span><span class="sxs-lookup"><span data-stu-id="f83ea-134">Stop</span></span>
- <span data-ttu-id="f83ea-135">Avbryt</span><span class="sxs-lookup"><span data-stu-id="f83ea-135">Suspend</span></span>

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

### <span data-ttu-id="f83ea-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f83ea-136">-InformationVariable</span></span>
<span data-ttu-id="f83ea-137">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="f83ea-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f83ea-138">-Etikett</span><span class="sxs-lookup"><span data-stu-id="f83ea-138">-Label</span></span>
<span data-ttu-id="f83ea-139">Anger ett etikett namn för distributionen.</span><span class="sxs-lookup"><span data-stu-id="f83ea-139">Specifies a label name for the deployment.</span></span>
<span data-ttu-id="f83ea-140">Om du inte anger en etikett använder denna cmdlet en GUID.</span><span class="sxs-lookup"><span data-stu-id="f83ea-140">If you do not specify a label, this cmdlet uses a GUID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83ea-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="f83ea-141">-Name</span></span>
<span data-ttu-id="f83ea-142">Anger ett distributions namn.</span><span class="sxs-lookup"><span data-stu-id="f83ea-142">Specifies a deployment name.</span></span>
<span data-ttu-id="f83ea-143">Om du inte anger ett namn använder denna cmdlet en GUID.</span><span class="sxs-lookup"><span data-stu-id="f83ea-143">If you do not specify a name, this cmdlet uses a GUID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83ea-144">-Paketera</span><span class="sxs-lookup"><span data-stu-id="f83ea-144">-Package</span></span>
<span data-ttu-id="f83ea-145">Anger sökväg eller URI för en. cspkg-fil i lagrings utrymmet inom samma prenumeration eller projekt.</span><span class="sxs-lookup"><span data-stu-id="f83ea-145">Specifies the path or URI of a .cspkg file in storage within the same subscription or project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83ea-146">-Profil</span><span class="sxs-lookup"><span data-stu-id="f83ea-146">-Profile</span></span>
<span data-ttu-id="f83ea-147">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f83ea-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f83ea-148">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="f83ea-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f83ea-149">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f83ea-149">-ServiceName</span></span>
<span data-ttu-id="f83ea-150">Anger namnet på Azure-tjänsten för distributionen.</span><span class="sxs-lookup"><span data-stu-id="f83ea-150">Specifies the name of the Azure service for the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f83ea-151">-Plats</span><span class="sxs-lookup"><span data-stu-id="f83ea-151">-Slot</span></span>
<span data-ttu-id="f83ea-152">Anger miljön där den här cmdleten skapar distributionen.</span><span class="sxs-lookup"><span data-stu-id="f83ea-152">Specifies the environment where this cmdlet creates the deployment.</span></span>
<span data-ttu-id="f83ea-153">Giltiga värden är: för produktion och produktion.</span><span class="sxs-lookup"><span data-stu-id="f83ea-153">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="f83ea-154">Standardvärdet är produktion.</span><span class="sxs-lookup"><span data-stu-id="f83ea-154">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f83ea-155">-TreatWarningsAsError</span><span class="sxs-lookup"><span data-stu-id="f83ea-155">-TreatWarningsAsError</span></span>
<span data-ttu-id="f83ea-156">Anger att varnings meddelanden är fel.</span><span class="sxs-lookup"><span data-stu-id="f83ea-156">Specifies that warning messages are errors.</span></span>
<span data-ttu-id="f83ea-157">Om du anger den här parametern kommer ett varnings meddelande att fungera.</span><span class="sxs-lookup"><span data-stu-id="f83ea-157">If you specify this parameter, a warning message causes the deployment to fail.</span></span>

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

### <span data-ttu-id="f83ea-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f83ea-158">CommonParameters</span></span>
<span data-ttu-id="f83ea-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f83ea-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f83ea-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f83ea-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f83ea-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f83ea-161">INPUTS</span></span>

## <span data-ttu-id="f83ea-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f83ea-162">OUTPUTS</span></span>

## <span data-ttu-id="f83ea-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f83ea-163">NOTES</span></span>

## <span data-ttu-id="f83ea-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f83ea-164">RELATED LINKS</span></span>

[<span data-ttu-id="f83ea-165">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="f83ea-165">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="f83ea-166">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="f83ea-166">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="f83ea-167">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="f83ea-167">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="f83ea-168">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f83ea-168">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="f83ea-169">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="f83ea-169">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="f83ea-170">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="f83ea-170">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


