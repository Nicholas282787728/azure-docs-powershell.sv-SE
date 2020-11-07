---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 6a59b49da2ae283af50487bec21da6c1d2457878
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757290"
---
# <span data-ttu-id="fb54b-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="fb54b-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="fb54b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb54b-102">SYNOPSIS</span></span>
<span data-ttu-id="fb54b-103">Hämtar kontakter som är registrerade för certifikat aviseringar för ett viktigt valv.</span><span class="sxs-lookup"><span data-stu-id="fb54b-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb54b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb54b-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb54b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb54b-105">DESCRIPTION</span></span>
<span data-ttu-id="fb54b-106">Cmdleten **Get-AzureKeyVaultCertificateContact** hämtar kontakter som är registrerade för certifikat aviseringar för ett huvud valv i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="fb54b-106">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="fb54b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb54b-107">EXAMPLES</span></span>

### <span data-ttu-id="fb54b-108">Exempel 1: Hämta alla certifikat kontakter</span><span class="sxs-lookup"><span data-stu-id="fb54b-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="fb54b-109">Det här kommandot får alla kontakter för certifikat objekt i ett contoso-valv och lagrar dem sedan i $Contacts variabel.</span><span class="sxs-lookup"><span data-stu-id="fb54b-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="fb54b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb54b-110">PARAMETERS</span></span>

### <span data-ttu-id="fb54b-111">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fb54b-111">-VaultName</span></span>
<span data-ttu-id="fb54b-112">Anger namnet på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="fb54b-112">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="fb54b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb54b-113">-DefaultProfile</span></span>
<span data-ttu-id="fb54b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fb54b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb54b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb54b-115">CommonParameters</span></span>
<span data-ttu-id="fb54b-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb54b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb54b-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb54b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb54b-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb54b-118">INPUTS</span></span>

## <span data-ttu-id="fb54b-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb54b-119">OUTPUTS</span></span>

### <span data-ttu-id="fb54b-120">List<Microsoft. Azure.-kommandon. valv. KeyVaultCertificateContact-></span><span class="sxs-lookup"><span data-stu-id="fb54b-120">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="fb54b-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb54b-121">NOTES</span></span>

## <span data-ttu-id="fb54b-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb54b-122">RELATED LINKS</span></span>

[<span data-ttu-id="fb54b-123">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="fb54b-123">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="fb54b-124">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="fb54b-124">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

