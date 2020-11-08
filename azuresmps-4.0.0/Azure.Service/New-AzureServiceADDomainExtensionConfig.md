---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: DFD4BA63-A7DE-49DD-878C-68062EF17873
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4d4830d049ab01142c75847b4afd5419729f14d1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099127"
---
# <span data-ttu-id="b4d6e-101">New-AzureServiceADDomainExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="b4d6e-101">New-AzureServiceADDomainExtensionConfig</span></span>

## <span data-ttu-id="b4d6e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4d6e-102">SYNOPSIS</span></span>
<span data-ttu-id="b4d6e-103">Genererar konfigurationen för AD-domännamnet för moln tjänster.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-103">Generates the configuration for the AD domain extension for cloud services.</span></span>

## <span data-ttu-id="b4d6e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4d6e-104">SYNTAX</span></span>

### <span data-ttu-id="b4d6e-105">JoinDomainUsingEnumOptions (standard)</span><span class="sxs-lookup"><span data-stu-id="b4d6e-105">JoinDomainUsingEnumOptions (Default)</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>] [[-OUPath] <String>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b4d6e-106">JoinDomainUsingJoinOption</span><span class="sxs-lookup"><span data-stu-id="b4d6e-106">JoinDomainUsingJoinOption</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32> [[-OUPath] <String>] [[-Version] <String>]
 [[-ExtensionId] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b4d6e-107">WorkGroupName</span><span class="sxs-lookup"><span data-stu-id="b4d6e-107">WorkGroupName</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b4d6e-108">JoinDomainUsingEnumOptionsAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="b4d6e-108">JoinDomainUsingEnumOptionsAndThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>] [[-OUPath] <String>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b4d6e-109">JoinDomainUsingJoinOptionAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="b4d6e-109">JoinDomainUsingJoinOptionAndThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32> [[-OUPath] <String>] [[-Version] <String>]
 [[-ExtensionId] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b4d6e-110">WorkGroupNameThumbprint</span><span class="sxs-lookup"><span data-stu-id="b4d6e-110">WorkGroupNameThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b4d6e-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4d6e-111">DESCRIPTION</span></span>
<span data-ttu-id="b4d6e-112">Cmdleten **New-AzureServiceADDomainExtensionConfig** skapar konfigurationen för Active Directory (AD)-domän tillägget för moln tjänster.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-112">The **New-AzureServiceADDomainExtensionConfig** cmdlet generates the configuration for the Active Directory (AD) domain extension for cloud services.</span></span>

## <span data-ttu-id="b4d6e-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4d6e-113">EXAMPLES</span></span>

### <span data-ttu-id="b4d6e-114">Exempel 1: Ange en AD-domän-konfiguration</span><span class="sxs-lookup"><span data-stu-id="b4d6e-114">Example 1: Specify an AD domain configuration</span></span>
```
PS C:\> $ExtensionCfg = New-AzureServiceADDomainExtensionConfig -Role WorkerRole1 -DomainName $Domain -Credential $Cred -JoinOption 35;

PS C:\> New-AzureDeployment -ServiceName $CloudSvc -Slot "Production" -Package $Pkg -Configuration $Config -ExtensionConfiguration $ExtensionCfg;
```

<span data-ttu-id="b4d6e-115">Det här kommandot genererar en konfiguration för annons domän tillägget.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-115">This command generates a configuration for the AD domain extension.</span></span>

## <span data-ttu-id="b4d6e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4d6e-116">PARAMETERS</span></span>

### <span data-ttu-id="b4d6e-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="b4d6e-117">-CertificateThumbprint</span></span>
<span data-ttu-id="b4d6e-118">Anger ett certifikat-tumavtryck som ska användas för att kryptera den privata konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-118">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="b4d6e-119">Det här certifikatet måste redan finnas i certifikat arkivet.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-119">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="b4d6e-120">Om du inte anger ett certifikat skapar den här cmdleten ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-120">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4d6e-121">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="b4d6e-121">-Credential</span></span>
<span data-ttu-id="b4d6e-122">Anger de autentiseringsuppgifter som ska användas för att ansluta till AD-domänen.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-122">Specifies the credentials to use to join the AD domain.</span></span>
<span data-ttu-id="b4d6e-123">Uppgifterna inkluderar ett användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-123">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4d6e-124">-Domän namn</span><span class="sxs-lookup"><span data-stu-id="b4d6e-124">-DomainName</span></span>
<span data-ttu-id="b4d6e-125">Anger namnet på AD-domänen.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-125">Specifies the AD domain name.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4d6e-126">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="b4d6e-126">-ExtensionId</span></span>
<span data-ttu-id="b4d6e-127">Anger tilläggs-ID.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-127">Specifies the extension ID.</span></span>

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

### <span data-ttu-id="b4d6e-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b4d6e-128">-InformationAction</span></span>
<span data-ttu-id="b4d6e-129">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b4d6e-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b4d6e-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b4d6e-131">Vidare</span><span class="sxs-lookup"><span data-stu-id="b4d6e-131">Continue</span></span>
- <span data-ttu-id="b4d6e-132">Över</span><span class="sxs-lookup"><span data-stu-id="b4d6e-132">Ignore</span></span>
- <span data-ttu-id="b4d6e-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="b4d6e-133">Inquire</span></span>
- <span data-ttu-id="b4d6e-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b4d6e-134">SilentlyContinue</span></span>
- <span data-ttu-id="b4d6e-135">Stanna</span><span class="sxs-lookup"><span data-stu-id="b4d6e-135">Stop</span></span>
- <span data-ttu-id="b4d6e-136">Avbryt</span><span class="sxs-lookup"><span data-stu-id="b4d6e-136">Suspend</span></span>

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

### <span data-ttu-id="b4d6e-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b4d6e-137">-InformationVariable</span></span>
<span data-ttu-id="b4d6e-138">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b4d6e-139">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="b4d6e-139">-JoinOption</span></span>
<span data-ttu-id="b4d6e-140">Anger alternativet för att delta i kopplingen.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-140">Specifies the join option enumeration.</span></span>

```yaml
Type: UInt32
Parameter Sets: JoinDomainUsingJoinOption, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4d6e-141">-Alternativ</span><span class="sxs-lookup"><span data-stu-id="b4d6e-141">-Options</span></span>
<span data-ttu-id="b4d6e-142">Anger alternativet för att koppla osignerat heltal.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-142">Specifies the unsigned integer join option.</span></span>

```yaml
Type: JoinOptions
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingEnumOptionsAndThumbprint
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4d6e-143">-OUPath</span><span class="sxs-lookup"><span data-stu-id="b4d6e-143">-OUPath</span></span>
<span data-ttu-id="b4d6e-144">Anger organisations enhets vägen (OU) för AD Domain Join-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-144">Specifies the organization unit (OU) path for AD domain join operation.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4d6e-145">-Profil</span><span class="sxs-lookup"><span data-stu-id="b4d6e-145">-Profile</span></span>
<span data-ttu-id="b4d6e-146">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-146">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b4d6e-147">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-147">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b4d6e-148">-Starta om</span><span class="sxs-lookup"><span data-stu-id="b4d6e-148">-Restart</span></span>
<span data-ttu-id="b4d6e-149">Anger om datorn ska startas om när Join-åtgärden lyckas.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-149">Specifies whether to restart the computer if the join operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4d6e-150">-Roll</span><span class="sxs-lookup"><span data-stu-id="b4d6e-150">-Role</span></span>
<span data-ttu-id="b4d6e-151">Anger en valfri uppsättning roller för att ange konfigurationen för fjärr skrivbord för AD Domain-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-151">Specifies an optional array of roles to specify the remote desktop configuration for the AD domain configuration.</span></span>
<span data-ttu-id="b4d6e-152">Om du inte anger den här parametern används AD-klientkonfiguration som standard konfiguration för alla roller.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-152">If you do not specify this parameter, the AD domain configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="b4d6e-153">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="b4d6e-153">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="b4d6e-154">Anger en algoritm för tumavtryck som används med tumavtrycket för att identifiera certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-154">Specifies a thumbprint hashing algorithm that is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="b4d6e-155">Den här parametern är valfri och standardvärdet är SHA1.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-155">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4d6e-156">-UnjoinDomainCredential</span><span class="sxs-lookup"><span data-stu-id="b4d6e-156">-UnjoinDomainCredential</span></span>
<span data-ttu-id="b4d6e-157">Anger autentiseringsuppgifterna (användar namn och lösen ord) för att koppla från AD-domänen.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-157">Specifies the credentials (user name and password) to unjoin the AD domain.</span></span>

```yaml
Type: PSCredential
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4d6e-158">-Version</span><span class="sxs-lookup"><span data-stu-id="b4d6e-158">-Version</span></span>
<span data-ttu-id="b4d6e-159">Anger tilläggs versionen.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-159">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4d6e-160">-WorkgroupName</span><span class="sxs-lookup"><span data-stu-id="b4d6e-160">-WorkgroupName</span></span>
<span data-ttu-id="b4d6e-161">Anger namnet på arbets gruppen.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-161">Specifies the workgroup name.</span></span>

```yaml
Type: String
Parameter Sets: WorkGroupName, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4d6e-162">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="b4d6e-162">-X509Certificate</span></span>
<span data-ttu-id="b4d6e-163">Anger ett X. 509-certifikat som automatiskt laddas upp till moln tjänsten och används för att kryptera den privata konfigurationen för tillägget.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-163">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, WorkGroupName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4d6e-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4d6e-164">CommonParameters</span></span>
<span data-ttu-id="b4d6e-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4d6e-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4d6e-166">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4d6e-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4d6e-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4d6e-167">INPUTS</span></span>

## <span data-ttu-id="b4d6e-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4d6e-168">OUTPUTS</span></span>

## <span data-ttu-id="b4d6e-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4d6e-169">NOTES</span></span>

## <span data-ttu-id="b4d6e-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4d6e-170">RELATED LINKS</span></span>

[<span data-ttu-id="b4d6e-171">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="b4d6e-171">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="b4d6e-172">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="b4d6e-172">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


