---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5C8B1482-80B0-4060-A35D-E9D394156886
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a6303e685ea02408772a237c6b5f154764107e4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099043"
---
# <span data-ttu-id="29bd4-101">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="29bd4-101">Set-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="29bd4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29bd4-102">SYNOPSIS</span></span>
<span data-ttu-id="29bd4-103">Aktiverar fjärr skrivbords tillägget för angivna roller eller alla roller på en distribuerad tjänst eller vid distribution.</span><span class="sxs-lookup"><span data-stu-id="29bd4-103">Enables remote desktop extension on specified role(s) or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="29bd4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29bd4-104">SYNTAX</span></span>

### <span data-ttu-id="29bd4-105">SetExtension (standard)</span><span class="sxs-lookup"><span data-stu-id="29bd4-105">SetExtension (Default)</span></span>
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="29bd4-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="29bd4-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="29bd4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29bd4-107">DESCRIPTION</span></span>
<span data-ttu-id="29bd4-108">Cmdleten **set-AzureServiceRemoteDesktopExtension** aktiverar fjärr skrivbords tillägget för angivna roller eller alla roller på en distribuerad tjänst eller vid distribution.</span><span class="sxs-lookup"><span data-stu-id="29bd4-108">The **Set-AzureServiceRemoteDesktopExtension** cmdlet enables remote desktop extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="29bd4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29bd4-109">EXAMPLES</span></span>

### <span data-ttu-id="29bd4-110">Exempel 1: aktivera tillägget fjärr skrivbord</span><span class="sxs-lookup"><span data-stu-id="29bd4-110">Example 1: Enable remote desktop extension</span></span>
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds
```

<span data-ttu-id="29bd4-111">Det här kommandot aktiverar fjärr skrivbords tillägget för den angivna tjänsten.</span><span class="sxs-lookup"><span data-stu-id="29bd4-111">This command enables the remote desktop extension for the specified service.</span></span>

### <span data-ttu-id="29bd4-112">Exempel 2: aktivera tillägget fjärr skrivbord för en viss roll</span><span class="sxs-lookup"><span data-stu-id="29bd4-112">Example 2: Enable remote desktop extension for a specified role</span></span>
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds -Role "WebRole1"
```

<span data-ttu-id="29bd4-113">Det här kommandot aktiverar fjärr skrivbords tillägget för den angivna tjänsten och rollen.</span><span class="sxs-lookup"><span data-stu-id="29bd4-113">This command enables the remote desktop extension for the specified service and role.</span></span>

## <span data-ttu-id="29bd4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29bd4-114">PARAMETERS</span></span>

### <span data-ttu-id="29bd4-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="29bd4-115">-CertificateThumbprint</span></span>
<span data-ttu-id="29bd4-116">Anger ett certifikat-tumavtryck som ska användas för att kryptera den privata konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="29bd4-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="29bd4-117">Det här certifikatet måste redan finnas i certifikat arkivet.</span><span class="sxs-lookup"><span data-stu-id="29bd4-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="29bd4-118">Om du inte anger ett certifikat skapar den här cmdleten ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="29bd4-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="29bd4-119">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="29bd4-119">-Credential</span></span>
<span data-ttu-id="29bd4-120">Anger de autentiseringsuppgifter som ska aktive ras för fjärr skrivbord.</span><span class="sxs-lookup"><span data-stu-id="29bd4-120">Specifies the credentials to enable for remote desktop.</span></span>
<span data-ttu-id="29bd4-121">Uppgifterna inkluderar ett användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="29bd4-121">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29bd4-122">-Utgång</span><span class="sxs-lookup"><span data-stu-id="29bd4-122">-Expiration</span></span>
<span data-ttu-id="29bd4-123">Anger ett datum/tid-objekt som gör att användaren kan ange när användar kontot upphör att gälla.</span><span class="sxs-lookup"><span data-stu-id="29bd4-123">Specifies a date time object that allows the user to specify when the user account expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29bd4-124">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="29bd4-124">-ExtensionId</span></span>
<span data-ttu-id="29bd4-125">Anger tilläggs-ID.</span><span class="sxs-lookup"><span data-stu-id="29bd4-125">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29bd4-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="29bd4-126">-InformationAction</span></span>
<span data-ttu-id="29bd4-127">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="29bd4-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="29bd4-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="29bd4-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="29bd4-129">Vidare</span><span class="sxs-lookup"><span data-stu-id="29bd4-129">Continue</span></span>
- <span data-ttu-id="29bd4-130">Över</span><span class="sxs-lookup"><span data-stu-id="29bd4-130">Ignore</span></span>
- <span data-ttu-id="29bd4-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="29bd4-131">Inquire</span></span>
- <span data-ttu-id="29bd4-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="29bd4-132">SilentlyContinue</span></span>
- <span data-ttu-id="29bd4-133">Stanna</span><span class="sxs-lookup"><span data-stu-id="29bd4-133">Stop</span></span>
- <span data-ttu-id="29bd4-134">Avbryt</span><span class="sxs-lookup"><span data-stu-id="29bd4-134">Suspend</span></span>

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

