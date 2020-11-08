---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1F76C63E-5289-4F88-9522-3FF4EF732908
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a232ec03da38ea3d527dcd9aa214dbf681bcc6a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099128"
---
# <span data-ttu-id="927d1-101">New-AzureServiceDiagnosticsExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="927d1-101">New-AzureServiceDiagnosticsExtensionConfig</span></span>

## <span data-ttu-id="927d1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="927d1-102">SYNOPSIS</span></span>
<span data-ttu-id="927d1-103">Genererar en konfiguration för en diagnostik-anknytning för angivna roller eller alla roller.</span><span class="sxs-lookup"><span data-stu-id="927d1-103">Generates a configuration for a diagnostics extension for specified role(s) or all roles.</span></span>

## <span data-ttu-id="927d1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="927d1-104">SYNTAX</span></span>

### <span data-ttu-id="927d1-105">NewExtension (standard)</span><span class="sxs-lookup"><span data-stu-id="927d1-105">NewExtension (Default)</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="927d1-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="927d1-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>]
 [[-StorageContext] <AzureStorageContext>] [-DiagnosticsConfigurationPath] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="927d1-107">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="927d1-107">SetExtensionUsingThumbprint</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="927d1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="927d1-108">DESCRIPTION</span></span>
<span data-ttu-id="927d1-109">Cmdleten **New-AzureServiceDiagnosticsExtensionConfig** genererar en konfiguration för en diagnostik-anknytning för angivna roller eller alla roller.</span><span class="sxs-lookup"><span data-stu-id="927d1-109">The **New-AzureServiceDiagnosticsExtensionConfig** cmdlet generates a configuration for a diagnostics extension for specified roles or all roles.</span></span>

## <span data-ttu-id="927d1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="927d1-110">EXAMPLES</span></span>

### <span data-ttu-id="927d1-111">Exempel 1: Skapa Azure Diagnostics-tillägget för alla roller i moln tjänsten</span><span class="sxs-lookup"><span data-stu-id="927d1-111">Example 1: Create the Azure Diagnostics extension for all roles in the cloud service</span></span>
```
PS C:\> $WadConfig = New-AzureServiceDiagnosticExtensionConfig -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML
```

<span data-ttu-id="927d1-112">Det här kommandot skapar Azure Diagnostics-tillägget för alla roller i moln tjänsten.</span><span class="sxs-lookup"><span data-stu-id="927d1-112">This command creates the Azure Diagnostics extension for all of the roles in the cloud service.</span></span>

### <span data-ttu-id="927d1-113">Exempel 2: Skapa Azure Diagnostics-tillägget för en roll</span><span class="sxs-lookup"><span data-stu-id="927d1-113">Example 2: Create the Azure Diagnostics extension for a role</span></span>
```
PS C:\> $WadConfig = New-AzureServiceDiagnosticExtensionConfig -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML -Role "WebRole1"
```

<span data-ttu-id="927d1-114">Det här kommandot skapar Azure Diagnostics-tillägget för rollen WebRole01 i moln tjänsten.</span><span class="sxs-lookup"><span data-stu-id="927d1-114">This command creates the Azure Diagnostics extension for the role WebRole01 in the cloud service.</span></span>

## <span data-ttu-id="927d1-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="927d1-115">PARAMETERS</span></span>

