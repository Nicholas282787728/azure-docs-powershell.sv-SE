---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: d525a47dde9551e5d48c7c316cf6844323b75e81
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922722"
---
# <span data-ttu-id="eb428-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="eb428-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="eb428-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb428-102">SYNOPSIS</span></span>
<span data-ttu-id="eb428-103">Hämtar policyn för ett certifikat i ett valv.</span><span class="sxs-lookup"><span data-stu-id="eb428-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="eb428-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb428-104">SYNTAX</span></span>

```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb428-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb428-105">DESCRIPTION</span></span>
<span data-ttu-id="eb428-106">Cmdleten **Get-AzKeyVaultCertificatePolicy** hämtar policyn för ett certifikat i ett nyckelord i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="eb428-106">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="eb428-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb428-107">EXAMPLES</span></span>

### <span data-ttu-id="eb428-108">Exempel 1: skaffa en certifikat policy</span><span class="sxs-lookup"><span data-stu-id="eb428-108">Example 1: Get a certificate policy</span></span>
```
PS C:\>Get-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"
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
RenewAtNumberOfDaysBeforeExpiry : 
RenewAtPercentageLifetime       : 80
EmailOnly                       : False
Enabled                         : True
Created                         : 2/8/2016 11:10:29 PM
Updated                         : 2/8/2016 11:10:29 PM
```

<span data-ttu-id="eb428-109">Det här kommandot får certifikat principen för TestCert01-certifikatet i ContosoKV01-nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="eb428-109">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="eb428-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb428-110">PARAMETERS</span></span>

### <span data-ttu-id="eb428-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb428-111">-DefaultProfile</span></span>
<span data-ttu-id="eb428-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="eb428-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb428-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="eb428-113">-Name</span></span>
<span data-ttu-id="eb428-114">Anger namnet på ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="eb428-114">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb428-115">-VaultName</span><span class="sxs-lookup"><span data-stu-id="eb428-115">-VaultName</span></span>
<span data-ttu-id="eb428-116">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="eb428-116">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="eb428-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb428-117">CommonParameters</span></span>
<span data-ttu-id="eb428-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb428-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb428-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb428-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb428-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb428-120">INPUTS</span></span>

### <span data-ttu-id="eb428-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="eb428-121">None</span></span>
<span data-ttu-id="eb428-122">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="eb428-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eb428-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb428-123">OUTPUTS</span></span>

### <span data-ttu-id="eb428-124">Microsoft. Azure. commands. valv. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="eb428-124">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="eb428-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb428-125">NOTES</span></span>

## <span data-ttu-id="eb428-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb428-126">RELATED LINKS</span></span>

[<span data-ttu-id="eb428-127">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="eb428-127">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="eb428-128">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="eb428-128">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

