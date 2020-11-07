---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
ms.openlocfilehash: d6d2070afcb4a5b9b0b13af1fa54dc93621c5a97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929874"
---
# <span data-ttu-id="8a2b4-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8a2b4-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="8a2b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a2b4-102">SYNOPSIS</span></span>
<span data-ttu-id="8a2b4-103">Hämtar kontakter som är registrerade för certifikat aviseringar för ett viktigt valv.</span><span class="sxs-lookup"><span data-stu-id="8a2b4-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a2b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a2b4-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a2b4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a2b4-105">DESCRIPTION</span></span>
<span data-ttu-id="8a2b4-106">Cmdleten **Get-AzureKeyVaultCertificateContact** hämtar kontakter som är registrerade för certifikat aviseringar för ett huvud valv i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="8a2b4-106">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="8a2b4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a2b4-107">EXAMPLES</span></span>

### <span data-ttu-id="8a2b4-108">Exempel 1: Hämta alla certifikat kontakter</span><span class="sxs-lookup"><span data-stu-id="8a2b4-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="8a2b4-109">Det här kommandot får alla kontakter för certifikat objekt i ett contoso-valv och lagrar dem sedan i $Contacts variabel.</span><span class="sxs-lookup"><span data-stu-id="8a2b4-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="8a2b4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a2b4-110">PARAMETERS</span></span>

### <span data-ttu-id="8a2b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a2b4-111">-DefaultProfile</span></span>
<span data-ttu-id="8a2b4-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8a2b4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a2b4-113">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8a2b4-113">-VaultName</span></span>
<span data-ttu-id="8a2b4-114">Anger namnet på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="8a2b4-114">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="8a2b4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a2b4-115">CommonParameters</span></span>
<span data-ttu-id="8a2b4-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a2b4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a2b4-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a2b4-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a2b4-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a2b4-118">INPUTS</span></span>

## <span data-ttu-id="8a2b4-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a2b4-119">OUTPUTS</span></span>

### <span data-ttu-id="8a2b4-120">List<Microsoft. Azure.-kommandon. valv. KeyVaultCertificateContact-></span><span class="sxs-lookup"><span data-stu-id="8a2b4-120">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="8a2b4-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a2b4-121">NOTES</span></span>

## <span data-ttu-id="8a2b4-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a2b4-122">RELATED LINKS</span></span>

[<span data-ttu-id="8a2b4-123">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8a2b4-123">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="8a2b4-124">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8a2b4-124">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

