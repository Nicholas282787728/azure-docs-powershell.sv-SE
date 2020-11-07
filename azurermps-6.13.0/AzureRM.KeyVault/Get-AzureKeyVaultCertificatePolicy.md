---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 8d03d93a374f2184a995d9cbcdb83050aa98a8ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757078"
---
# <span data-ttu-id="13f45-101">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="13f45-101">Get-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="13f45-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13f45-102">SYNOPSIS</span></span>
<span data-ttu-id="13f45-103">Hämtar policyn för ett certifikat i ett valv.</span><span class="sxs-lookup"><span data-stu-id="13f45-103">Gets the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13f45-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13f45-104">SYNTAX</span></span>

### <span data-ttu-id="13f45-105">VaultAndCertName (standard)</span><span class="sxs-lookup"><span data-stu-id="13f45-105">VaultAndCertName (Default)</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13f45-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="13f45-106">InputObject</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13f45-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13f45-107">DESCRIPTION</span></span>
<span data-ttu-id="13f45-108">Cmdleten **Get-AzureKeyVaultCertificatePolicy** hämtar policyn för ett certifikat i ett nyckelord i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="13f45-108">The **Get-AzureKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="13f45-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13f45-109">EXAMPLES</span></span>

### <span data-ttu-id="13f45-110">Exempel 1: skaffa en certifikat policy</span><span class="sxs-lookup"><span data-stu-id="13f45-110">Example 1: Get a certificate policy</span></span>
```powershell
PS C:\ >Get-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"

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

<span data-ttu-id="13f45-111">Det här kommandot får certifikat principen för TestCert01-certifikatet i ContosoKV01-nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="13f45-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="13f45-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13f45-112">PARAMETERS</span></span>

### <span data-ttu-id="13f45-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13f45-113">-DefaultProfile</span></span>
<span data-ttu-id="13f45-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="13f45-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13f45-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13f45-115">-InputObject</span></span>
<span data-ttu-id="13f45-116">Certifikat objekt.</span><span class="sxs-lookup"><span data-stu-id="13f45-116">Certificate Object.</span></span>

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

### <span data-ttu-id="13f45-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="13f45-117">-Name</span></span>
<span data-ttu-id="13f45-118">Anger namnet på ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="13f45-118">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="13f45-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="13f45-119">-VaultName</span></span>
<span data-ttu-id="13f45-120">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="13f45-120">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="13f45-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13f45-121">CommonParameters</span></span>
<span data-ttu-id="13f45-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13f45-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13f45-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13f45-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13f45-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13f45-124">INPUTS</span></span>

### <span data-ttu-id="13f45-125">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="13f45-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="13f45-126">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="13f45-126">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="13f45-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13f45-127">OUTPUTS</span></span>

### <span data-ttu-id="13f45-128">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="13f45-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="13f45-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13f45-129">NOTES</span></span>

## <span data-ttu-id="13f45-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13f45-130">RELATED LINKS</span></span>

[<span data-ttu-id="13f45-131">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="13f45-131">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="13f45-132">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="13f45-132">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

