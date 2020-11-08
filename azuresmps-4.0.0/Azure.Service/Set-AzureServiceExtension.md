---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D37920D3-AF6C-4CFC-B9A3-8ED931AEC0DC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 318683c26d05c624549363ff1afe4a2b963c1fe6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093173"
---
# <span data-ttu-id="4f93b-101">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="4f93b-101">Set-AzureServiceExtension</span></span>

## <span data-ttu-id="4f93b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f93b-102">SYNOPSIS</span></span>
<span data-ttu-id="4f93b-103">Lägger till ett moln tjänst tillägg i en distribution.</span><span class="sxs-lookup"><span data-stu-id="4f93b-103">Adds a cloud service extension to a deployment.</span></span>

## <span data-ttu-id="4f93b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f93b-104">SYNTAX</span></span>

### <span data-ttu-id="4f93b-105">SetExtension (standard)</span><span class="sxs-lookup"><span data-stu-id="4f93b-105">SetExtension (Default)</span></span>
```
Set-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-PublicConfiguration] <String> [-PrivateConfiguration] <String>
 [-Version] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4f93b-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="4f93b-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-PublicConfiguration] <String> [-PrivateConfiguration] <String>
 [-Version] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4f93b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f93b-107">DESCRIPTION</span></span>
<span data-ttu-id="4f93b-108">Cmdleten **set-AzureServiceExtension** lägger till en moln tjänst anknytning till en distribution.</span><span class="sxs-lookup"><span data-stu-id="4f93b-108">The **Set-AzureServiceExtension** cmdlet adds a cloud service extension to a deployment.</span></span>

## <span data-ttu-id="4f93b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f93b-109">EXAMPLES</span></span>

### <span data-ttu-id="4f93b-110">Exempel 1: lägga till en moln tjänst till en distribution</span><span class="sxs-lookup"><span data-stu-id="4f93b-110">Example 1: Add a cloud service to a deployment</span></span>
```
PS C:\> Set-AzureServiceExtension -Service $Svc -Slot "Production" -ExtensionName "RDP" -Version "1.0" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -PublicConfiguration $P1 -PrivateConfiguration $P2;
```

<span data-ttu-id="4f93b-111">Det här kommandot lägger till en moln tjänst till en distribution.</span><span class="sxs-lookup"><span data-stu-id="4f93b-111">This command adds a cloud service to a deployment.</span></span>

### <span data-ttu-id="4f93b-112">Exempel 2: lägga till en moln tjänst till en distribution för en viss roll</span><span class="sxs-lookup"><span data-stu-id="4f93b-112">Example 2: Add a cloud service to a deployment for a specified role</span></span>
```
PS C:\> Set-AzureServiceExtension -Service $Svc -Slot "Production" -Role "WebRole1" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -PublicConfiguration $P1 -PrivateConfiguration $P2;
```

<span data-ttu-id="4f93b-113">Det här kommandot lägger till en moln tjänst till en distribution för en viss roll.</span><span class="sxs-lookup"><span data-stu-id="4f93b-113">This command adds a cloud service to a deployment for a specified role.</span></span>

## <span data-ttu-id="4f93b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f93b-114">PARAMETERS</span></span>

### <span data-ttu-id="4f93b-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="4f93b-115">-CertificateThumbprint</span></span>
<span data-ttu-id="4f93b-116">Anger ett certifikat-tumavtryck som ska användas för att kryptera den privata konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="4f93b-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="4f93b-117">Det här certifikatet måste redan finnas i certifikat arkivet.</span><span class="sxs-lookup"><span data-stu-id="4f93b-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="4f93b-118">Om du inte anger ett certifikat skapar den här cmdleten ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="4f93b-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f93b-119">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="4f93b-119">-ExtensionId</span></span>
<span data-ttu-id="4f93b-120">Anger tilläggs-ID.</span><span class="sxs-lookup"><span data-stu-id="4f93b-120">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f93b-121">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="4f93b-121">-ExtensionName</span></span>
<span data-ttu-id="4f93b-122">Anger tillägget.</span><span class="sxs-lookup"><span data-stu-id="4f93b-122">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f93b-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4f93b-123">-InformationAction</span></span>
<span data-ttu-id="4f93b-124">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="4f93b-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4f93b-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4f93b-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4f93b-126">Vidare</span><span class="sxs-lookup"><span data-stu-id="4f93b-126">Continue</span></span>
- <span data-ttu-id="4f93b-127">Över</span><span class="sxs-lookup"><span data-stu-id="4f93b-127">Ignore</span></span>
- <span data-ttu-id="4f93b-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="4f93b-128">Inquire</span></span>
- <span data-ttu-id="4f93b-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4f93b-129">SilentlyContinue</span></span>
- <span data-ttu-id="4f93b-130">Stanna</span><span class="sxs-lookup"><span data-stu-id="4f93b-130">Stop</span></span>
- <span data-ttu-id="4f93b-131">Avbryt</span><span class="sxs-lookup"><span data-stu-id="4f93b-131">Suspend</span></span>

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

### <span data-ttu-id="4f93b-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4f93b-132">-InformationVariable</span></span>
<span data-ttu-id="4f93b-133">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="4f93b-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4f93b-134">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f93b-134">-PrivateConfiguration</span></span>
<span data-ttu-id="4f93b-135">Anger den privata konfigurations texten.</span><span class="sxs-lookup"><span data-stu-id="4f93b-135">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f93b-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="4f93b-136">-Profile</span></span>
<span data-ttu-id="4f93b-137">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="4f93b-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4f93b-138">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="4f93b-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4f93b-139">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="4f93b-139">-ProviderNamespace</span></span>
<span data-ttu-id="4f93b-140">Anger namn området för tilläggs leverantör.</span><span class="sxs-lookup"><span data-stu-id="4f93b-140">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f93b-141">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f93b-141">-PublicConfiguration</span></span>
<span data-ttu-id="4f93b-142">Anger den allmänna konfigurations texten.</span><span class="sxs-lookup"><span data-stu-id="4f93b-142">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f93b-143">-Roll</span><span class="sxs-lookup"><span data-stu-id="4f93b-143">-Role</span></span>
<span data-ttu-id="4f93b-144">Anger en valfri matris med roller som du kan ange fjärr skrivbords konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="4f93b-144">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="4f93b-145">Om den här parametern inte anges används fjärr skrivbords konfigurationen som standard konfiguration för alla roller.</span><span class="sxs-lookup"><span data-stu-id="4f93b-145">If this parameter is not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f93b-146">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4f93b-146">-ServiceName</span></span>
<span data-ttu-id="4f93b-147">Anger namnet på distributionen av Azure-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4f93b-147">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="4f93b-148">-Plats</span><span class="sxs-lookup"><span data-stu-id="4f93b-148">-Slot</span></span>
<span data-ttu-id="4f93b-149">Anger miljön för distributionen som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="4f93b-149">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="4f93b-150">Giltiga värden är: produktion eller mellanlagring.</span><span class="sxs-lookup"><span data-stu-id="4f93b-150">Valid values are: Production or Staging.</span></span>

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

### <span data-ttu-id="4f93b-151">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="4f93b-151">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="4f93b-152">Anger den tumavtryck för hash-algoritm som används med tumavtrycket för att identifiera certifikatet.</span><span class="sxs-lookup"><span data-stu-id="4f93b-152">Specifies the thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="4f93b-153">Den här parametern är valfri och standardvärdet är SHA1.</span><span class="sxs-lookup"><span data-stu-id="4f93b-153">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f93b-154">-Version</span><span class="sxs-lookup"><span data-stu-id="4f93b-154">-Version</span></span>
<span data-ttu-id="4f93b-155">Anger tilläggs versionen.</span><span class="sxs-lookup"><span data-stu-id="4f93b-155">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f93b-156">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="4f93b-156">-X509Certificate</span></span>
<span data-ttu-id="4f93b-157">Anger ett X. 509-certifikat som automatiskt laddas upp till moln tjänsten och används för att kryptera den privata konfigurationen för tillägget.</span><span class="sxs-lookup"><span data-stu-id="4f93b-157">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="4f93b-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f93b-158">CommonParameters</span></span>
<span data-ttu-id="4f93b-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f93b-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f93b-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f93b-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f93b-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f93b-161">INPUTS</span></span>

## <span data-ttu-id="4f93b-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f93b-162">OUTPUTS</span></span>

## <span data-ttu-id="4f93b-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f93b-163">NOTES</span></span>

## <span data-ttu-id="4f93b-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f93b-164">RELATED LINKS</span></span>

[<span data-ttu-id="4f93b-165">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="4f93b-165">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="4f93b-166">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="4f93b-166">Remove-AzureServiceExtension</span></span>](./Remove-AzureServiceExtension.md)


