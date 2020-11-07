---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 15e11e9deedbc8a2e442d9b3f006511a98fd6394
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922725"
---
# <span data-ttu-id="96129-101">Get-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="96129-101">Get-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="96129-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96129-102">SYNOPSIS</span></span>
<span data-ttu-id="96129-103">Hämtar SAS-definitioner för hanterade nycklar för viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="96129-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

## <span data-ttu-id="96129-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96129-104">SYNTAX</span></span>

### <span data-ttu-id="96129-105">ByAccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="96129-105">ByAccountName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96129-106">ByDefinitionName</span><span class="sxs-lookup"><span data-stu-id="96129-106">ByDefinitionName</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96129-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96129-107">DESCRIPTION</span></span>
<span data-ttu-id="96129-108">Hämtar en säkerhets beskrivning för Managed Storage för viktiga nycklar om namnet på definitionen anges.</span><span class="sxs-lookup"><span data-stu-id="96129-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="96129-109">Om du inte anger något definitions namn visas alla SAS-definitioner som är kopplade till det angivna lagrings kontot för Key valv som hanteras i valvet.</span><span class="sxs-lookup"><span data-stu-id="96129-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="96129-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96129-110">EXAMPLES</span></span>

### <span data-ttu-id="96129-111">Exempel 1: lista alla sa-definitioner för hanterade nycklar</span><span class="sxs-lookup"><span data-stu-id="96129-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="96129-112">Visar en lista över alla SAS-definitioner som är associerade med Key valv Managed Storage Account ' mystorageaccount ' som hanteras av valv ' online Vault '</span><span class="sxs-lookup"><span data-stu-id="96129-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="96129-113">Exempel 2: Hämta ett hanterat lagrings konto för viktiga valv</span><span class="sxs-lookup"><span data-stu-id="96129-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasDef'
```

<span data-ttu-id="96129-114">Hämtar information om SAS-definitionen ' mysasDef ' som är associerad med Key valv Managed Storage-konto ' mystorageaccount ' som hanteras av valv ' The valv '.</span><span class="sxs-lookup"><span data-stu-id="96129-114">Gets the details of SAS Definition 'mysasDef' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

## <span data-ttu-id="96129-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96129-115">PARAMETERS</span></span>

### <span data-ttu-id="96129-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="96129-116">-AccountName</span></span>
<span data-ttu-id="96129-117">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="96129-117">Vault name.</span></span>
<span data-ttu-id="96129-118">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="96129-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="96129-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96129-119">-DefaultProfile</span></span>
<span data-ttu-id="96129-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="96129-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96129-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="96129-121">-Name</span></span>
<span data-ttu-id="96129-122">Namn på lagrings-sa.</span><span class="sxs-lookup"><span data-stu-id="96129-122">Storage sas definition name.</span></span>
<span data-ttu-id="96129-123">Cmdlet konstruerar FQDN-namnet på en lagrings-säkerhets Association från ett valv namn, för närvarande valda miljö-, lagrings konto namn och SAS-namn.</span><span class="sxs-lookup"><span data-stu-id="96129-123">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="96129-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="96129-124">-VaultName</span></span>
<span data-ttu-id="96129-125">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="96129-125">Vault name.</span></span>
<span data-ttu-id="96129-126">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="96129-126">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="96129-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96129-127">CommonParameters</span></span>
<span data-ttu-id="96129-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96129-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96129-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96129-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96129-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96129-130">INPUTS</span></span>

### <span data-ttu-id="96129-131">System. String</span><span class="sxs-lookup"><span data-stu-id="96129-131">System.String</span></span>

## <span data-ttu-id="96129-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96129-132">OUTPUTS</span></span>

### <span data-ttu-id="96129-133">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. 2.5.0.0. Models. ManagedStorageSasDefinitionListItem, Microsoft. Azure. commands., version =, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="96129-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinitionListItem, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="96129-134">Microsoft. Azure. commands. valv. Models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="96129-134">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="96129-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96129-135">NOTES</span></span>

## <span data-ttu-id="96129-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96129-136">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