### <span data-ttu-id="29bd4-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="29bd4-135">-InformationVariable</span></span>
<span data-ttu-id="29bd4-136">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="29bd4-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="29bd4-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="29bd4-137">-Profile</span></span>
<span data-ttu-id="29bd4-138">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="29bd4-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="29bd4-139">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="29bd4-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="29bd4-140">-Roll</span><span class="sxs-lookup"><span data-stu-id="29bd4-140">-Role</span></span>
<span data-ttu-id="29bd4-141">Anger en valfri matris med roller som du kan ange fjärr skrivbords konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="29bd4-141">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="29bd4-142">Om den här parametern inte anges används fjärr skrivbords konfigurationen som standard konfiguration för alla roller.</span><span class="sxs-lookup"><span data-stu-id="29bd4-142">If this parameter is not specified, the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="29bd4-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="29bd4-143">-ServiceName</span></span>
<span data-ttu-id="29bd4-144">Anger namnet på distributionen av Azure-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="29bd4-144">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="29bd4-145">-Plats</span><span class="sxs-lookup"><span data-stu-id="29bd4-145">-Slot</span></span>
<span data-ttu-id="29bd4-146">Anger miljön för distributionen som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="29bd4-146">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="29bd4-147">De acceptabla värdena för den här parametern är: produktion, mellanlagring.</span><span class="sxs-lookup"><span data-stu-id="29bd4-147">The acceptable values for this parameter are: Production, Staging.</span></span>

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

### <span data-ttu-id="29bd4-148">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="29bd4-148">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="29bd4-149">Anger en algoritm för tumavtryck som används tillsammans med tumavtrycket för att identifiera certifikatet.</span><span class="sxs-lookup"><span data-stu-id="29bd4-149">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="29bd4-150">Den här parametern är valfri och standardvärdet är SHA1.</span><span class="sxs-lookup"><span data-stu-id="29bd4-150">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="29bd4-151">-Version</span><span class="sxs-lookup"><span data-stu-id="29bd4-151">-Version</span></span>
<span data-ttu-id="29bd4-152">Anger tilläggs versionen.</span><span class="sxs-lookup"><span data-stu-id="29bd4-152">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29bd4-153">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="29bd4-153">-X509Certificate</span></span>
<span data-ttu-id="29bd4-154">Anger ett x509-certifikat som automatiskt laddas upp till moln tjänsten och används för att kryptera den privata konfigurationen för tillägget.</span><span class="sxs-lookup"><span data-stu-id="29bd4-154">Specifies an x509 certificate that is automatically uploaded to the cloud service and used for encrypting the private configuration of the extension.</span></span>

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

### <span data-ttu-id="29bd4-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29bd4-155">CommonParameters</span></span>
<span data-ttu-id="29bd4-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29bd4-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29bd4-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29bd4-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29bd4-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29bd4-158">INPUTS</span></span>

## <span data-ttu-id="29bd4-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29bd4-159">OUTPUTS</span></span>

## <span data-ttu-id="29bd4-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29bd4-160">NOTES</span></span>

## <span data-ttu-id="29bd4-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29bd4-161">RELATED LINKS</span></span>

[<span data-ttu-id="29bd4-162">Get-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="29bd4-162">Get-AzureServiceRemoteDesktopExtension</span></span>](./Get-AzureServiceRemoteDesktopExtension.md)


