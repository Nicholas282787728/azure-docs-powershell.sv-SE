---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2E738CEF-BBDD-425D-B12C-86FF7C45A634
online version: ''
schema: 2.0.0
ms.openlocfilehash: 518528d4af8889cf36b30c417e0170e0ea228ebf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099277"
---
# <span data-ttu-id="e7c04-101">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e7c04-101">Set-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="e7c04-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e7c04-102">SYNOPSIS</span></span>
<span data-ttu-id="e7c04-103">Aktiverar Azure Diagnostics-tillägget för angivna roller eller alla roller på en distribuerad tjänst eller vid distribution.</span><span class="sxs-lookup"><span data-stu-id="e7c04-103">Enables Azure Diagnostics extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="e7c04-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e7c04-104">SYNTAX</span></span>

### <span data-ttu-id="e7c04-105">SetExtension (standard)</span><span class="sxs-lookup"><span data-stu-id="e7c04-105">SetExtension (Default)</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-Version] <String>] [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7c04-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="e7c04-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-CertificateThumbprint] <String>] [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-Version] <String>] [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7c04-107">SetExtensionUsingDiagnosticsConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7c04-107">SetExtensionUsingDiagnosticsConfiguration</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>]
 [-DiagnosticsConfiguration] <ExtensionConfigurationInput[]> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e7c04-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e7c04-108">DESCRIPTION</span></span>
<span data-ttu-id="e7c04-109">Cmdleten **set-AzureServiceDiagnosticsExtension** aktiverar Azure Diagnostics-tillägget för angivna roller eller alla roller på en distribuerad tjänst eller vid distribution.</span><span class="sxs-lookup"><span data-stu-id="e7c04-109">The **Set-AzureServiceDiagnosticsExtension** cmdlet enables Azure Diagnostics extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="e7c04-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e7c04-110">EXAMPLES</span></span>

### <span data-ttu-id="e7c04-111">Exempel 1: Aktivera Azure Diagnostics-tillägget</span><span class="sxs-lookup"><span data-stu-id="e7c04-111">Example 1: Enable Azure Diagnostics extension</span></span>
```
PS C:\> Set-AzureServiceDiagnosticsExtension -ServiceName $Svc -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML
```

<span data-ttu-id="e7c04-112">Med det här kommandot aktive ras Azure Diagnostics-tillägget för alla roller.</span><span class="sxs-lookup"><span data-stu-id="e7c04-112">This command enables the Azure Diagnostics extension for all roles.</span></span>

### <span data-ttu-id="e7c04-113">Exempel 2: Aktivera Azure Diagnostics-tillägget för en viss roll</span><span class="sxs-lookup"><span data-stu-id="e7c04-113">Example 2: Enable Azure Diagnostics extension for a specified role</span></span>
```
PS C:\> Set-AzureServiceDiagnosticsExtension -ServiceName $Svc -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML -Role "WebRole01"
```

<span data-ttu-id="e7c04-114">Det här kommandot aktiverar Azure Diagnostics-tillägget för en viss roll.</span><span class="sxs-lookup"><span data-stu-id="e7c04-114">This command enables the Azure Diagnostics extension for a specified role.</span></span>

## <span data-ttu-id="e7c04-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e7c04-115">PARAMETERS</span></span>

### <span data-ttu-id="e7c04-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="e7c04-116">-CertificateThumbprint</span></span>
<span data-ttu-id="e7c04-117">Anger ett certifikat-tumavtryck som ska användas för att kryptera den privata konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="e7c04-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="e7c04-118">Det här certifikatet måste redan finnas i certifikat arkivet.</span><span class="sxs-lookup"><span data-stu-id="e7c04-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="e7c04-119">Om du inte anger ett certifikat skapar den här cmdleten ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="e7c04-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c04-120">-DiagnosticsConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7c04-120">-DiagnosticsConfiguration</span></span>
<span data-ttu-id="e7c04-121">Anger en konfigurations mat ris för Azure Diagnostics.</span><span class="sxs-lookup"><span data-stu-id="e7c04-121">Specifies an array of configuration for Azure Diagnostics.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: SetExtensionUsingDiagnosticsConfiguration
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c04-122">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="e7c04-122">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="e7c04-123">Anger konfiguration för Azure Diagnostics.</span><span class="sxs-lookup"><span data-stu-id="e7c04-123">Specifies the configuration for Azure Diagnostics.</span></span>
<span data-ttu-id="e7c04-124">Du kan ladda ned schemat genom att använda följande kommando:</span><span class="sxs-lookup"><span data-stu-id="e7c04-124">You can download the schema by using the following command:</span></span> 

