---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: d6e2225cc7441d4c370d990aa45c9b2c2bb40457
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088418"
---
# <span data-ttu-id="039a7-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="039a7-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="039a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="039a7-102">SYNOPSIS</span></span>
<span data-ttu-id="039a7-103">Hämtar policyn för ett certifikat i ett valv.</span><span class="sxs-lookup"><span data-stu-id="039a7-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="039a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="039a7-104">SYNTAX</span></span>

### <span data-ttu-id="039a7-105">VaultAndCertName (standard)</span><span class="sxs-lookup"><span data-stu-id="039a7-105">VaultAndCertName (Default)</span></span>
```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="039a7-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="039a7-106">InputObject</span></span>
```
Get-AzKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="039a7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="039a7-107">DESCRIPTION</span></span>
<span data-ttu-id="039a7-108">Cmdleten **Get-AzKeyVaultCertificatePolicy** hämtar policyn för ett certifikat i ett nyckelord i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="039a7-108">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="039a7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="039a7-109">EXAMPLES</span></span>

### <span data-ttu-id="039a7-110">Exempel 1: skaffa en certifikat policy</span><span class="sxs-lookup"><span data-stu-id="039a7-110">Example 1: Get a certificate policy</span></span>
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

<span data-ttu-id="039a7-111">Det här kommandot får certifikat principen för TestCert01-certifikatet i ContosoKV01-nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="039a7-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="039a7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="039a7-112">PARAMETERS</span></span>

### <span data-ttu-id="039a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="039a7-113">-DefaultProfile</span></span>
<span data-ttu-id="039a7-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="039a7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="039a7-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="039a7-115">-InputObject</span></span>
<span data-ttu-id="039a7-116">Certifikat objekt.</span><span class="sxs-lookup"><span data-stu-id="039a7-116">Certificate Object.</span></span>

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

### <span data-ttu-id="039a7-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="039a7-117">-Name</span></span>
<span data-ttu-id="039a7-118">Anger namnet på ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="039a7-118">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="039a7-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="039a7-119">-VaultName</span></span>
<span data-ttu-id="039a7-120">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="039a7-120">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="039a7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="039a7-121">CommonParameters</span></span>
<span data-ttu-id="039a7-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="039a7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="039a7-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="039a7-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="039a7-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="039a7-124">INPUTS</span></span>

### <span data-ttu-id="039a7-125">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="039a7-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="039a7-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="039a7-126">OUTPUTS</span></span>

### <span data-ttu-id="039a7-127">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="039a7-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="039a7-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="039a7-128">NOTES</span></span>

## <span data-ttu-id="039a7-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="039a7-129">RELATED LINKS</span></span>

[<span data-ttu-id="039a7-130">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="039a7-130">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="039a7-131">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="039a7-131">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