### <span data-ttu-id="927d1-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="927d1-116">-CertificateThumbprint</span></span>
<span data-ttu-id="927d1-117">Anger ett certifikat-tumavtryck som ska användas för att kryptera den privata konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="927d1-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="927d1-118">Det här certifikatet måste redan finnas i certifikat arkivet.</span><span class="sxs-lookup"><span data-stu-id="927d1-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="927d1-119">Om du inte anger ett certifikat skapar den här cmdleten ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="927d1-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="927d1-120">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="927d1-120">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="927d1-121">Anger diagnostisk konfigurations Sök vägen.</span><span class="sxs-lookup"><span data-stu-id="927d1-121">Specifies the diagnostics configuration path.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="927d1-122">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="927d1-122">-ExtensionId</span></span>
<span data-ttu-id="927d1-123">Anger tilläggs-ID.</span><span class="sxs-lookup"><span data-stu-id="927d1-123">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="927d1-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="927d1-124">-InformationAction</span></span>
<span data-ttu-id="927d1-125">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="927d1-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="927d1-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="927d1-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="927d1-127">Vidare</span><span class="sxs-lookup"><span data-stu-id="927d1-127">Continue</span></span>
- <span data-ttu-id="927d1-128">Över</span><span class="sxs-lookup"><span data-stu-id="927d1-128">Ignore</span></span>
- <span data-ttu-id="927d1-129">Inquire</span><span class="sxs-lookup"><span data-stu-id="927d1-129">Inquire</span></span>
- <span data-ttu-id="927d1-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="927d1-130">SilentlyContinue</span></span>
- <span data-ttu-id="927d1-131">Stanna</span><span class="sxs-lookup"><span data-stu-id="927d1-131">Stop</span></span>
- <span data-ttu-id="927d1-132">Avbryt</span><span class="sxs-lookup"><span data-stu-id="927d1-132">Suspend</span></span>

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

### <span data-ttu-id="927d1-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="927d1-133">-InformationVariable</span></span>
<span data-ttu-id="927d1-134">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="927d1-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="927d1-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="927d1-135">-Profile</span></span>
<span data-ttu-id="927d1-136">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="927d1-136">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="927d1-137">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="927d1-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="927d1-138">-Roll</span><span class="sxs-lookup"><span data-stu-id="927d1-138">-Role</span></span>
<span data-ttu-id="927d1-139">Anger en valfri uppsättning roller för att ange diagnostikverktyg för.</span><span class="sxs-lookup"><span data-stu-id="927d1-139">Specifies an optional array of roles to specify the diagnostics configuration for.</span></span>
<span data-ttu-id="927d1-140">Om du inte anger att diagnostikverktyget används som standard konfiguration för alla roller.</span><span class="sxs-lookup"><span data-stu-id="927d1-140">If not specified the diagnostics configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="927d1-141">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="927d1-141">-StorageAccountEndpoint</span></span>
<span data-ttu-id="927d1-142">Anger slut punkt för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="927d1-142">Specifies the storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="927d1-143">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="927d1-143">-StorageAccountKey</span></span>
<span data-ttu-id="927d1-144">Anger lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="927d1-144">Specifies the storage account key.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="927d1-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="927d1-145">-StorageAccountName</span></span>
<span data-ttu-id="927d1-146">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="927d1-146">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="927d1-147">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="927d1-147">-StorageContext</span></span>
<span data-ttu-id="927d1-148">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="927d1-148">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="927d1-149">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="927d1-149">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="927d1-150">Anger en algoritm för tumavtryck som används tillsammans med tumavtrycket för att identifiera certifikatet.</span><span class="sxs-lookup"><span data-stu-id="927d1-150">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="927d1-151">Den här parametern är valfri och standardvärdet är SHA1.</span><span class="sxs-lookup"><span data-stu-id="927d1-151">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="927d1-152">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="927d1-152">-X509Certificate</span></span>
<span data-ttu-id="927d1-153">Anger ett X. 509-certifikat som automatiskt laddas upp till moln tjänsten och används för att kryptera den privata konfigurationen för tillägget.</span><span class="sxs-lookup"><span data-stu-id="927d1-153">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: NewExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="927d1-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="927d1-154">CommonParameters</span></span>
<span data-ttu-id="927d1-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="927d1-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="927d1-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="927d1-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="927d1-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="927d1-157">INPUTS</span></span>

## <span data-ttu-id="927d1-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="927d1-158">OUTPUTS</span></span>

## <span data-ttu-id="927d1-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="927d1-159">NOTES</span></span>

## <span data-ttu-id="927d1-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="927d1-160">RELATED LINKS</span></span>

[<span data-ttu-id="927d1-161">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="927d1-161">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="927d1-162">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="927d1-162">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


