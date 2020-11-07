---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
ms.openlocfilehash: 51e7b941e5dbb4d07b48444196f6e3d3aa830452
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930237"
---
# <span data-ttu-id="08bda-101">Get-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08bda-101">Get-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="08bda-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08bda-102">SYNOPSIS</span></span>
<span data-ttu-id="08bda-103">Hämtar Key valv-hanterade Azure Storage-konton.</span><span class="sxs-lookup"><span data-stu-id="08bda-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08bda-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08bda-104">SYNTAX</span></span>

### <span data-ttu-id="08bda-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="08bda-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08bda-106">ByAccountName</span><span class="sxs-lookup"><span data-stu-id="08bda-106">ByAccountName</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08bda-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08bda-107">DESCRIPTION</span></span>
<span data-ttu-id="08bda-108">Hämtar ett nyckel valv hanterat Azure Storage-konto om namnet på kontot anges och konto nycklarna hanteras av det angivna valvet.</span><span class="sxs-lookup"><span data-stu-id="08bda-108">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="08bda-109">Om konto namnet inte anges visas alla konton vars nycklar hanteras av angivet valv.</span><span class="sxs-lookup"><span data-stu-id="08bda-109">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="08bda-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08bda-110">EXAMPLES</span></span>

### <span data-ttu-id="08bda-111">Exempel 1: lista alla hanterade lagrings konton för viktiga valv nycklar</span><span class="sxs-lookup"><span data-stu-id="08bda-111">Example 1: List all Key Vault managed Storage Accounts</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault'
```

<span data-ttu-id="08bda-112">Visar alla konton vars nycklar hanteras av valv ' Mina valv '</span><span class="sxs-lookup"><span data-stu-id="08bda-112">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="08bda-113">Exempel 2: Hämta ett hanterat lagrings konto för viktiga valv</span><span class="sxs-lookup"><span data-stu-id="08bda-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'
```

<span data-ttu-id="08bda-114">Hämtar information om Key valv Managed Storage-kontot för ' mystorageaccount ' om dess nycklar hanteras av valvet ' för valv '</span><span class="sxs-lookup"><span data-stu-id="08bda-114">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

## <span data-ttu-id="08bda-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08bda-115">PARAMETERS</span></span>

### <span data-ttu-id="08bda-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="08bda-116">-AccountName</span></span>
<span data-ttu-id="08bda-117">Namn på hanterat lagrings konto för viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="08bda-117">Key Vault managed storage account name.</span></span> <span data-ttu-id="08bda-118">Cmdlet konstruerar FQDN för ett hanterat lagrings konto namn från valv namn, valt miljö-och manged.</span><span class="sxs-lookup"><span data-stu-id="08bda-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bda-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08bda-119">-DefaultProfile</span></span>
<span data-ttu-id="08bda-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="08bda-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08bda-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="08bda-121">-VaultName</span></span>
<span data-ttu-id="08bda-122">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="08bda-122">Vault name.</span></span>
<span data-ttu-id="08bda-123">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="08bda-123">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="08bda-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08bda-124">CommonParameters</span></span>
<span data-ttu-id="08bda-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08bda-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08bda-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08bda-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08bda-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08bda-127">INPUTS</span></span>

### <span data-ttu-id="08bda-128">System. String</span><span class="sxs-lookup"><span data-stu-id="08bda-128">System.String</span></span>

## <span data-ttu-id="08bda-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08bda-129">OUTPUTS</span></span>

### <span data-ttu-id="08bda-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. 2.5.0.0. Models. ManagedStorageAccount, Microsoft. Azure. commands., version =, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="08bda-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="08bda-131">Microsoft. Azure. commands. valv. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08bda-131">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="08bda-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08bda-132">NOTES</span></span>

## <span data-ttu-id="08bda-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08bda-133">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

