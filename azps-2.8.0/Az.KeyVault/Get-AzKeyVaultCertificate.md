---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: 5935706c341fac5f0b26d3e4965f226342c3dfc8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743932"
---
# <span data-ttu-id="4221f-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4221f-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="4221f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4221f-102">SYNOPSIS</span></span>
<span data-ttu-id="4221f-103">Hämtar ett certifikat från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="4221f-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="4221f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4221f-104">SYNTAX</span></span>

### <span data-ttu-id="4221f-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="4221f-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4221f-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="4221f-106">ByCertificateNameAndVersion</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4221f-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="4221f-107">ByCertificateAllVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4221f-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="4221f-108">ByNameInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4221f-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="4221f-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4221f-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="4221f-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4221f-111">ByNameResourceId</span><span class="sxs-lookup"><span data-stu-id="4221f-111">ByNameResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4221f-112">ByCertificateNameAndVersionResourceId</span><span class="sxs-lookup"><span data-stu-id="4221f-112">ByCertificateNameAndVersionResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4221f-113">ByCertificateAllVersionsResourceId</span><span class="sxs-lookup"><span data-stu-id="4221f-113">ByCertificateAllVersionsResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4221f-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4221f-114">DESCRIPTION</span></span>
<span data-ttu-id="4221f-115">Cmdleten **Get-AzKeyVaultCertificate** hämtar det angivna certifikatet eller versionerna av ett certifikat från ett nyckelord i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="4221f-115">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="4221f-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4221f-116">EXAMPLES</span></span>

### <span data-ttu-id="4221f-117">Exempel 1: skaffa ett certifikat</span><span class="sxs-lookup"><span data-stu-id="4221f-117">Example 1: Get a certificate</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject] 
                CN=contoso.com

              [Issuer] 
                CN=contoso.com

              [Serial Number] 
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before] 
                2/8/2016 3:11:45 PM

              [Not After] 
                8/8/2016 4:21:45 PM

              [Thumbprint] 
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="4221f-118">Det här kommandot hämtar certifikatet med namnet TestCert01 från Key-valvet med namnet ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="4221f-118">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="4221f-119">Exempel 2: Hämta alla certifikat som har tagits bort men inte rensats för detta huvud valv.</span><span class="sxs-lookup"><span data-stu-id="4221f-119">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName 'contoso' -InRemovedState

DeletedDate        : 5/24/2018 6:08:32 PM
Enabled            : True
Expires            : 11/24/2018 6:08:13 PM
NotBefore          : 5/24/2018 5:58:13 PM
Created            : 5/24/2018 6:08:13 PM
Updated            : 5/24/2018 6:08:13 PM
Tags               :
VaultName          : contoso
Name               : test1
Version            :
Id                 : https://contoso.vault.azure.net:443/certificates/test1

ScheduledPurgeDate : 8/22/2018 6:10:47 PM
DeletedDate        : 5/24/2018 6:10:47 PM
Enabled            : True
Expires            : 11/24/2018 6:09:44 PM
NotBefore          : 5/24/2018 5:59:44 PM
Created            : 5/24/2018 6:09:44 PM
Updated            : 5/24/2018 6:09:44 PM
Tags               :
VaultName          : contoso
Name               : test2
Version            :
Id                 : https://contoso.vault.azure.net:443/certificates/test2
```

<span data-ttu-id="4221f-120">Det här kommandot får alla certifikat som tidigare har tagits bort, men inte rensats, i det nyckelord som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="4221f-120">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="4221f-121">Exempel 3: hämtar certifikatet mina certifikat som har tagits bort men inte rensats för detta huvud valv.</span><span class="sxs-lookup"><span data-stu-id="4221f-121">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName 'contoso' -Name 'test1' -InRemovedState

Certificate        : [Subject]
                       CN=contoso.com

                     [Issuer]
                       CN=contoso.com

                     [Serial Number]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                     [Not Before]
                       5/24/2018 10:58:13 AM

                     [Not After]
                       11/24/2018 10:08:13 AM

                     [Thumbprint]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId              : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
SecretId           : https://contoso.vault.azure.net:443/secrets/test1/7fe415d5518240c1a6fce89986b8d334
Thumbprint         : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel      : Recoverable+Purgeable
ScheduledPurgeDate : 8/22/2018 6:08:32 PM
DeletedDate        : 5/24/2018 6:08:32 PM
Enabled            : True
Expires            : 11/24/2018 6:08:13 PM
NotBefore          : 5/24/2018 5:58:13 PM
Created            : 5/24/2018 6:08:13 PM
Updated            : 5/24/2018 6:08:13 PM
Tags               :
VaultName          : contoso
Name               : test1
Version            : 7fe415d5518240c1a6fce89986b8d334
Id                 : https://contoso.vault.azure.net:443/certificates/test1/7fe415d5518240c1a6fce89986b8d334
```

