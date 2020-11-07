---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
ms.openlocfilehash: fcbb19936bb9924f95aa3a20fa026a9c8c723033
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930258"
---
# <span data-ttu-id="b0898-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b0898-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="b0898-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0898-102">SYNOPSIS</span></span>
<span data-ttu-id="b0898-103">Hämtar en certifikat utfärdare för ett viktigt valv.</span><span class="sxs-lookup"><span data-stu-id="b0898-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0898-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0898-104">SYNTAX</span></span>

### <span data-ttu-id="b0898-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="b0898-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0898-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b0898-106">ByName</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0898-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0898-107">DESCRIPTION</span></span>
<span data-ttu-id="b0898-108">Cmdleten **Get-AzureKeyVaultCertificateIssuer** hämtar en angiven certifikat utfärdare eller alla certifikat utfärdare för ett nyckeltal i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="b0898-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="b0898-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0898-109">EXAMPLES</span></span>

### <span data-ttu-id="b0898-110">Exempel 1: skaffa en certifikat utfärdare</span><span class="sxs-lookup"><span data-stu-id="b0898-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="b0898-111">Det här kommandot får certifikat utfärdaren med namnet TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="b0898-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="b0898-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0898-112">PARAMETERS</span></span>

### <span data-ttu-id="b0898-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0898-113">-DefaultProfile</span></span>
<span data-ttu-id="b0898-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b0898-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0898-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="b0898-115">-Name</span></span>
<span data-ttu-id="b0898-116">Anger namnet på den certifikat utfärdare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="b0898-116">Specifies the name of the certificate issuer to get.</span></span>

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

### <span data-ttu-id="b0898-117">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b0898-117">-VaultName</span></span>
<span data-ttu-id="b0898-118">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="b0898-118">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="b0898-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0898-119">CommonParameters</span></span>
<span data-ttu-id="b0898-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0898-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0898-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0898-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0898-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0898-122">INPUTS</span></span>

## <span data-ttu-id="b0898-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0898-123">OUTPUTS</span></span>

### <span data-ttu-id="b0898-124">List<Microsoft. Azure. kommandon. KeyVaultCertificateIssuer. Models. CertificateIssuerIdentityItem>, Microsoft. Azure. kommandon.</span><span class="sxs-lookup"><span data-stu-id="b0898-124">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="b0898-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0898-125">NOTES</span></span>

## <span data-ttu-id="b0898-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0898-126">RELATED LINKS</span></span>

[<span data-ttu-id="b0898-127">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b0898-127">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="b0898-128">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b0898-128">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


