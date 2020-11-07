---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: e02b60055818d1ed79e93e6853353795e78c5830
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922745"
---
# <span data-ttu-id="52309-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="52309-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="52309-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52309-102">SYNOPSIS</span></span>
<span data-ttu-id="52309-103">Hämtar kontakter som är registrerade för certifikat aviseringar för ett viktigt valv.</span><span class="sxs-lookup"><span data-stu-id="52309-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="52309-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52309-104">SYNTAX</span></span>

```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52309-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52309-105">DESCRIPTION</span></span>
<span data-ttu-id="52309-106">Cmdleten **Get-AzKeyVaultCertificateContact** hämtar kontakter som är registrerade för certifikat aviseringar för ett huvud valv i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="52309-106">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="52309-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52309-107">EXAMPLES</span></span>

### <span data-ttu-id="52309-108">Exempel 1: Hämta alla certifikat kontakter</span><span class="sxs-lookup"><span data-stu-id="52309-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="52309-109">Det här kommandot får alla kontakter för certifikat objekt i ett contoso-valv och lagrar dem sedan i $Contacts variabel.</span><span class="sxs-lookup"><span data-stu-id="52309-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="52309-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52309-110">PARAMETERS</span></span>

### <span data-ttu-id="52309-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52309-111">-DefaultProfile</span></span>
<span data-ttu-id="52309-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="52309-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52309-113">-VaultName</span><span class="sxs-lookup"><span data-stu-id="52309-113">-VaultName</span></span>
<span data-ttu-id="52309-114">Anger namnet på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="52309-114">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="52309-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52309-115">CommonParameters</span></span>
<span data-ttu-id="52309-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52309-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52309-117">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52309-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52309-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52309-118">INPUTS</span></span>

### <span data-ttu-id="52309-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="52309-119">None</span></span>
<span data-ttu-id="52309-120">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="52309-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="52309-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52309-121">OUTPUTS</span></span>

### <span data-ttu-id="52309-122">List<Microsoft. Azure.-kommandon. valv. KeyVaultCertificateContact-></span><span class="sxs-lookup"><span data-stu-id="52309-122">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="52309-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52309-123">NOTES</span></span>

## <span data-ttu-id="52309-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52309-124">RELATED LINKS</span></span>

[<span data-ttu-id="52309-125">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="52309-125">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="52309-126">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="52309-126">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