<span data-ttu-id="4221f-122">Det här kommandot hämtar certifikatet med namnet "cert" som tidigare har tagits bort, men inte rensat, i det viktigaste valvet med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="4221f-122">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="4221f-123">Det här kommandot returnerar metadata, till exempel borttagnings datum och det schemalagda rensnings datumet för det här borttagna certifikatet.</span><span class="sxs-lookup"><span data-stu-id="4221f-123">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

### <span data-ttu-id="4221f-124">Exempel 4: ange certifikat med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="4221f-124">Example 4: List certificates using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "test*"

Enabled   : True
Expires   : 8/5/2019 2:39:25 AM
NotBefore : 2/5/2019 2:29:25 AM
Created   : 2/5/2019 2:39:25 AM
Updated   : 2/5/2019 2:39:25 AM
Tags      :
VaultName : ContosoKV01
Name      : test1
Version   :
Id        : https://ContosoKV01.vault.azure.net:443/certificates/test1

Enabled   : True
Expires   : 8/5/2019 2:39:25 AM
NotBefore : 2/5/2019 2:29:25 AM
Created   : 2/5/2019 2:39:25 AM
Updated   : 2/5/2019 2:39:25 AM
Tags      :
VaultName : ContosoKV01
Name      : test2
Version   :
Id        : https://ContosoKV01.vault.azure.net:443/certificates/test2

This command gets all certificates starting with "test" from the key vault named ContosoKV01.
```

## <span data-ttu-id="4221f-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4221f-125">PARAMETERS</span></span>

### <span data-ttu-id="4221f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4221f-126">-DefaultProfile</span></span>
<span data-ttu-id="4221f-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4221f-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4221f-128">-IncludePending</span><span class="sxs-lookup"><span data-stu-id="4221f-128">-IncludePending</span></span>
<span data-ttu-id="4221f-129">Anger om väntande certifikat ska tas med i resultatet</span><span class="sxs-lookup"><span data-stu-id="4221f-129">Specifies whether to include pending certificates in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4221f-130">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="4221f-130">-IncludeVersions</span></span>
<span data-ttu-id="4221f-131">Anger att den här åtgärden får alla versioner av certifikatet.</span><span class="sxs-lookup"><span data-stu-id="4221f-131">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByCertificateAllVersions, ByCertificateAllVersionsInputObject, ByCertificateAllVersionsResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4221f-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4221f-132">-InputObject</span></span>
<span data-ttu-id="4221f-133">Valv objekt.</span><span class="sxs-lookup"><span data-stu-id="4221f-133">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByNameInputObject, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4221f-134">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="4221f-134">-InRemovedState</span></span>
<span data-ttu-id="4221f-135">Anger om tidigare borttagna certifikat ska tas med i resultatet</span><span class="sxs-lookup"><span data-stu-id="4221f-135">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4221f-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="4221f-136">-Name</span></span>
<span data-ttu-id="4221f-137">Anger namnet på det certifikat som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="4221f-137">Specifies the name of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="4221f-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4221f-138">-ResourceId</span></span>
<span data-ttu-id="4221f-139">Resurs-ID för valv.</span><span class="sxs-lookup"><span data-stu-id="4221f-139">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameResourceId, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4221f-140">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4221f-140">-VaultName</span></span>
<span data-ttu-id="4221f-141">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="4221f-141">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByCertificateNameAndVersion, ByCertificateAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4221f-142">-Version</span><span class="sxs-lookup"><span data-stu-id="4221f-142">-Version</span></span>
<span data-ttu-id="4221f-143">Anger ett certifikats version.</span><span class="sxs-lookup"><span data-stu-id="4221f-143">Specifies the version of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateNameAndVersionInputObject, ByCertificateNameAndVersionResourceId
Aliases: CertificateVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4221f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4221f-144">CommonParameters</span></span>
<span data-ttu-id="4221f-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4221f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4221f-146">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4221f-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4221f-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4221f-147">INPUTS</span></span>

### <span data-ttu-id="4221f-148">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="4221f-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="4221f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="4221f-149">System.String</span></span>

## <span data-ttu-id="4221f-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4221f-150">OUTPUTS</span></span>

### <span data-ttu-id="4221f-151">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4221f-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

### <span data-ttu-id="4221f-152">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4221f-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

### <span data-ttu-id="4221f-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4221f-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

### <span data-ttu-id="4221f-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4221f-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="4221f-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4221f-155">NOTES</span></span>

## <span data-ttu-id="4221f-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4221f-156">RELATED LINKS</span></span>

[<span data-ttu-id="4221f-157">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4221f-157">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="4221f-158">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4221f-158">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="4221f-159">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4221f-159">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="4221f-160">Ångra-AzKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="4221f-160">Undo-AzKeyVaultSecretCertificate</span></span>](./Undo-AzKeyVaultSecretCertificate.md)
