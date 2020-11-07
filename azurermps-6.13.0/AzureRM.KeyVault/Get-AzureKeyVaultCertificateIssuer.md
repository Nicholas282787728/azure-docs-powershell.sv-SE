---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 83e81e479807c3eada25456d53521dfcecd81f40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757082"
---
# <span data-ttu-id="80b58-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="80b58-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="80b58-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="80b58-102">SYNOPSIS</span></span>
<span data-ttu-id="80b58-103">Hämtar en certifikat utfärdare för ett viktigt valv.</span><span class="sxs-lookup"><span data-stu-id="80b58-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80b58-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="80b58-104">SYNTAX</span></span>

### <span data-ttu-id="80b58-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="80b58-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80b58-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="80b58-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80b58-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="80b58-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80b58-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="80b58-108">DESCRIPTION</span></span>
<span data-ttu-id="80b58-109">Cmdleten **Get-AzureKeyVaultCertificateIssuer** hämtar en angiven certifikat utfärdare eller alla certifikat utfärdare för ett nyckeltal i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="80b58-109">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="80b58-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="80b58-110">EXAMPLES</span></span>

### <span data-ttu-id="80b58-111">Exempel 1: skaffa en certifikat utfärdare</span><span class="sxs-lookup"><span data-stu-id="80b58-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="80b58-112">Det här kommandot får certifikat utfärdaren med namnet TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="80b58-112">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="80b58-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="80b58-113">PARAMETERS</span></span>

### <span data-ttu-id="80b58-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80b58-114">-DefaultProfile</span></span>
<span data-ttu-id="80b58-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="80b58-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80b58-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80b58-116">-InputObject</span></span>
<span data-ttu-id="80b58-117">Valv objekt.</span><span class="sxs-lookup"><span data-stu-id="80b58-117">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80b58-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="80b58-118">-Name</span></span>
<span data-ttu-id="80b58-119">Anger namnet på den certifikat utfärdare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="80b58-119">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b58-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80b58-120">-ResourceId</span></span>
<span data-ttu-id="80b58-121">Resurs-ID för valv.</span><span class="sxs-lookup"><span data-stu-id="80b58-121">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80b58-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="80b58-122">-VaultName</span></span>
<span data-ttu-id="80b58-123">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="80b58-123">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b58-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80b58-124">CommonParameters</span></span>
<span data-ttu-id="80b58-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80b58-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80b58-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80b58-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80b58-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="80b58-127">INPUTS</span></span>

### <span data-ttu-id="80b58-128">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="80b58-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="80b58-129">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="80b58-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="80b58-130">System. String</span><span class="sxs-lookup"><span data-stu-id="80b58-130">System.String</span></span>

## <span data-ttu-id="80b58-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="80b58-131">OUTPUTS</span></span>

### <span data-ttu-id="80b58-132">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="80b58-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="80b58-133">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="80b58-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="80b58-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="80b58-134">NOTES</span></span>

## <span data-ttu-id="80b58-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="80b58-135">RELATED LINKS</span></span>

[<span data-ttu-id="80b58-136">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="80b58-136">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="80b58-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="80b58-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


