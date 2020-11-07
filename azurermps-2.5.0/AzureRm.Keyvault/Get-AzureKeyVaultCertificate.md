---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificate
schema: 2.0.0
ms.openlocfilehash: ed52e229f114666782cb24388db585fd08fa685b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930990"
---
# <span data-ttu-id="e600c-101">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e600c-101">Get-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="e600c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e600c-102">SYNOPSIS</span></span>
<span data-ttu-id="e600c-103">Hämtar ett certifikat från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="e600c-103">Gets a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e600c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e600c-104">SYNTAX</span></span>

### <span data-ttu-id="e600c-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="e600c-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e600c-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="e600c-106">ByCertificateName</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e600c-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="e600c-107">ByCertificateVersions</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e600c-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="e600c-108">ByDeletedCertificates</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e600c-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e600c-109">DESCRIPTION</span></span>
<span data-ttu-id="e600c-110">Cmdleten **Get-AzureKeyVaultCertificate** hämtar det angivna certifikatet eller versionerna av ett certifikat från ett nyckelord i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e600c-110">The **Get-AzureKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="e600c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e600c-111">EXAMPLES</span></span>

### <span data-ttu-id="e600c-112">Exempel 1: skaffa ett certifikat</span><span class="sxs-lookup"><span data-stu-id="e600c-112">Example 1: Get a certificate</span></span>
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

<span data-ttu-id="e600c-113">Det här kommandot hämtar certifikatet med namnet TestCert01 från Key-valvet med namnet ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="e600c-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="e600c-114">Exempel 2: Hämta alla certifikat som har tagits bort men inte rensats för detta huvud valv.</span><span class="sxs-lookup"><span data-stu-id="e600c-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="e600c-115">Det här kommandot får alla certifikat som tidigare har tagits bort, men inte rensats, i det nyckelord som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="e600c-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="e600c-116">Exempel 3: hämtar certifikatet mina certifikat som har tagits bort men inte rensats för detta huvud valv.</span><span class="sxs-lookup"><span data-stu-id="e600c-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="e600c-117">Det här kommandot hämtar certifikatet med namnet "cert" som tidigare har tagits bort, men inte rensat, i det viktigaste valvet med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="e600c-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="e600c-118">Det här kommandot returnerar metadata, till exempel borttagnings datum och det schemalagda rensnings datumet för det här borttagna certifikatet.</span><span class="sxs-lookup"><span data-stu-id="e600c-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="e600c-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e600c-119">PARAMETERS</span></span>

### <span data-ttu-id="e600c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e600c-120">-DefaultProfile</span></span>
<span data-ttu-id="e600c-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e600c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e600c-122">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="e600c-122">-IncludeVersions</span></span>
<span data-ttu-id="e600c-123">Anger att den här åtgärden får alla versioner av certifikatet.</span><span class="sxs-lookup"><span data-stu-id="e600c-123">Indicates that this operation gets all versions of the certificate.</span></span>

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

### <span data-ttu-id="e600c-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="e600c-124">-InRemovedState</span></span>
<span data-ttu-id="e600c-125">Anger om tidigare borttagna certifikat ska tas med i resultatet</span><span class="sxs-lookup"><span data-stu-id="e600c-125">Specifies whether to include previously deleted certificates in the output</span></span>

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

### <span data-ttu-id="e600c-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="e600c-126">-Name</span></span>
<span data-ttu-id="e600c-127">Anger namnet på det certifikat som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="e600c-127">Specifies the name of the certificate to get.</span></span>

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

### <span data-ttu-id="e600c-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e600c-128">-VaultName</span></span>
<span data-ttu-id="e600c-129">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="e600c-129">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="e600c-130">-Version</span><span class="sxs-lookup"><span data-stu-id="e600c-130">-Version</span></span>
<span data-ttu-id="e600c-131">Anger ett certifikats version.</span><span class="sxs-lookup"><span data-stu-id="e600c-131">Specifies the version of a certificate.</span></span>

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

### <span data-ttu-id="e600c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e600c-132">CommonParameters</span></span>
<span data-ttu-id="e600c-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e600c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e600c-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e600c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e600c-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e600c-135">INPUTS</span></span>

## <span data-ttu-id="e600c-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e600c-136">OUTPUTS</span></span>

### <span data-ttu-id="e600c-137">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. valv. Models. CertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="e600c-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="e600c-138">Microsoft. Azure. commands. valv. Models. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e600c-138">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="e600c-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e600c-139">NOTES</span></span>

## <span data-ttu-id="e600c-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e600c-140">RELATED LINKS</span></span>

[<span data-ttu-id="e600c-141">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e600c-141">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="e600c-142">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e600c-142">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="e600c-143">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e600c-143">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)