`(Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics').PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'`

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c04-125">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="e7c04-125">-ExtensionId</span></span>
<span data-ttu-id="e7c04-126">Anger tilläggs-ID</span><span class="sxs-lookup"><span data-stu-id="e7c04-126">Specifies the extension ID</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c04-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e7c04-127">-InformationAction</span></span>
<span data-ttu-id="e7c04-128">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="e7c04-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e7c04-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e7c04-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e7c04-130">Vidare</span><span class="sxs-lookup"><span data-stu-id="e7c04-130">Continue</span></span>
- <span data-ttu-id="e7c04-131">Över</span><span class="sxs-lookup"><span data-stu-id="e7c04-131">Ignore</span></span>
- <span data-ttu-id="e7c04-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="e7c04-132">Inquire</span></span>
- <span data-ttu-id="e7c04-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e7c04-133">SilentlyContinue</span></span>
- <span data-ttu-id="e7c04-134">Stanna</span><span class="sxs-lookup"><span data-stu-id="e7c04-134">Stop</span></span>
- <span data-ttu-id="e7c04-135">Avbryt</span><span class="sxs-lookup"><span data-stu-id="e7c04-135">Suspend</span></span>

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

### <span data-ttu-id="e7c04-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e7c04-136">-InformationVariable</span></span>
<span data-ttu-id="e7c04-137">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="e7c04-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e7c04-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="e7c04-138">-Profile</span></span>
<span data-ttu-id="e7c04-139">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e7c04-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e7c04-140">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e7c04-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e7c04-141">-Roll</span><span class="sxs-lookup"><span data-stu-id="e7c04-141">-Role</span></span>
<span data-ttu-id="e7c04-142">Anger en valfri matris med roller som du kan använda för att ange Azure Diagnostics-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e7c04-142">Specifies an optional array of roles for which to specify the Azure Diagnostics configuration.</span></span>
<span data-ttu-id="e7c04-143">Om du inte anger den här parametern används diagnostikverktyget som standard konfiguration för alla roller.</span><span class="sxs-lookup"><span data-stu-id="e7c04-143">If you do not specify this parameter, the diagnostics configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c04-144">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e7c04-144">-ServiceName</span></span>
<span data-ttu-id="e7c04-145">Anger namnet på distributionen av Azure-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e7c04-145">Specifies the Azure service name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c04-146">-Plats</span><span class="sxs-lookup"><span data-stu-id="e7c04-146">-Slot</span></span>
<span data-ttu-id="e7c04-147">Anger miljön för distributionen som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="e7c04-147">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="e7c04-148">De acceptabla värdena för denna parameter är: produktion eller mellanlagring.</span><span class="sxs-lookup"><span data-stu-id="e7c04-148">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c04-149">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7c04-149">-StorageAccountEndpoint</span></span>
<span data-ttu-id="e7c04-150">Anger en slut punkt för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="e7c04-150">Specifies a storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c04-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e7c04-151">-StorageAccountKey</span></span>
<span data-ttu-id="e7c04-152">Anger en lagrings konto profil.</span><span class="sxs-lookup"><span data-stu-id="e7c04-152">Specifies a storage account key.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c04-153">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e7c04-153">-StorageAccountName</span></span>
<span data-ttu-id="e7c04-154">Anger ett lagrings konto namn.</span><span class="sxs-lookup"><span data-stu-id="e7c04-154">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c04-155">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="e7c04-155">-StorageContext</span></span>
<span data-ttu-id="e7c04-156">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="e7c04-156">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c04-157">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e7c04-157">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="e7c04-158">Anger en algoritm för tumavtryck som används med tumavtrycket för att identifiera certifikatet.</span><span class="sxs-lookup"><span data-stu-id="e7c04-158">Specifies a thumbprint hashing algorithm that is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="e7c04-159">Den här parametern är valfri och standardvärdet är SHA1.</span><span class="sxs-lookup"><span data-stu-id="e7c04-159">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c04-160">-Version</span><span class="sxs-lookup"><span data-stu-id="e7c04-160">-Version</span></span>
<span data-ttu-id="e7c04-161">Anger version för tillägget.</span><span class="sxs-lookup"><span data-stu-id="e7c04-161">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c04-162">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="e7c04-162">-X509Certificate</span></span>
<span data-ttu-id="e7c04-163">Anger ett X. 509-certifikat som när det anges automatiskt laddas upp till moln tjänsten och används för att kryptera den privata konfigurationen för tillägget.</span><span class="sxs-lookup"><span data-stu-id="e7c04-163">Specifies an X.509 certificate that, when specified, is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: SetExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c04-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7c04-164">CommonParameters</span></span>
<span data-ttu-id="e7c04-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7c04-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7c04-166">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7c04-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7c04-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e7c04-167">INPUTS</span></span>

## <span data-ttu-id="e7c04-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e7c04-168">OUTPUTS</span></span>

## <span data-ttu-id="e7c04-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e7c04-169">NOTES</span></span>

## <span data-ttu-id="e7c04-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e7c04-170">RELATED LINKS</span></span>

[<span data-ttu-id="e7c04-171">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e7c04-171">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="e7c04-172">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e7c04-172">Remove-AzureServiceDiagnosticsExtension</span></span>](./Remove-AzureServiceDiagnosticsExtension.md)


