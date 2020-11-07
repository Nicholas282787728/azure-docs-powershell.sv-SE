---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 70ee1aaf9fb082819c626c43ba5c08ad01f0f1d6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924470"
---
# <span data-ttu-id="e7b4a-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e7b4a-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="e7b4a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e7b4a-102">SYNOPSIS</span></span>
<span data-ttu-id="e7b4a-103">Hämtar Key valv-hanterade Azure Storage-konton.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="e7b4a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e7b4a-104">SYNTAX</span></span>

### <span data-ttu-id="e7b4a-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="e7b4a-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7b4a-106">ByAccountName</span><span class="sxs-lookup"><span data-stu-id="e7b4a-106">ByAccountName</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7b4a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e7b4a-107">DESCRIPTION</span></span>
<span data-ttu-id="e7b4a-108">Hämtar ett nyckel valv hanterat Azure Storage-konto om namnet på kontot anges och konto nycklarna hanteras av det angivna valvet.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-108">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="e7b4a-109">Om konto namnet inte anges visas alla konton vars nycklar hanteras av angivet valv.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-109">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="e7b4a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e7b4a-110">EXAMPLES</span></span>

### <span data-ttu-id="e7b4a-111">Exempel 1: lista alla hanterade lagrings konton för viktiga valv nycklar</span><span class="sxs-lookup"><span data-stu-id="e7b4a-111">Example 1: List all Key Vault managed Storage Accounts</span></span>
```
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault'
```

<span data-ttu-id="e7b4a-112">Visar alla konton vars nycklar hanteras av valv ' Mina valv '</span><span class="sxs-lookup"><span data-stu-id="e7b4a-112">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="e7b4a-113">Exempel 2: Hämta ett hanterat lagrings konto för viktiga valv</span><span class="sxs-lookup"><span data-stu-id="e7b4a-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'
```

<span data-ttu-id="e7b4a-114">Hämtar information om Key valv Managed Storage-kontot för ' mystorageaccount ' om dess nycklar hanteras av valvet ' för valv '</span><span class="sxs-lookup"><span data-stu-id="e7b4a-114">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

## <span data-ttu-id="e7b4a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e7b4a-115">PARAMETERS</span></span>

### <span data-ttu-id="e7b4a-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e7b4a-116">-AccountName</span></span>
<span data-ttu-id="e7b4a-117">Namn på hanterat lagrings konto för viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-117">Key Vault managed storage account name.</span></span> <span data-ttu-id="e7b4a-118">Cmdlet konstruerar FQDN för ett hanterat lagrings konto namn från valv namn, valt miljö-och manged.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="e7b4a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7b4a-119">-DefaultProfile</span></span>
<span data-ttu-id="e7b4a-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e7b4a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7b4a-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e7b4a-121">-VaultName</span></span>
<span data-ttu-id="e7b4a-122">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-122">Vault name.</span></span>
<span data-ttu-id="e7b4a-123">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-123">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e7b4a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7b4a-124">CommonParameters</span></span>
<span data-ttu-id="e7b4a-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7b4a-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7b4a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7b4a-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e7b4a-127">INPUTS</span></span>

### <span data-ttu-id="e7b4a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e7b4a-128">System.String</span></span>

## <span data-ttu-id="e7b4a-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e7b4a-129">OUTPUTS</span></span>

### <span data-ttu-id="e7b4a-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. 2.5.0.0. Models. ManagedStorageAccount, Microsoft. Azure. commands., version =, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e7b4a-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="e7b4a-131">Microsoft. Azure. commands. valv. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e7b4a-131">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="e7b4a-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e7b4a-132">NOTES</span></span>

## <span data-ttu-id="e7b4a-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e7b4a-133">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

