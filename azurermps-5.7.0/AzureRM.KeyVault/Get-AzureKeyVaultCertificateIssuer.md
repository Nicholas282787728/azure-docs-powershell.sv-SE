---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: f19fa119bf307724fb318e0a1d9a390190523bd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575644"
---
# <span data-ttu-id="48fa6-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="48fa6-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="48fa6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48fa6-102">SYNOPSIS</span></span>
<span data-ttu-id="48fa6-103">Hämtar en certifikat utfärdare för ett viktigt valv.</span><span class="sxs-lookup"><span data-stu-id="48fa6-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48fa6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48fa6-104">SYNTAX</span></span>

### <span data-ttu-id="48fa6-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="48fa6-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48fa6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="48fa6-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48fa6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48fa6-107">DESCRIPTION</span></span>
<span data-ttu-id="48fa6-108">Cmdleten **Get-AzureKeyVaultCertificateIssuer** hämtar en angiven certifikat utfärdare eller alla certifikat utfärdare för ett nyckeltal i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="48fa6-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="48fa6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48fa6-109">EXAMPLES</span></span>

### <span data-ttu-id="48fa6-110">Exempel 1: skaffa en certifikat utfärdare</span><span class="sxs-lookup"><span data-stu-id="48fa6-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="48fa6-111">Det här kommandot får certifikat utfärdaren med namnet TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="48fa6-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="48fa6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48fa6-112">PARAMETERS</span></span>

### <span data-ttu-id="48fa6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48fa6-113">-DefaultProfile</span></span>
<span data-ttu-id="48fa6-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="48fa6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48fa6-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48fa6-115">-InputObject</span></span>
<span data-ttu-id="48fa6-116">Valv objekt.</span><span class="sxs-lookup"><span data-stu-id="48fa6-116">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48fa6-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="48fa6-117">-Name</span></span>
<span data-ttu-id="48fa6-118">Anger namnet på den certifikat utfärdare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="48fa6-118">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48fa6-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="48fa6-119">-VaultName</span></span>
<span data-ttu-id="48fa6-120">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="48fa6-120">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48fa6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48fa6-121">CommonParameters</span></span>
<span data-ttu-id="48fa6-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48fa6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48fa6-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48fa6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48fa6-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48fa6-124">INPUTS</span></span>

### <span data-ttu-id="48fa6-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="48fa6-125">None</span></span>
<span data-ttu-id="48fa6-126">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="48fa6-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="48fa6-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48fa6-127">OUTPUTS</span></span>

### <span data-ttu-id="48fa6-128">List<Microsoft. Azure. kommandon. PSKeyVaultCertificateIssuer. Models. PSKeyVaultCertificateIssuerIdentityItem>, Microsoft. Azure. kommandon.</span><span class="sxs-lookup"><span data-stu-id="48fa6-128">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="48fa6-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48fa6-129">NOTES</span></span>

## <span data-ttu-id="48fa6-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48fa6-130">RELATED LINKS</span></span>

[<span data-ttu-id="48fa6-131">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="48fa6-131">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="48fa6-132">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="48fa6-132">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


