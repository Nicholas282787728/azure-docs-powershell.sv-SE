---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 350638E1-636E-484B-88EB-91F48129D80B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c665288d12897e4ab7277dd4ccf4bc5d975c037
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099278"
---
# <span data-ttu-id="89b90-101">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="89b90-101">Set-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="89b90-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="89b90-102">SYNOPSIS</span></span>
<span data-ttu-id="89b90-103">Aktiverar ett AD-domännätverk för en moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="89b90-103">Enables an AD Domain extension for a cloud service.</span></span>

## <span data-ttu-id="89b90-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="89b90-104">SYNTAX</span></span>

### <span data-ttu-id="89b90-105">JoinDomainUsingEnumOptions (standard)</span><span class="sxs-lookup"><span data-stu-id="89b90-105">JoinDomainUsingEnumOptions (Default)</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>]
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="89b90-106">JoinDomainUsingJoinOption</span><span class="sxs-lookup"><span data-stu-id="89b90-106">JoinDomainUsingJoinOption</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32>
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="89b90-107">WorkGroupName</span><span class="sxs-lookup"><span data-stu-id="89b90-107">WorkGroupName</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="89b90-108">JoinDomainUsingEnumOptionsAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="89b90-108">JoinDomainUsingEnumOptionsAndThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>]
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="89b90-109">JoinDomainUsingJoinOptionAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="89b90-109">JoinDomainUsingJoinOptionAndThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32>
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="89b90-110">WorkGroupNameThumbprint</span><span class="sxs-lookup"><span data-stu-id="89b90-110">WorkGroupNameThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="89b90-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="89b90-111">DESCRIPTION</span></span>
<span data-ttu-id="89b90-112">Cmdleten **set-AzureServiceADDomainExtension** aktiverar en AD-ändelse (Active Directory) för en moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="89b90-112">The **Set-AzureServiceADDomainExtension** cmdlet enables an AD (Active Directory) Domain extension for a cloud service.</span></span>

## <span data-ttu-id="89b90-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="89b90-113">EXAMPLES</span></span>

### <span data-ttu-id="89b90-114">9.1</span><span class="sxs-lookup"><span data-stu-id="89b90-114">1:</span></span>
```

```

## <span data-ttu-id="89b90-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="89b90-115">PARAMETERS</span></span>

### <span data-ttu-id="89b90-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="89b90-116">-CertificateThumbprint</span></span>
<span data-ttu-id="89b90-117">Anger ett certifikat-tumavtryck som ska användas för att kryptera den privata konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="89b90-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="89b90-118">Det här certifikatet måste redan finnas i certifikat arkivet.</span><span class="sxs-lookup"><span data-stu-id="89b90-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="89b90-119">Om du inte anger ett certifikat skapar den här cmdleten ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="89b90-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89b90-120">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="89b90-120">-Credential</span></span>
<span data-ttu-id="89b90-121">Anger autentiseringsuppgifter för att ansluta till AD-domänen.</span><span class="sxs-lookup"><span data-stu-id="89b90-121">Specifies the credentials to join the AD domain.</span></span>
<span data-ttu-id="89b90-122">Uppgifterna inkluderar ett användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="89b90-122">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89b90-123">-Domän namn</span><span class="sxs-lookup"><span data-stu-id="89b90-123">-DomainName</span></span>
<span data-ttu-id="89b90-124">Anger namnet på AD-domänen.</span><span class="sxs-lookup"><span data-stu-id="89b90-124">Specifies the AD domain name.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89b90-125">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="89b90-125">-ExtensionId</span></span>
<span data-ttu-id="89b90-126">Anger tilläggs-ID.</span><span class="sxs-lookup"><span data-stu-id="89b90-126">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89b90-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="89b90-127">-InformationAction</span></span>
<span data-ttu-id="89b90-128">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="89b90-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="89b90-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="89b90-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="89b90-130">Vidare</span><span class="sxs-lookup"><span data-stu-id="89b90-130">Continue</span></span>
- <span data-ttu-id="89b90-131">Över</span><span class="sxs-lookup"><span data-stu-id="89b90-131">Ignore</span></span>
- <span data-ttu-id="89b90-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="89b90-132">Inquire</span></span>
- <span data-ttu-id="89b90-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="89b90-133">SilentlyContinue</span></span>
- <span data-ttu-id="89b90-134">Stanna</span><span class="sxs-lookup"><span data-stu-id="89b90-134">Stop</span></span>
- <span data-ttu-id="89b90-135">Avbryt</span><span class="sxs-lookup"><span data-stu-id="89b90-135">Suspend</span></span>

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

### <span data-ttu-id="89b90-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="89b90-136">-InformationVariable</span></span>
<span data-ttu-id="89b90-137">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="89b90-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="89b90-138">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="89b90-138">-JoinOption</span></span>
<span data-ttu-id="89b90-139">Anger alternativet för att delta i kopplingen.</span><span class="sxs-lookup"><span data-stu-id="89b90-139">Specifies the join option enumeration.</span></span>

