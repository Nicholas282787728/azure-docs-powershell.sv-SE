---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 31619366c1d2a1a025cb7ff563a04b166abb2a46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757083"
---
# <span data-ttu-id="d9155-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="d9155-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="d9155-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9155-102">SYNOPSIS</span></span>
<span data-ttu-id="d9155-103">Hämtar kontakter som är registrerade för certifikat aviseringar för ett viktigt valv.</span><span class="sxs-lookup"><span data-stu-id="d9155-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9155-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9155-104">SYNTAX</span></span>

### <span data-ttu-id="d9155-105">VaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="d9155-105">VaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d9155-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d9155-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d9155-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d9155-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9155-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9155-108">DESCRIPTION</span></span>
<span data-ttu-id="d9155-109">Cmdleten **Get-AzureKeyVaultCertificateContact** hämtar kontakter som är registrerade för certifikat aviseringar för ett huvud valv i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="d9155-109">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="d9155-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9155-110">EXAMPLES</span></span>

### <span data-ttu-id="d9155-111">Exempel 1: Hämta alla certifikat kontakter</span><span class="sxs-lookup"><span data-stu-id="d9155-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="d9155-112">Det här kommandot får alla kontakter för certifikat objekt i ett contoso-valv och lagrar dem sedan i $Contacts variabel.</span><span class="sxs-lookup"><span data-stu-id="d9155-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="d9155-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9155-113">PARAMETERS</span></span>

### <span data-ttu-id="d9155-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9155-114">-DefaultProfile</span></span>
<span data-ttu-id="d9155-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d9155-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9155-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9155-116">-InputObject</span></span>
<span data-ttu-id="d9155-117">Valv objekt.</span><span class="sxs-lookup"><span data-stu-id="d9155-117">KeyVault object.</span></span>

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

### <span data-ttu-id="d9155-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9155-118">-ResourceId</span></span>
<span data-ttu-id="d9155-119">ID för valv.</span><span class="sxs-lookup"><span data-stu-id="d9155-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="d9155-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d9155-120">-VaultName</span></span>
<span data-ttu-id="d9155-121">Anger namnet på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="d9155-121">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9155-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9155-122">CommonParameters</span></span>
<span data-ttu-id="d9155-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9155-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9155-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9155-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9155-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9155-125">INPUTS</span></span>

### <span data-ttu-id="d9155-126">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d9155-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="d9155-127">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d9155-127">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="d9155-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d9155-128">System.String</span></span>

## <span data-ttu-id="d9155-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9155-129">OUTPUTS</span></span>

### <span data-ttu-id="d9155-130">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="d9155-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="d9155-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9155-131">NOTES</span></span>

## <span data-ttu-id="d9155-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9155-132">RELATED LINKS</span></span>

[<span data-ttu-id="d9155-133">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="d9155-133">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="d9155-134">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="d9155-134">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

