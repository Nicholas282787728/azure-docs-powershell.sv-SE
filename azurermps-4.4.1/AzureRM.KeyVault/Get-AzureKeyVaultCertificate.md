---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
ms.openlocfilehash: dd87a5b9abf6126fee71bbc308ec3a985c9da9de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758398"
---
# <span data-ttu-id="db4c3-101">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="db4c3-101">Get-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="db4c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db4c3-102">SYNOPSIS</span></span>
<span data-ttu-id="db4c3-103">Hämtar ett certifikat från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="db4c3-103">Gets a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db4c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db4c3-104">SYNTAX</span></span>

### <span data-ttu-id="db4c3-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="db4c3-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db4c3-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="db4c3-106">ByCertificateName</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db4c3-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="db4c3-107">ByCertificateVersions</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db4c3-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="db4c3-108">ByDeletedCertificates</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db4c3-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db4c3-109">DESCRIPTION</span></span>
<span data-ttu-id="db4c3-110">Cmdleten **Get-AzureKeyVaultCertificate** hämtar det angivna certifikatet eller versionerna av ett certifikat från ett nyckelord i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="db4c3-110">The **Get-AzureKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="db4c3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db4c3-111">EXAMPLES</span></span>

### <span data-ttu-id="db4c3-112">Exempel 1: skaffa ett certifikat</span><span class="sxs-lookup"><span data-stu-id="db4c3-112">Example 1: Get a certificate</span></span>
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

<span data-ttu-id="db4c3-113">Det här kommandot hämtar certifikatet med namnet TestCert01 från Key-valvet med namnet ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="db4c3-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="db4c3-114">Exempel 2: Hämta alla certifikat som har tagits bort men inte rensats för detta huvud valv.</span><span class="sxs-lookup"><span data-stu-id="db4c3-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="db4c3-115">Det här kommandot får alla certifikat som tidigare har tagits bort, men inte rensats, i det nyckelord som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="db4c3-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="db4c3-116">Exempel 3: hämtar certifikatet mina certifikat som har tagits bort men inte rensats för detta huvud valv.</span><span class="sxs-lookup"><span data-stu-id="db4c3-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="db4c3-117">Det här kommandot hämtar certifikatet med namnet "cert" som tidigare har tagits bort, men inte rensat, i det viktigaste valvet med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="db4c3-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="db4c3-118">Det här kommandot returnerar metadata, till exempel borttagnings datum och det schemalagda rensnings datumet för det här borttagna certifikatet.</span><span class="sxs-lookup"><span data-stu-id="db4c3-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="db4c3-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db4c3-119">PARAMETERS</span></span>

### <span data-ttu-id="db4c3-120">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="db4c3-120">-IncludeVersions</span></span>
<span data-ttu-id="db4c3-121">Anger att den här åtgärden får alla versioner av certifikatet.</span><span class="sxs-lookup"><span data-stu-id="db4c3-121">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByCertificateVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4c3-122">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="db4c3-122">-InRemovedState</span></span>
<span data-ttu-id="db4c3-123">Anger om tidigare borttagna certifikat ska tas med i resultatet.</span><span class="sxs-lookup"><span data-stu-id="db4c3-123">Specifies whether to include previously deleted certificates in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedCertificates
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4c3-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="db4c3-124">-Name</span></span>
<span data-ttu-id="db4c3-125">Anger namnet på det certifikat som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="db4c3-125">Specifies the name of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName, ByCertificateVersions
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedCertificates
Aliases: CertificateName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db4c3-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="db4c3-126">-VaultName</span></span>
<span data-ttu-id="db4c3-127">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="db4c3-127">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db4c3-128">-Version</span><span class="sxs-lookup"><span data-stu-id="db4c3-128">-Version</span></span>
<span data-ttu-id="db4c3-129">Anger ett certifikats version.</span><span class="sxs-lookup"><span data-stu-id="db4c3-129">Specifies the version of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: CertificateVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db4c3-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db4c3-130">-DefaultProfile</span></span>
<span data-ttu-id="db4c3-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="db4c3-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db4c3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db4c3-132">CommonParameters</span></span>
<span data-ttu-id="db4c3-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db4c3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db4c3-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db4c3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db4c3-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db4c3-135">INPUTS</span></span>

## <span data-ttu-id="db4c3-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db4c3-136">OUTPUTS</span></span>

### <span data-ttu-id="db4c3-137">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. valv. Models. CertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="db4c3-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="db4c3-138">Microsoft. Azure. commands. valv. Models. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="db4c3-138">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="db4c3-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db4c3-139">NOTES</span></span>

## <span data-ttu-id="db4c3-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db4c3-140">RELATED LINKS</span></span>

[<span data-ttu-id="db4c3-141">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="db4c3-141">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="db4c3-142">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="db4c3-142">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="db4c3-143">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="db4c3-143">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="db4c3-144">Ångra-AzureKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="db4c3-144">Undo-AzureKeyVaultSecretCertificate</span></span>](./Undo-AzureKeyVaultSecretCertificate.md)