```yaml
Type: UInt32
Parameter Sets: JoinDomainUsingJoinOption, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89b90-140">-Alternativ</span><span class="sxs-lookup"><span data-stu-id="89b90-140">-Options</span></span>
<span data-ttu-id="89b90-141">Anger alternativet för att koppla osignerat heltal.</span><span class="sxs-lookup"><span data-stu-id="89b90-141">Specifies the unsigned integer join option.</span></span>

```yaml
Type: JoinOptions
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingEnumOptionsAndThumbprint
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89b90-142">-OUPath</span><span class="sxs-lookup"><span data-stu-id="89b90-142">-OUPath</span></span>
<span data-ttu-id="89b90-143">Anger organisationsenhetens sökväg (OU) för AD Domain Join-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="89b90-143">Specifies the Organization Unit (OU) path for the AD domain join operation.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89b90-144">-Profil</span><span class="sxs-lookup"><span data-stu-id="89b90-144">-Profile</span></span>
<span data-ttu-id="89b90-145">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="89b90-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="89b90-146">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="89b90-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="89b90-147">-Starta om</span><span class="sxs-lookup"><span data-stu-id="89b90-147">-Restart</span></span>
<span data-ttu-id="89b90-148">Anger om datorn ska startas om när Join-åtgärden lyckas.</span><span class="sxs-lookup"><span data-stu-id="89b90-148">Specifies whether to restart the computer if the join operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89b90-149">-Roll</span><span class="sxs-lookup"><span data-stu-id="89b90-149">-Role</span></span>
<span data-ttu-id="89b90-150">Anger en valfri matris med roller som du kan ange fjärr skrivbords konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="89b90-150">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="89b90-151">Om du inte anger konfiguration för AD-domän används den som standard konfiguration för alla roller.</span><span class="sxs-lookup"><span data-stu-id="89b90-151">If not specified the AD domain configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="89b90-152">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="89b90-152">-ServiceName</span></span>
<span data-ttu-id="89b90-153">Anger moln tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="89b90-153">Specifies the cloud service name.</span></span>

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

### <span data-ttu-id="89b90-154">-Plats</span><span class="sxs-lookup"><span data-stu-id="89b90-154">-Slot</span></span>
<span data-ttu-id="89b90-155">Anger miljön för distributionen som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="89b90-155">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="89b90-156">De acceptabla värdena för denna parameter är: produktion eller mellanlagring.</span><span class="sxs-lookup"><span data-stu-id="89b90-156">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="89b90-157">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="89b90-157">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="89b90-158">Anger en algoritm för tumavtryck som används tillsammans med tumavtrycket för att identifiera certifikatet.</span><span class="sxs-lookup"><span data-stu-id="89b90-158">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="89b90-159">Den här parametern är valfri och standardvärdet är SHA1.</span><span class="sxs-lookup"><span data-stu-id="89b90-159">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="89b90-160">-UnjoinDomainCredential</span><span class="sxs-lookup"><span data-stu-id="89b90-160">-UnjoinDomainCredential</span></span>
<span data-ttu-id="89b90-161">Anger autentiseringsuppgifterna (användar namn och lösen ord) för att koppla från AD-domänen.</span><span class="sxs-lookup"><span data-stu-id="89b90-161">Specifies the credentials (user name and password) to unjoin the AD domain.</span></span>

```yaml
Type: PSCredential
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89b90-162">-Version</span><span class="sxs-lookup"><span data-stu-id="89b90-162">-Version</span></span>
<span data-ttu-id="89b90-163">Anger tilläggs versionen.</span><span class="sxs-lookup"><span data-stu-id="89b90-163">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89b90-164">-WorkgroupName</span><span class="sxs-lookup"><span data-stu-id="89b90-164">-WorkgroupName</span></span>
<span data-ttu-id="89b90-165">Anger namnet på arbets gruppen.</span><span class="sxs-lookup"><span data-stu-id="89b90-165">Specifies the workgroup name.</span></span>

```yaml
Type: String
Parameter Sets: WorkGroupName, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89b90-166">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="89b90-166">-X509Certificate</span></span>
<span data-ttu-id="89b90-167">Anger ett x509-certifikat som ska laddas automatiskt till moln tjänsten och användas för att kryptera den privata konfigurationen för tillägget.</span><span class="sxs-lookup"><span data-stu-id="89b90-167">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, WorkGroupName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89b90-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89b90-168">CommonParameters</span></span>
<span data-ttu-id="89b90-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89b90-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89b90-170">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89b90-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89b90-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="89b90-171">INPUTS</span></span>

## <span data-ttu-id="89b90-172">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="89b90-172">OUTPUTS</span></span>

## <span data-ttu-id="89b90-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="89b90-173">NOTES</span></span>

## <span data-ttu-id="89b90-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="89b90-174">RELATED LINKS</span></span>

[<span data-ttu-id="89b90-175">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="89b90-175">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="89b90-176">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="89b90-176">Remove-AzureServiceADDomainExtension</span></span>](./Remove-AzureServiceADDomainExtension.md)

[<span data-ttu-id="89b90-177">New-AzureServiceADDomainExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="89b90-177">New-AzureServiceADDomainExtensionConfig</span></span>](./New-AzureServiceADDomainExtensionConfig.md)


