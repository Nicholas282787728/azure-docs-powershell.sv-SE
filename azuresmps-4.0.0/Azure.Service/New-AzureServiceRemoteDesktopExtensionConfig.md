---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2563898E-C4A0-4530-AB46-30A6FC1BE55C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d295e2198cdbd8168d76b1f8e19e75fb4a662116
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099125"
---
# <span data-ttu-id="bf5eb-101">New-AzureServiceRemoteDesktopExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="bf5eb-101">New-AzureServiceRemoteDesktopExtensionConfig</span></span>

## <span data-ttu-id="bf5eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bf5eb-102">SYNOPSIS</span></span>
<span data-ttu-id="bf5eb-103">Genererar en konfiguration för fjärr skrivbords tillägg för en distribution.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-103">Generates a remote desktop extension configuration for a deployment.</span></span>

## <span data-ttu-id="bf5eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bf5eb-104">SYNTAX</span></span>

### <span data-ttu-id="bf5eb-105">NewExtension (standard)</span><span class="sxs-lookup"><span data-stu-id="bf5eb-105">NewExtension (Default)</span></span>
```
New-AzureServiceRemoteDesktopExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential> [[-Expiration] <DateTime>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="bf5eb-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="bf5eb-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceRemoteDesktopExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential> [[-Expiration] <DateTime>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bf5eb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bf5eb-107">DESCRIPTION</span></span>
<span data-ttu-id="bf5eb-108">Cmdleten **New-AzureServiceRemoteDesktopExtensionConfig** genererar en konfiguration för en fjärr skrivbords ändelse för en distribution.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-108">The **New-AzureServiceRemoteDesktopExtensionConfig** cmdlet generates a configuration for a remote desktop extension for a deployment.</span></span>

## <span data-ttu-id="bf5eb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bf5eb-109">EXAMPLES</span></span>

### <span data-ttu-id="bf5eb-110">Exempel 1: generera en konfiguration för fjärr skrivbords tillägg</span><span class="sxs-lookup"><span data-stu-id="bf5eb-110">Example 1: Generate a remote desktop extension configuration</span></span>
```
PS C:\> $rdpConfig = New-AzureServiceRemoteDesktopExtensionConfig -Credential $cred
```

<span data-ttu-id="bf5eb-111">Det här kommandot skapar en konfiguration för fjärr skrivbords tillägg för angivna autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-111">This command generates a remote desktop extension configuration for the specified credentials.</span></span>

### <span data-ttu-id="bf5eb-112">Exempel 2: generera en konfiguration för fjärr skrivbords tillägg för en viss roll</span><span class="sxs-lookup"><span data-stu-id="bf5eb-112">Example 2: Generate a remote desktop extension configuration for a specified role</span></span>
```
PS C:\> $rdpConfig = New-AzureServiceRemoteDesktopExtensionConfig -Credential $cred -Role "WebRole01"
```

<span data-ttu-id="bf5eb-113">Det här kommandot skapar en konfiguration för fjärr skrivbords tillägg för angivna autentiseringsuppgifter och WebRole01-rollen.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-113">This command generates a remote desktop extension configuration for the specified credentials and the WebRole01 role.</span></span>

## <span data-ttu-id="bf5eb-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bf5eb-114">PARAMETERS</span></span>

### <span data-ttu-id="bf5eb-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="bf5eb-115">-CertificateThumbprint</span></span>
<span data-ttu-id="bf5eb-116">Anger ett certifikat-tumavtryck som ska användas för att kryptera den privata konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="bf5eb-117">Det här certifikatet måste redan finnas i certifikat arkivet.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="bf5eb-118">Om du inte anger ett certifikat skapar den här cmdleten ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="bf5eb-119">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="bf5eb-119">-Credential</span></span>
<span data-ttu-id="bf5eb-120">Anger de autentiseringsuppgifter som ska aktive ras för fjärr skrivbord.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-120">Specifies the credentials to enable for remote desktop.</span></span>
<span data-ttu-id="bf5eb-121">Uppgifterna inkluderar ett användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-121">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf5eb-122">-Utgång</span><span class="sxs-lookup"><span data-stu-id="bf5eb-122">-Expiration</span></span>
<span data-ttu-id="bf5eb-123">Anger ett **datetime** -objekt som gör att användaren kan ange när användar kontot upphör att gälla.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-123">Specifies a **DateTime** object that allows the user to specify when the user account expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf5eb-124">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="bf5eb-124">-ExtensionId</span></span>
<span data-ttu-id="bf5eb-125">Anger tilläggs-ID.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-125">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf5eb-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bf5eb-126">-InformationAction</span></span>
<span data-ttu-id="bf5eb-127">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bf5eb-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="bf5eb-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bf5eb-129">Vidare</span><span class="sxs-lookup"><span data-stu-id="bf5eb-129">Continue</span></span>
- <span data-ttu-id="bf5eb-130">Över</span><span class="sxs-lookup"><span data-stu-id="bf5eb-130">Ignore</span></span>
- <span data-ttu-id="bf5eb-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="bf5eb-131">Inquire</span></span>
- <span data-ttu-id="bf5eb-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bf5eb-132">SilentlyContinue</span></span>
- <span data-ttu-id="bf5eb-133">Stanna</span><span class="sxs-lookup"><span data-stu-id="bf5eb-133">Stop</span></span>
- <span data-ttu-id="bf5eb-134">Avbryt</span><span class="sxs-lookup"><span data-stu-id="bf5eb-134">Suspend</span></span>

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

### <span data-ttu-id="bf5eb-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bf5eb-135">-InformationVariable</span></span>
<span data-ttu-id="bf5eb-136">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bf5eb-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="bf5eb-137">-Profile</span></span>
<span data-ttu-id="bf5eb-138">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bf5eb-139">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bf5eb-140">-Roll</span><span class="sxs-lookup"><span data-stu-id="bf5eb-140">-Role</span></span>
<span data-ttu-id="bf5eb-141">Anger en valfri matris med roller som du kan ange fjärr skrivbords konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-141">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="bf5eb-142">Om den här parametern inte anges används fjärr skrivbords konfigurationen som standard konfiguration för alla roller.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-142">If this parameter is not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="bf5eb-143">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="bf5eb-143">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="bf5eb-144">Anger en algoritm för tumavtryck som används tillsammans med tumavtrycket för att identifiera certifikatet.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-144">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="bf5eb-145">Den här parametern är valfri och standardvärdet är SHA1.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-145">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="bf5eb-146">-Version</span><span class="sxs-lookup"><span data-stu-id="bf5eb-146">-Version</span></span>
<span data-ttu-id="bf5eb-147">Anger tilläggs versionen.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-147">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf5eb-148">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="bf5eb-148">-X509Certificate</span></span>
<span data-ttu-id="bf5eb-149">Anger ett x509-certifikat som ska laddas automatiskt till moln tjänsten och användas för att kryptera den privata konfigurationen för tillägget.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-149">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="bf5eb-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf5eb-150">CommonParameters</span></span>
<span data-ttu-id="bf5eb-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf5eb-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf5eb-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf5eb-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf5eb-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bf5eb-153">INPUTS</span></span>

## <span data-ttu-id="bf5eb-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bf5eb-154">OUTPUTS</span></span>

## <span data-ttu-id="bf5eb-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bf5eb-155">NOTES</span></span>

## <span data-ttu-id="bf5eb-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bf5eb-156">RELATED LINKS</span></span>

[<span data-ttu-id="bf5eb-157">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="bf5eb-157">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


