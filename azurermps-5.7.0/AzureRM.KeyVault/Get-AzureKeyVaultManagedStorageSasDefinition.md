---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 7606293338e6467247e257f34e6850f52b67a1c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756504"
---
# <span data-ttu-id="9e2c4-101">Get-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="9e2c4-101">Get-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="9e2c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e2c4-102">SYNOPSIS</span></span>
<span data-ttu-id="9e2c4-103">Hämtar SAS-definitioner för hanterade nycklar för viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="9e2c4-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e2c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e2c4-104">SYNTAX</span></span>

### <span data-ttu-id="9e2c4-105">ByAccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="9e2c4-105">ByAccountName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e2c4-106">ByDefinitionName</span><span class="sxs-lookup"><span data-stu-id="9e2c4-106">ByDefinitionName</span></span>
```
Get-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e2c4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e2c4-107">DESCRIPTION</span></span>
<span data-ttu-id="9e2c4-108">Hämtar en säkerhets beskrivning för Managed Storage för viktiga nycklar om namnet på definitionen anges.</span><span class="sxs-lookup"><span data-stu-id="9e2c4-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="9e2c4-109">Om du inte anger något definitions namn visas alla SAS-definitioner som är kopplade till det angivna lagrings kontot för Key valv som hanteras i valvet.</span><span class="sxs-lookup"><span data-stu-id="9e2c4-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="9e2c4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e2c4-110">EXAMPLES</span></span>

### <span data-ttu-id="9e2c4-111">Exempel 1: lista alla sa-definitioner för hanterade nycklar</span><span class="sxs-lookup"><span data-stu-id="9e2c4-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="9e2c4-112">Visar en lista över alla SAS-definitioner som är associerade med Key valv Managed Storage Account ' mystorageaccount ' som hanteras av valv ' online Vault '</span><span class="sxs-lookup"><span data-stu-id="9e2c4-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="9e2c4-113">Exempel 2: Hämta ett hanterat lagrings konto för viktiga valv</span><span class="sxs-lookup"><span data-stu-id="9e2c4-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasDef'
```

<span data-ttu-id="9e2c4-114">Hämtar information om SAS-definitionen ' mysasDef ' som är associerad med Key valv Managed Storage-konto ' mystorageaccount ' som hanteras av valv ' The valv '.</span><span class="sxs-lookup"><span data-stu-id="9e2c4-114">Gets the details of SAS Definition 'mysasDef' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

## <span data-ttu-id="9e2c4-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e2c4-115">PARAMETERS</span></span>

### <span data-ttu-id="9e2c4-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9e2c4-116">-AccountName</span></span>
<span data-ttu-id="9e2c4-117">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="9e2c4-117">Vault name.</span></span>
<span data-ttu-id="9e2c4-118">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="9e2c4-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e2c4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e2c4-119">-DefaultProfile</span></span>
<span data-ttu-id="9e2c4-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9e2c4-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e2c4-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="9e2c4-121">-Name</span></span>
<span data-ttu-id="9e2c4-122">Namn på lagrings-sa.</span><span class="sxs-lookup"><span data-stu-id="9e2c4-122">Storage sas definition name.</span></span>
<span data-ttu-id="9e2c4-123">Cmdlet konstruerar FQDN-namnet på en lagrings-säkerhets Association från ett valv namn, för närvarande valda miljö-, lagrings konto namn och SAS-namn.</span><span class="sxs-lookup"><span data-stu-id="9e2c4-123">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: ByDefinitionName
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e2c4-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9e2c4-124">-VaultName</span></span>
<span data-ttu-id="9e2c4-125">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="9e2c4-125">Vault name.</span></span>
<span data-ttu-id="9e2c4-126">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="9e2c4-126">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="9e2c4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e2c4-127">CommonParameters</span></span>
<span data-ttu-id="9e2c4-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e2c4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e2c4-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e2c4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e2c4-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e2c4-130">INPUTS</span></span>

### <span data-ttu-id="9e2c4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9e2c4-131">System.String</span></span>

## <span data-ttu-id="9e2c4-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e2c4-132">OUTPUTS</span></span>

### <span data-ttu-id="9e2c4-133">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. 2.5.0.0. Models. ManagedStorageSasDefinitionListItem, Microsoft. Azure. commands., version =, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9e2c4-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinitionListItem, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="9e2c4-134">Microsoft. Azure. commands. valv. Models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="9e2c4-134">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="9e2c4-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e2c4-135">NOTES</span></span>

## <span data-ttu-id="9e2c4-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e2c4-136">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

