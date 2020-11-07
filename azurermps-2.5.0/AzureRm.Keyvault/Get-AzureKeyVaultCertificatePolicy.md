---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatepolicy
schema: 2.0.0
ms.openlocfilehash: 692c639ac42d0a8f2dc2bf121321dfc116ebce1b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930254"
---
# <span data-ttu-id="cbdf3-101">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="cbdf3-101">Get-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="cbdf3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cbdf3-102">SYNOPSIS</span></span>
<span data-ttu-id="cbdf3-103">Hämtar policyn för ett certifikat i ett valv.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-103">Gets the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbdf3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cbdf3-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbdf3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cbdf3-105">DESCRIPTION</span></span>
<span data-ttu-id="cbdf3-106">Cmdleten **Get-AzureKeyVaultCertificatePolicy** hämtar policyn för ett certifikat i ett nyckelord i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-106">The **Get-AzureKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="cbdf3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cbdf3-107">EXAMPLES</span></span>

### <span data-ttu-id="cbdf3-108">Exempel 1: skaffa en certifikat policy</span><span class="sxs-lookup"><span data-stu-id="cbdf3-108">Example 1: Get a certificate policy</span></span>
```
PS C:\>Get-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="cbdf3-109">Det här kommandot får certifikat principen för TestCert01-certifikatet i ContosoKV01-nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-109">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="cbdf3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cbdf3-110">PARAMETERS</span></span>

### <span data-ttu-id="cbdf3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbdf3-111">-DefaultProfile</span></span>
<span data-ttu-id="cbdf3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="cbdf3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cbdf3-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="cbdf3-113">-Name</span></span>
<span data-ttu-id="cbdf3-114">Anger namnet på ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-114">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="cbdf3-115">-VaultName</span><span class="sxs-lookup"><span data-stu-id="cbdf3-115">-VaultName</span></span>
<span data-ttu-id="cbdf3-116">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-116">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="cbdf3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbdf3-117">CommonParameters</span></span>
<span data-ttu-id="cbdf3-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbdf3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbdf3-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbdf3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbdf3-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cbdf3-120">INPUTS</span></span>

## <span data-ttu-id="cbdf3-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cbdf3-121">OUTPUTS</span></span>

### <span data-ttu-id="cbdf3-122">Microsoft. Azure. commands. valv. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="cbdf3-122">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="cbdf3-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cbdf3-123">NOTES</span></span>

## <span data-ttu-id="cbdf3-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cbdf3-124">RELATED LINKS</span></span>

[<span data-ttu-id="cbdf3-125">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="cbdf3-125">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="cbdf3-126">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="cbdf3-126">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

