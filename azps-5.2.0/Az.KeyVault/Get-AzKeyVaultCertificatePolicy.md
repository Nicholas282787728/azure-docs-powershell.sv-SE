---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: d6e2225cc7441d4c370d990aa45c9b2c2bb40457
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414995"
---
# <span data-ttu-id="40017-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="40017-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="40017-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40017-102">SYNOPSIS</span></span>
<span data-ttu-id="40017-103">Hämtar policyn för ett certifikat i ett valv.</span><span class="sxs-lookup"><span data-stu-id="40017-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="40017-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40017-104">SYNTAX</span></span>

### <span data-ttu-id="40017-105">VaultAndCertName (standard)</span><span class="sxs-lookup"><span data-stu-id="40017-105">VaultAndCertName (Default)</span></span>
```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40017-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="40017-106">InputObject</span></span>
```
Get-AzKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40017-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40017-107">DESCRIPTION</span></span>
<span data-ttu-id="40017-108">Cmdleten **Get-AzKeyVaultCertificatePolicy** hämtar policyn för ett certifikat i ett nyckelord i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="40017-108">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="40017-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40017-109">EXAMPLES</span></span>

### <span data-ttu-id="40017-110">Exempel 1: skaffa en certifikat policy</span><span class="sxs-lookup"><span data-stu-id="40017-110">Example 1: Get a certificate policy</span></span>
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

<span data-ttu-id="40017-111">Det här kommandot får certifikat principen för TestCert01-certifikatet i ContosoKV01-nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="40017-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="40017-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40017-112">PARAMETERS</span></span>

### <span data-ttu-id="40017-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40017-113">-DefaultProfile</span></span>
<span data-ttu-id="40017-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="40017-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40017-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40017-115">-InputObject</span></span>
<span data-ttu-id="40017-116">Certifikat objekt.</span><span class="sxs-lookup"><span data-stu-id="40017-116">Certificate Object.</span></span>

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

### <span data-ttu-id="40017-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="40017-117">-Name</span></span>
<span data-ttu-id="40017-118">Anger namnet på ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="40017-118">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="40017-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="40017-119">-VaultName</span></span>
<span data-ttu-id="40017-120">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="40017-120">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="40017-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40017-121">CommonParameters</span></span>
<span data-ttu-id="40017-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40017-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40017-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40017-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40017-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40017-124">INPUTS</span></span>

### <span data-ttu-id="40017-125">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="40017-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="40017-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40017-126">OUTPUTS</span></span>

### <span data-ttu-id="40017-127">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="40017-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="40017-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40017-128">NOTES</span></span>

## <span data-ttu-id="40017-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40017-129">RELATED LINKS</span></span>

[<span data-ttu-id="40017-130">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="40017-130">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="40017-131">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="40017-131">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

