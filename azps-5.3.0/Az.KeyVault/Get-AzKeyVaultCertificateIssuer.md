---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: d089cf44e14e70be8b377de310ab4a332ae2d1a1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523549"
---
# <span data-ttu-id="a732c-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="a732c-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="a732c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a732c-102">SYNOPSIS</span></span>
<span data-ttu-id="a732c-103">Hämtar en certifikat utfärdare för ett viktigt valv.</span><span class="sxs-lookup"><span data-stu-id="a732c-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="a732c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a732c-104">SYNTAX</span></span>

### <span data-ttu-id="a732c-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="a732c-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a732c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a732c-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a732c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a732c-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a732c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a732c-108">DESCRIPTION</span></span>
<span data-ttu-id="a732c-109">Cmdleten **Get-AzKeyVaultCertificateIssuer** hämtar en angiven certifikat utfärdare eller alla certifikat utfärdare för ett nyckeltal i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a732c-109">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="a732c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a732c-110">EXAMPLES</span></span>

### <span data-ttu-id="a732c-111">Exempel 1: skaffa en certifikat utfärdare</span><span class="sxs-lookup"><span data-stu-id="a732c-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="a732c-112">Det här kommandot får certifikat utfärdaren med namnet TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="a732c-112">This command gets the certificate issuer named TestIssuer01.</span></span>

### <span data-ttu-id="a732c-113">Exempel 2: Visa en lista med certifikat utfärdare med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="a732c-113">Example 2: List certificate issuers using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "test*"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer02
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="a732c-114">Det här kommandot får de certifikat utfärdare som börjar med "test".</span><span class="sxs-lookup"><span data-stu-id="a732c-114">This command gets the certificate issuers that start with "test".</span></span>

## <span data-ttu-id="a732c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a732c-115">PARAMETERS</span></span>

### <span data-ttu-id="a732c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a732c-116">-DefaultProfile</span></span>
<span data-ttu-id="a732c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a732c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a732c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a732c-118">-InputObject</span></span>
<span data-ttu-id="a732c-119">Valv objekt.</span><span class="sxs-lookup"><span data-stu-id="a732c-119">KeyVault object.</span></span>

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

### <span data-ttu-id="a732c-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="a732c-120">-Name</span></span>
<span data-ttu-id="a732c-121">Anger namnet på den certifikat utfärdare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="a732c-121">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="a732c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a732c-122">-ResourceId</span></span>
<span data-ttu-id="a732c-123">Resurs-ID för valv.</span><span class="sxs-lookup"><span data-stu-id="a732c-123">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="a732c-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a732c-124">-VaultName</span></span>
<span data-ttu-id="a732c-125">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="a732c-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="a732c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a732c-126">CommonParameters</span></span>
<span data-ttu-id="a732c-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a732c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a732c-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a732c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a732c-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a732c-129">INPUTS</span></span>

### <span data-ttu-id="a732c-130">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a732c-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="a732c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a732c-131">System.String</span></span>

## <span data-ttu-id="a732c-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a732c-132">OUTPUTS</span></span>

### <span data-ttu-id="a732c-133">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a732c-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="a732c-134">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="a732c-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="a732c-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a732c-135">NOTES</span></span>

## <span data-ttu-id="a732c-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a732c-136">RELATED LINKS</span></span>

[<span data-ttu-id="a732c-137">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="a732c-137">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="a732c-138">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="a732c-138">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


