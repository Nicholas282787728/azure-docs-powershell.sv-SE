---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
ms.openlocfilehash: 87b030229eb2a1f4bb91122aaec8a119134d27fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575645"
---
# <span data-ttu-id="7e8b4-101">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7e8b4-101">Get-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="7e8b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e8b4-102">SYNOPSIS</span></span>
<span data-ttu-id="7e8b4-103">Hämtar ett certifikat från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-103">Gets a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e8b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e8b4-104">SYNTAX</span></span>

### <span data-ttu-id="7e8b4-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="7e8b4-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e8b4-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="7e8b4-106">ByCertificateNameAndVersion</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e8b4-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="7e8b4-107">ByCertificateAllVersions</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e8b4-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="7e8b4-108">ByNameInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e8b4-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="7e8b4-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e8b4-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="7e8b4-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e8b4-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e8b4-111">DESCRIPTION</span></span>
<span data-ttu-id="7e8b4-112">Cmdleten **Get-AzureKeyVaultCertificate** hämtar det angivna certifikatet eller versionerna av ett certifikat från ett nyckelord i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-112">The **Get-AzureKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="7e8b4-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e8b4-113">EXAMPLES</span></span>

### <span data-ttu-id="7e8b4-114">Exempel 1: skaffa ett certifikat</span><span class="sxs-lookup"><span data-stu-id="7e8b4-114">Example 1: Get a certificate</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject] 
                CN=contoso.com

              [Issuer] 
                CN=contoso.com

              [Serial Number] 
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before] 
                2/8/2016 3:11:45 PM

              [Not After] 
                8/8/2016 4:21:45 PM

              [Thumbprint] 
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="7e8b4-115">Det här kommandot hämtar certifikatet med namnet TestCert01 från Key-valvet med namnet ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-115">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="7e8b4-116">Exempel 2: Hämta alla certifikat som har tagits bort men inte rensats för detta huvud valv.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-116">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="7e8b4-117">Det här kommandot får alla certifikat som tidigare har tagits bort, men inte rensats, i det nyckelord som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-117">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="7e8b4-118">Exempel 3: hämtar certifikatet mina certifikat som har tagits bort men inte rensats för detta huvud valv.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-118">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="7e8b4-119">Det här kommandot hämtar certifikatet med namnet "cert" som tidigare har tagits bort, men inte rensat, i det viktigaste valvet med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-119">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="7e8b4-120">Det här kommandot returnerar metadata, till exempel borttagnings datum och det schemalagda rensnings datumet för det här borttagna certifikatet.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-120">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="7e8b4-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e8b4-121">PARAMETERS</span></span>

### <span data-ttu-id="7e8b4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e8b4-122">-DefaultProfile</span></span>
<span data-ttu-id="7e8b4-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7e8b4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e8b4-124">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="7e8b4-124">-IncludeVersions</span></span>
<span data-ttu-id="7e8b4-125">Anger att den här åtgärden får alla versioner av certifikatet.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-125">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByCertificateAllVersions, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e8b4-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e8b4-126">-InputObject</span></span>
<span data-ttu-id="7e8b4-127">Valv objekt.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-127">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByNameInputObject, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e8b4-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="7e8b4-128">-InRemovedState</span></span>
<span data-ttu-id="7e8b4-129">Anger om tidigare borttagna certifikat ska tas med i resultatet</span><span class="sxs-lookup"><span data-stu-id="7e8b4-129">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByName, ByNameInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e8b4-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="7e8b4-130">-Name</span></span>
<span data-ttu-id="7e8b4-131">Anger namnet på det certifikat som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-131">Specifies the name of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByNameInputObject
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e8b4-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7e8b4-132">-VaultName</span></span>
<span data-ttu-id="7e8b4-133">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-133">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByCertificateNameAndVersion, ByCertificateAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e8b4-134">-Version</span><span class="sxs-lookup"><span data-stu-id="7e8b4-134">-Version</span></span>
<span data-ttu-id="7e8b4-135">Anger ett certifikats version.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-135">Specifies the version of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateNameAndVersionInputObject
Aliases: CertificateVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e8b4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e8b4-136">CommonParameters</span></span>
<span data-ttu-id="7e8b4-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e8b4-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e8b4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e8b4-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e8b4-139">INPUTS</span></span>

### <span data-ttu-id="7e8b4-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="7e8b4-140">None</span></span>
<span data-ttu-id="7e8b4-141">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7e8b4-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e8b4-142">OUTPUTS</span></span>

### <span data-ttu-id="7e8b4-143">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="7e8b4-143">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem]</span></span>

### <span data-ttu-id="7e8b4-144">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7e8b4-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="7e8b4-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e8b4-145">NOTES</span></span>

## <span data-ttu-id="7e8b4-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e8b4-146">RELATED LINKS</span></span>

[<span data-ttu-id="7e8b4-147">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7e8b4-147">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="7e8b4-148">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7e8b4-148">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="7e8b4-149">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7e8b4-149">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="7e8b4-150">Ångra-AzureKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="7e8b4-150">Undo-AzureKeyVaultSecretCertificate</span></span>](./Undo-AzureKeyVaultSecretCertificate.md)
