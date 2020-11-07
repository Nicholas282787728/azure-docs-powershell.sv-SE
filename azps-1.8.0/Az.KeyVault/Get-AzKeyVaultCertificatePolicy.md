---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: a6635afc19f95f32d7c50ff7a92ba5868a5945e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916326"
---
# <span data-ttu-id="bd97a-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="bd97a-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="bd97a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd97a-102">SYNOPSIS</span></span>
<span data-ttu-id="bd97a-103">Hämtar policyn för ett certifikat i ett valv.</span><span class="sxs-lookup"><span data-stu-id="bd97a-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="bd97a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd97a-104">SYNTAX</span></span>

### <span data-ttu-id="bd97a-105">VaultAndCertName (standard)</span><span class="sxs-lookup"><span data-stu-id="bd97a-105">VaultAndCertName (Default)</span></span>
```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd97a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="bd97a-106">InputObject</span></span>
```
Get-AzKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd97a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd97a-107">DESCRIPTION</span></span>
<span data-ttu-id="bd97a-108">Cmdleten **Get-AzKeyVaultCertificatePolicy** hämtar policyn för ett certifikat i ett nyckelord i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="bd97a-108">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="bd97a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd97a-109">EXAMPLES</span></span>

### <span data-ttu-id="bd97a-110">Exempel 1: skaffa en certifikat policy</span><span class="sxs-lookup"><span data-stu-id="bd97a-110">Example 1: Get a certificate policy</span></span>
```powershell
PS C:\ >Get-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"

SecretContentType               : application/x-pkcs12
Kty                             : RSA
KeySize                         : 2048
Exportable                      : True
ReuseKeyOnRenewal               : True
SubjectName                     : CN=contoso.com
DnsNames                        : 
Ekus                            : {1.3.6.1.5.5.7.3.1, 1.3.6.1.5.5.7.3.2}
ValidityInMonths                : 6
IssuerName                      : Self
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry : 
RenewAtPercentageLifetime       : 80
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
Enabled                         : True
Created                         : 2/8/2016 11:10:29 PM
Updated                         : 2/8/2016 11:10:29 PM
```

<span data-ttu-id="bd97a-111">Det här kommandot får certifikat principen för TestCert01-certifikatet i ContosoKV01-nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="bd97a-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="bd97a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd97a-112">PARAMETERS</span></span>

### <span data-ttu-id="bd97a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd97a-113">-DefaultProfile</span></span>
<span data-ttu-id="bd97a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bd97a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd97a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd97a-115">-InputObject</span></span>
<span data-ttu-id="bd97a-116">Certifikat objekt.</span><span class="sxs-lookup"><span data-stu-id="bd97a-116">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd97a-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="bd97a-117">-Name</span></span>
<span data-ttu-id="bd97a-118">Anger namnet på ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="bd97a-118">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultAndCertName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd97a-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="bd97a-119">-VaultName</span></span>
<span data-ttu-id="bd97a-120">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="bd97a-120">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultAndCertName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd97a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd97a-121">CommonParameters</span></span>
<span data-ttu-id="bd97a-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd97a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd97a-123">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd97a-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd97a-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd97a-124">INPUTS</span></span>

### <span data-ttu-id="bd97a-125">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="bd97a-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="bd97a-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd97a-126">OUTPUTS</span></span>

### <span data-ttu-id="bd97a-127">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="bd97a-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="bd97a-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd97a-128">NOTES</span></span>

## <span data-ttu-id="bd97a-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd97a-129">RELATED LINKS</span></span>

[<span data-ttu-id="bd97a-130">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="bd97a-130">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="bd97a-131">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="bd97a-131">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

