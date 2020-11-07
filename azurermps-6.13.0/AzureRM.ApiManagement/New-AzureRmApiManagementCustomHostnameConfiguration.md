---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcustomhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCustomHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCustomHostnameConfiguration.md
ms.openlocfilehash: 2f929fc2968935284024e1112e62b395aa0d545e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756745"
---
# <span data-ttu-id="3d14c-101">New-AzureRmApiManagementCustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d14c-101">New-AzureRmApiManagementCustomHostnameConfiguration</span></span>

## <span data-ttu-id="3d14c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d14c-102">SYNOPSIS</span></span>
<span data-ttu-id="3d14c-103">Skapar en instans av `PsApiManagementCustomHostNameConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="3d14c-103">Creates an instance of `PsApiManagementCustomHostNameConfiguration`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d14c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d14c-104">SYNTAX</span></span>

### <span data-ttu-id="3d14c-105">NoChangeCertificate (standard)</span><span class="sxs-lookup"><span data-stu-id="3d14c-105">NoChangeCertificate (Default)</span></span>
```
New-AzureRmApiManagementCustomHostnameConfiguration -Hostname <String>
 -HostnameType <PsApiManagementHostnameType>
 -HostNameCertificateInformation <PsApiManagementCertificateInformation> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d14c-106">SslCertificateFromFile</span><span class="sxs-lookup"><span data-stu-id="3d14c-106">SslCertificateFromFile</span></span>
```
New-AzureRmApiManagementCustomHostnameConfiguration -Hostname <String>
 -HostnameType <PsApiManagementHostnameType> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultSslBinding] [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d14c-107">SslCertificateFromKeyVault</span><span class="sxs-lookup"><span data-stu-id="3d14c-107">SslCertificateFromKeyVault</span></span>
```
New-AzureRmApiManagementCustomHostnameConfiguration -Hostname <String>
 -HostnameType <PsApiManagementHostnameType> -KeyVaultId <String> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d14c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d14c-108">DESCRIPTION</span></span>
<span data-ttu-id="3d14c-109">**New-AzureRmApiManagementCustomHostnameConfiguration** cmdlet är ett hjälp kommando som skapar en instans av **PsApiManagementCustomHostNameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="3d14c-109">The **New-AzureRmApiManagementCustomHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>
<span data-ttu-id="3d14c-110">Kommandot används med cmdleten New-AzureRmApiManagement och Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="3d14c-110">This command is used with the New-AzureRmApiManagement and Set-AzureRmApiManagement cmdlet.</span></span>

## <span data-ttu-id="3d14c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d14c-111">EXAMPLES</span></span>

### <span data-ttu-id="3d14c-112">Exempel 1: skapa och initiera en instans av PsApiManagementCustomHostNameConfiguration med ett SSL-certifikat från en fil</span><span class="sxs-lookup"><span data-stu-id="3d14c-112">Example 1: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -PfxPath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111" -DefaultSslBinding
PS C:\>$customConfig = @($portal)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig
```

<span data-ttu-id="3d14c-113">Det här kommandot skapar och initierar en instans av **PsApiManagementCustomHostNameConfiguration** för Portal.</span><span class="sxs-lookup"><span data-stu-id="3d14c-113">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration** for Portal.</span></span> <span data-ttu-id="3d14c-114">Därefter skapas en ny ApiManagement-tjänst med anpassad konfiguration av värdnamn.</span><span class="sxs-lookup"><span data-stu-id="3d14c-114">Then it creates a new ApiManagement service with custom hostname configuration.</span></span>

### <span data-ttu-id="3d14c-115">Exempel 2: skapa och initiera en instans av PsApiManagementCustomHostNameConfiguration med en hemlighet från en nyckel valv resurs</span><span class="sxs-lookup"><span data-stu-id="3d14c-115">Example 2: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"

PS C:\>$customConfig = @($portal)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig -AssignIdentity
```

<span data-ttu-id="3d14c-116">Det här kommandot skapar och initierar en instans av **PsApiManagementCustomHostNameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="3d14c-116">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>

## <span data-ttu-id="3d14c-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d14c-117">PARAMETERS</span></span>

### <span data-ttu-id="3d14c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d14c-118">-DefaultProfile</span></span>
<span data-ttu-id="3d14c-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d14c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d14c-120">-DefaultSslBinding</span><span class="sxs-lookup"><span data-stu-id="3d14c-120">-DefaultSslBinding</span></span>
<span data-ttu-id="3d14c-121">Avgör om värdet är hemligt och ska vara krypterat eller inte.</span><span class="sxs-lookup"><span data-stu-id="3d14c-121">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="3d14c-122">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="3d14c-122">This parameter is optional.</span></span>
<span data-ttu-id="3d14c-123">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="3d14c-123">Default Value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d14c-124">-Hostname</span><span class="sxs-lookup"><span data-stu-id="3d14c-124">-Hostname</span></span>
<span data-ttu-id="3d14c-125">Anpassat värdnamn</span><span class="sxs-lookup"><span data-stu-id="3d14c-125">Custom Hostname</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d14c-126">-HostNameCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="3d14c-126">-HostNameCertificateInformation</span></span>
<span data-ttu-id="3d14c-127">Befintlig certifikat konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3d14c-127">Existing Certificate Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation
Parameter Sets: NoChangeCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d14c-128">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="3d14c-128">-HostnameType</span></span>
<span data-ttu-id="3d14c-129">Ange värdnamn</span><span class="sxs-lookup"><span data-stu-id="3d14c-129">Hostname Type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType
Parameter Sets: (All)
Aliases:
Accepted values: Proxy, Portal, Management, Scm

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d14c-130">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="3d14c-130">-KeyVaultId</span></span>
<span data-ttu-id="3d14c-131">KeyVaultId till det hemliga SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="3d14c-131">KeyVaultId to the secret storing the Custom SSL Certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d14c-132">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3d14c-132">-NegotiateClientCertificate</span></span>
<span data-ttu-id="3d14c-133">Avgör om värdet är hemligt och ska vara krypterat eller inte.</span><span class="sxs-lookup"><span data-stu-id="3d14c-133">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="3d14c-134">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="3d14c-134">This parameter is optional.</span></span>
<span data-ttu-id="3d14c-135">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="3d14c-135">Default Value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d14c-136">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="3d14c-136">-PfxPassword</span></span>
<span data-ttu-id="3d14c-137">Lösen ord för. pfx-filen.</span><span class="sxs-lookup"><span data-stu-id="3d14c-137">Password for the .pfx certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SslCertificateFromFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d14c-138">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="3d14c-138">-PfxPath</span></span>
<span data-ttu-id="3d14c-139">Sökväg till en. pfx-fil.</span><span class="sxs-lookup"><span data-stu-id="3d14c-139">Path to a .pfx certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d14c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d14c-140">CommonParameters</span></span>
<span data-ttu-id="3d14c-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d14c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d14c-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d14c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d14c-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d14c-143">INPUTS</span></span>

### <span data-ttu-id="3d14c-144">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="3d14c-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span></span>

## <span data-ttu-id="3d14c-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d14c-145">OUTPUTS</span></span>

### <span data-ttu-id="3d14c-146">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementCustomHostNameConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d14c-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span></span>

## <span data-ttu-id="3d14c-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d14c-147">NOTES</span></span>

## <span data-ttu-id="3d14c-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d14c-148">RELATED LINKS</span></span>

[<span data-ttu-id="3d14c-149">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3d14c-149">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="3d14c-150">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3d14c-150">Set-AzureRmApiManagement</span></span>](./Set-AzureRmApiManagement.md)
