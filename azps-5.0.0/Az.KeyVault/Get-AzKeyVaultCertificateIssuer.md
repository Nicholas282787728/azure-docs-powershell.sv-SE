---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 1504d4f18c8ab3baee000c2cf8d873df1dd9a177
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273457"
---
# <span data-ttu-id="c9069-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="c9069-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="c9069-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c9069-102">SYNOPSIS</span></span>
<span data-ttu-id="c9069-103">Hämtar en certifikat utfärdare för ett viktigt valv.</span><span class="sxs-lookup"><span data-stu-id="c9069-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="c9069-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c9069-104">SYNTAX</span></span>

### <span data-ttu-id="c9069-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="c9069-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9069-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c9069-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9069-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c9069-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9069-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c9069-108">DESCRIPTION</span></span>
<span data-ttu-id="c9069-109">Cmdleten **Get-AzKeyVaultCertificateIssuer** hämtar en angiven certifikat utfärdare eller alla certifikat utfärdare för ett nyckeltal i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="c9069-109">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="c9069-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c9069-110">EXAMPLES</span></span>

### <span data-ttu-id="c9069-111">Exempel 1: skaffa en certifikat utfärdare</span><span class="sxs-lookup"><span data-stu-id="c9069-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="c9069-112">Det här kommandot får certifikat utfärdaren med namnet TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="c9069-112">This command gets the certificate issuer named TestIssuer01.</span></span>

### <span data-ttu-id="c9069-113">Exempel 2: Visa en lista med certifikat utfärdare med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="c9069-113">Example 2: List certificate issuers using filtering</span></span>
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

<span data-ttu-id="c9069-114">Det här kommandot får de certifikat utfärdare som börjar med "test".</span><span class="sxs-lookup"><span data-stu-id="c9069-114">This command gets the certificate issuers that start with "test".</span></span>

## <span data-ttu-id="c9069-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c9069-115">PARAMETERS</span></span>

### <span data-ttu-id="c9069-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9069-116">-DefaultProfile</span></span>
<span data-ttu-id="c9069-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c9069-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9069-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9069-118">-InputObject</span></span>
<span data-ttu-id="c9069-119">Valv objekt.</span><span class="sxs-lookup"><span data-stu-id="c9069-119">KeyVault object.</span></span>

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

### <span data-ttu-id="c9069-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="c9069-120">-Name</span></span>
<span data-ttu-id="c9069-121">Anger namnet på den certifikat utfärdare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="c9069-121">Specifies the name of the certificate issuer to get.</span></span>

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

### <span data-ttu-id="c9069-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9069-122">-ResourceId</span></span>
<span data-ttu-id="c9069-123">Resurs-ID för valv.</span><span class="sxs-lookup"><span data-stu-id="c9069-123">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="c9069-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c9069-124">-VaultName</span></span>
<span data-ttu-id="c9069-125">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="c9069-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="c9069-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9069-126">CommonParameters</span></span>
<span data-ttu-id="c9069-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9069-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9069-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9069-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9069-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c9069-129">INPUTS</span></span>

### <span data-ttu-id="c9069-130">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="c9069-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="c9069-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c9069-131">System.String</span></span>

## <span data-ttu-id="c9069-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c9069-132">OUTPUTS</span></span>

### <span data-ttu-id="c9069-133">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c9069-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="c9069-134">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="c9069-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="c9069-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c9069-135">NOTES</span></span>

## <span data-ttu-id="c9069-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c9069-136">RELATED LINKS</span></span>

[<span data-ttu-id="c9069-137">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="c9069-137">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="c9069-138">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="c9069-138">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


