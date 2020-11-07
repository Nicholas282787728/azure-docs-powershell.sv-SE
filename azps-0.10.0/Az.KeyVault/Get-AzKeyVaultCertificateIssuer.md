---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: b9188e1bb4d5de4896bf0ca3b2844c7718593ca2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922734"
---
# <span data-ttu-id="9d41f-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9d41f-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="9d41f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9d41f-102">SYNOPSIS</span></span>
<span data-ttu-id="9d41f-103">Hämtar en certifikat utfärdare för ett viktigt valv.</span><span class="sxs-lookup"><span data-stu-id="9d41f-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="9d41f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9d41f-104">SYNTAX</span></span>

### <span data-ttu-id="9d41f-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="9d41f-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d41f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9d41f-106">ByName</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d41f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9d41f-107">DESCRIPTION</span></span>
<span data-ttu-id="9d41f-108">Cmdleten **Get-AzKeyVaultCertificateIssuer** hämtar en angiven certifikat utfärdare eller alla certifikat utfärdare för ett nyckeltal i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="9d41f-108">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="9d41f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9d41f-109">EXAMPLES</span></span>

### <span data-ttu-id="9d41f-110">Exempel 1: skaffa en certifikat utfärdare</span><span class="sxs-lookup"><span data-stu-id="9d41f-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="9d41f-111">Det här kommandot får certifikat utfärdaren med namnet TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="9d41f-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="9d41f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9d41f-112">PARAMETERS</span></span>

### <span data-ttu-id="9d41f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d41f-113">-DefaultProfile</span></span>
<span data-ttu-id="9d41f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9d41f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d41f-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="9d41f-115">-Name</span></span>
<span data-ttu-id="9d41f-116">Anger namnet på den certifikat utfärdare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="9d41f-116">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d41f-117">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9d41f-117">-VaultName</span></span>
<span data-ttu-id="9d41f-118">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="9d41f-118">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="9d41f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d41f-119">CommonParameters</span></span>
<span data-ttu-id="9d41f-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d41f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d41f-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d41f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d41f-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9d41f-122">INPUTS</span></span>

### <span data-ttu-id="9d41f-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="9d41f-123">None</span></span>
<span data-ttu-id="9d41f-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="9d41f-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9d41f-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9d41f-125">OUTPUTS</span></span>

### <span data-ttu-id="9d41f-126">List<Microsoft. Azure. kommandon. KeyVaultCertificateIssuer. Models. CertificateIssuerIdentityItem>, Microsoft. Azure. kommandon.</span><span class="sxs-lookup"><span data-stu-id="9d41f-126">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="9d41f-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9d41f-127">NOTES</span></span>

## <span data-ttu-id="9d41f-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9d41f-128">RELATED LINKS</span></span>

[<span data-ttu-id="9d41f-129">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9d41f-129">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="9d41f-130">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9d41f-130">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


