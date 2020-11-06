---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 66c5e949cca8a6f53fdbac89e2745ac7697e14ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583303"
---
# <span data-ttu-id="40241-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="40241-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="40241-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40241-102">SYNOPSIS</span></span>
<span data-ttu-id="40241-103">Hämtar en certifikat utfärdare för ett viktigt valv.</span><span class="sxs-lookup"><span data-stu-id="40241-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40241-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40241-104">SYNTAX</span></span>

### <span data-ttu-id="40241-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="40241-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="40241-106">ByName</span><span class="sxs-lookup"><span data-stu-id="40241-106">ByName</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40241-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40241-107">DESCRIPTION</span></span>
<span data-ttu-id="40241-108">Cmdleten **Get-AzureKeyVaultCertificateIssuer** hämtar en angiven certifikat utfärdare eller alla certifikat utfärdare för ett nyckeltal i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="40241-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="40241-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40241-109">EXAMPLES</span></span>

### <span data-ttu-id="40241-110">Exempel 1: skaffa en certifikat utfärdare</span><span class="sxs-lookup"><span data-stu-id="40241-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="40241-111">Det här kommandot får certifikat utfärdaren med namnet TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="40241-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="40241-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40241-112">PARAMETERS</span></span>

### <span data-ttu-id="40241-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="40241-113">-Name</span></span>
<span data-ttu-id="40241-114">Anger namnet på den certifikat utfärdare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="40241-114">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40241-115">-VaultName</span><span class="sxs-lookup"><span data-stu-id="40241-115">-VaultName</span></span>
<span data-ttu-id="40241-116">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="40241-116">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="40241-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40241-117">-DefaultProfile</span></span>
<span data-ttu-id="40241-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="40241-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40241-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40241-119">CommonParameters</span></span>
<span data-ttu-id="40241-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40241-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40241-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40241-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40241-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40241-122">INPUTS</span></span>

## <span data-ttu-id="40241-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40241-123">OUTPUTS</span></span>

### <span data-ttu-id="40241-124">List<Microsoft. Azure. kommandon. KeyVaultCertificateIssuer. Models. CertificateIssuerIdentityItem>, Microsoft. Azure. kommandon.</span><span class="sxs-lookup"><span data-stu-id="40241-124">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="40241-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40241-125">NOTES</span></span>

## <span data-ttu-id="40241-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40241-126">RELATED LINKS</span></span>

[<span data-ttu-id="40241-127">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="40241-127">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="40241-128">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="40241-128">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


