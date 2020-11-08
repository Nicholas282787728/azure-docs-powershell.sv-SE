---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E27283AF-4057-48D9-9F08-7D36290DD907
online version: ''
schema: 2.0.0
ms.openlocfilehash: dfe55fb2ced2275eae06e96480249acd99d3ad6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099126"
---
# <span data-ttu-id="53b86-101">New-AzureServiceExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="53b86-101">New-AzureServiceExtensionConfig</span></span>

## <span data-ttu-id="53b86-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53b86-102">SYNOPSIS</span></span>
<span data-ttu-id="53b86-103">Skapar en konfiguration för moln tjänst tillägg för en distribution.</span><span class="sxs-lookup"><span data-stu-id="53b86-103">Creates a cloud service extension configuration for a deployment.</span></span>

## <span data-ttu-id="53b86-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53b86-104">SYNTAX</span></span>

### <span data-ttu-id="53b86-105">NewExtension (standard)</span><span class="sxs-lookup"><span data-stu-id="53b86-105">NewExtension (Default)</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String> [-ProviderNamespace] <String>
 [-PublicConfiguration] <String> [-PrivateConfiguration] <String> [-Version] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="53b86-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="53b86-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String> [-ProviderNamespace] <String>
 [-PublicConfiguration] <String> [-PrivateConfiguration] <String> [-Version] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="53b86-107">UpdateExtensionStatusParameterSetName</span><span class="sxs-lookup"><span data-stu-id="53b86-107">UpdateExtensionStatusParameterSetName</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [-ExtensionId] <String> [-ExtensionState] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="53b86-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53b86-108">DESCRIPTION</span></span>
<span data-ttu-id="53b86-109">Cmdleten **New-AzureServiceExtensionConfig** skapar en konfiguration för moln tjänst tillägg för distribution.</span><span class="sxs-lookup"><span data-stu-id="53b86-109">The **New-AzureServiceExtensionConfig** cmdlet creates a cloud service extension configuration for a deployment.</span></span>

## <span data-ttu-id="53b86-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53b86-110">EXAMPLES</span></span>

### <span data-ttu-id="53b86-111">Exempel 1: skapa en tilläggs konfiguration</span><span class="sxs-lookup"><span data-stu-id="53b86-111">Example 1: Create an extension configuration</span></span>
```
PS C:\> New-AzureServiceExtensionConfig -ExtensionName 'RDP' -Version '1.0' -ProviderNamespace Microsoft.Windows.Azure.Extensions -PublicConfiguration $p1 -PrivateConfiguration $p2;
```

<span data-ttu-id="53b86-112">Det här kommandot anger en tilläggs konfiguration.</span><span class="sxs-lookup"><span data-stu-id="53b86-112">This command specifies an extension configuration.</span></span>

### <span data-ttu-id="53b86-113">Exempel 2: skapa en tilläggs konfiguration för en roll</span><span class="sxs-lookup"><span data-stu-id="53b86-113">Example 2: Create an extension configuration for a role</span></span>
```
PS C:\> New-AzureServiceExtensionConfig -Role WebRole1 -ExtensionName 'RDP' -ProviderNamespace Microsoft.Windows.Azure.Extensions -PublicConfiguration $p1 -PrivateConfiguration $p2;
```

<span data-ttu-id="53b86-114">Det här kommandot anger en tilläggs konfiguration för rollen WebRole1.</span><span class="sxs-lookup"><span data-stu-id="53b86-114">This command specifies an extension configuration for the role WebRole1.</span></span>

## <span data-ttu-id="53b86-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53b86-115">PARAMETERS</span></span>

### <span data-ttu-id="53b86-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="53b86-116">-CertificateThumbprint</span></span>
<span data-ttu-id="53b86-117">Anger ett certifikat-tumavtryck som ska användas för att kryptera den privata konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="53b86-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="53b86-118">Det här certifikatet måste redan finnas i certifikat arkivet.</span><span class="sxs-lookup"><span data-stu-id="53b86-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="53b86-119">Om du inte anger ett certifikat skapar den här cmdleten ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="53b86-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="53b86-120">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="53b86-120">-ExtensionId</span></span>
<span data-ttu-id="53b86-121">Anger namnet på tillägget.</span><span class="sxs-lookup"><span data-stu-id="53b86-121">Specifies the name of the extension.</span></span>

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

