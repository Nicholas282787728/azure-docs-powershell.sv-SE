---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: 40514bdd6ed8d37679d3002f80146e622a0614e9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922741"
---
# <span data-ttu-id="8a722-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8a722-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="8a722-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a722-102">SYNOPSIS</span></span>
<span data-ttu-id="8a722-103">Hämtar ett certifikat från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="8a722-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="8a722-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a722-104">SYNTAX</span></span>

### <span data-ttu-id="8a722-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="8a722-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a722-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="8a722-106">ByCertificateName</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a722-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="8a722-107">ByCertificateVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a722-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="8a722-108">ByDeletedCertificates</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a722-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a722-109">DESCRIPTION</span></span>
<span data-ttu-id="8a722-110">Cmdleten **Get-AzKeyVaultCertificate** hämtar det angivna certifikatet eller versionerna av ett certifikat från ett nyckelord i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="8a722-110">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="8a722-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a722-111">EXAMPLES</span></span>

### <span data-ttu-id="8a722-112">Exempel 1: skaffa ett certifikat</span><span class="sxs-lookup"><span data-stu-id="8a722-112">Example 1: Get a certificate</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="8a722-113">Det här kommandot hämtar certifikatet med namnet TestCert01 från Key-valvet med namnet ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="8a722-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="8a722-114">Exempel 2: Hämta alla certifikat som har tagits bort men inte rensats för detta huvud valv.</span><span class="sxs-lookup"><span data-stu-id="8a722-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="8a722-115">Det här kommandot får alla certifikat som tidigare har tagits bort, men inte rensats, i det nyckelord som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="8a722-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="8a722-116">Exempel 3: hämtar certifikatet mina certifikat som har tagits bort men inte rensats för detta huvud valv.</span><span class="sxs-lookup"><span data-stu-id="8a722-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="8a722-117">Det här kommandot hämtar certifikatet med namnet "cert" som tidigare har tagits bort, men inte rensat, i det viktigaste valvet med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="8a722-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="8a722-118">Det här kommandot returnerar metadata, till exempel borttagnings datum och det schemalagda rensnings datumet för det här borttagna certifikatet.</span><span class="sxs-lookup"><span data-stu-id="8a722-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="8a722-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a722-119">PARAMETERS</span></span>

### <span data-ttu-id="8a722-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a722-120">-DefaultProfile</span></span>
<span data-ttu-id="8a722-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8a722-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a722-122">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="8a722-122">-IncludeVersions</span></span>
<span data-ttu-id="8a722-123">Anger att den här åtgärden får alla versioner av certifikatet.</span><span class="sxs-lookup"><span data-stu-id="8a722-123">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByCertificateVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a722-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="8a722-124">-InRemovedState</span></span>
<span data-ttu-id="8a722-125">Anger om tidigare borttagna certifikat ska tas med i resultatet</span><span class="sxs-lookup"><span data-stu-id="8a722-125">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedCertificates
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a722-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="8a722-126">-Name</span></span>
<span data-ttu-id="8a722-127">Anger namnet på det certifikat som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="8a722-127">Specifies the name of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName, ByCertificateVersions
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedCertificates
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a722-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8a722-128">-VaultName</span></span>
<span data-ttu-id="8a722-129">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="8a722-129">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a722-130">-Version</span><span class="sxs-lookup"><span data-stu-id="8a722-130">-Version</span></span>
<span data-ttu-id="8a722-131">Anger ett certifikats version.</span><span class="sxs-lookup"><span data-stu-id="8a722-131">Specifies the version of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a722-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a722-132">CommonParameters</span></span>
<span data-ttu-id="8a722-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a722-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a722-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a722-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a722-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a722-135">INPUTS</span></span>

### <span data-ttu-id="8a722-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="8a722-136">None</span></span>
<span data-ttu-id="8a722-137">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="8a722-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8a722-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a722-138">OUTPUTS</span></span>

### <span data-ttu-id="8a722-139">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. valv. Models. CertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="8a722-139">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="8a722-140">Microsoft. Azure. commands. valv. Models. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8a722-140">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="8a722-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a722-141">NOTES</span></span>

## <span data-ttu-id="8a722-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a722-142">RELATED LINKS</span></span>

[<span data-ttu-id="8a722-143">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8a722-143">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="8a722-144">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8a722-144">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="8a722-145">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8a722-145">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="8a722-146">Ångra-AzKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="8a722-146">Undo-AzKeyVaultSecretCertificate</span></span>](./Undo-AzKeyVaultSecretCertificate.md)