```yaml
Type: String
Parameter Sets: UpdateExtensionStatusParameterSetName
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53b86-122">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="53b86-122">-ExtensionName</span></span>
<span data-ttu-id="53b86-123">Anger namnet på tillägget.</span><span class="sxs-lookup"><span data-stu-id="53b86-123">Specifies the name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53b86-124">-ExtensionState</span><span class="sxs-lookup"><span data-stu-id="53b86-124">-ExtensionState</span></span>
<span data-ttu-id="53b86-125">Anger tillståndet för tillägget.</span><span class="sxs-lookup"><span data-stu-id="53b86-125">Specifies the state of the extension.</span></span>
<span data-ttu-id="53b86-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="53b86-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="53b86-127">Aktivering</span><span class="sxs-lookup"><span data-stu-id="53b86-127">Enable</span></span> 
- <span data-ttu-id="53b86-128">Aktiverar</span><span class="sxs-lookup"><span data-stu-id="53b86-128">Disable</span></span> 
- <span data-ttu-id="53b86-129">Avinstallera</span><span class="sxs-lookup"><span data-stu-id="53b86-129">Uninstall</span></span>

```yaml
Type: String
Parameter Sets: UpdateExtensionStatusParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53b86-130">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="53b86-130">-InformationAction</span></span>
<span data-ttu-id="53b86-131">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="53b86-131">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="53b86-132">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="53b86-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="53b86-133">Vidare</span><span class="sxs-lookup"><span data-stu-id="53b86-133">Continue</span></span>
- <span data-ttu-id="53b86-134">Över</span><span class="sxs-lookup"><span data-stu-id="53b86-134">Ignore</span></span>
- <span data-ttu-id="53b86-135">Inquire</span><span class="sxs-lookup"><span data-stu-id="53b86-135">Inquire</span></span>
- <span data-ttu-id="53b86-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="53b86-136">SilentlyContinue</span></span>
- <span data-ttu-id="53b86-137">Stanna</span><span class="sxs-lookup"><span data-stu-id="53b86-137">Stop</span></span>
- <span data-ttu-id="53b86-138">Avbryt</span><span class="sxs-lookup"><span data-stu-id="53b86-138">Suspend</span></span>

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

### <span data-ttu-id="53b86-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="53b86-139">-InformationVariable</span></span>
<span data-ttu-id="53b86-140">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="53b86-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="53b86-141">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="53b86-141">-PrivateConfiguration</span></span>
<span data-ttu-id="53b86-142">Anger den privata konfigurations texten.</span><span class="sxs-lookup"><span data-stu-id="53b86-142">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53b86-143">-Profil</span><span class="sxs-lookup"><span data-stu-id="53b86-143">-Profile</span></span>
<span data-ttu-id="53b86-144">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="53b86-144">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="53b86-145">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="53b86-145">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="53b86-146">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="53b86-146">-ProviderNamespace</span></span>
<span data-ttu-id="53b86-147">Anger tillägget leverantörens namn område.</span><span class="sxs-lookup"><span data-stu-id="53b86-147">Specifies the Extension's Provider Namespace.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53b86-148">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="53b86-148">-PublicConfiguration</span></span>
<span data-ttu-id="53b86-149">Anger den allmänna konfigurations texten.</span><span class="sxs-lookup"><span data-stu-id="53b86-149">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53b86-150">-Roll</span><span class="sxs-lookup"><span data-stu-id="53b86-150">-Role</span></span>
<span data-ttu-id="53b86-151">Anger en valfri uppsättning roller för att ange fjärr skrivbords konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="53b86-151">Specifies an optional array of roles to specify the remote desktop configuration for.</span></span>
<span data-ttu-id="53b86-152">Om du inte anger konfigurationen för fjärr skrivbord används som standard konfiguration för alla roller.</span><span class="sxs-lookup"><span data-stu-id="53b86-152">If not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53b86-153">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="53b86-153">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="53b86-154">Anger en algoritm för tumavtryck som används tillsammans med tumavtrycket för att identifiera certifikatet.</span><span class="sxs-lookup"><span data-stu-id="53b86-154">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="53b86-155">Den här parametern är valfri och standardvärdet är SHA1.</span><span class="sxs-lookup"><span data-stu-id="53b86-155">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="53b86-156">-Version</span><span class="sxs-lookup"><span data-stu-id="53b86-156">-Version</span></span>
<span data-ttu-id="53b86-157">Anger tilläggs versionen.</span><span class="sxs-lookup"><span data-stu-id="53b86-157">Specifies the extension version.</span></span>

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

### <span data-ttu-id="53b86-158">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="53b86-158">-X509Certificate</span></span>
<span data-ttu-id="53b86-159">Anger ett x509-certifikat som ska laddas automatiskt till moln tjänsten och användas för att kryptera den privata konfigurationen för tillägget.</span><span class="sxs-lookup"><span data-stu-id="53b86-159">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="53b86-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53b86-160">CommonParameters</span></span>
<span data-ttu-id="53b86-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53b86-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53b86-162">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53b86-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53b86-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53b86-163">INPUTS</span></span>

## <span data-ttu-id="53b86-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53b86-164">OUTPUTS</span></span>

## <span data-ttu-id="53b86-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53b86-165">NOTES</span></span>

## <span data-ttu-id="53b86-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53b86-166">RELATED LINKS</span></span>

[<span data-ttu-id="53b86-167">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="53b86-167">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="53b86-168">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="53b86-168">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


