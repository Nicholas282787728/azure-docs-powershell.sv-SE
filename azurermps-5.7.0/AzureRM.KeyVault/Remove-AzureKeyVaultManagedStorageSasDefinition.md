---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 9859c6f17f393a5ca691c34e3ee144e24ab59fa8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756087"
---
# <span data-ttu-id="21b51-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="21b51-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="21b51-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="21b51-102">SYNOPSIS</span></span>
<span data-ttu-id="21b51-103">Tar bort en Key valv Managed-definitioner för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="21b51-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21b51-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="21b51-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21b51-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="21b51-105">DESCRIPTION</span></span>
<span data-ttu-id="21b51-106">Tar bort en Key valv Managed-definitioner för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="21b51-106">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="21b51-107">Detta tar också bort hemligheten som används för att hämta SAS-token per denna säkerhets Association.</span><span class="sxs-lookup"><span data-stu-id="21b51-107">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="21b51-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="21b51-108">EXAMPLES</span></span>

### <span data-ttu-id="21b51-109">Exempel 1: ta bort en Key valv Managed definition för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="21b51-109">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef'
```

<span data-ttu-id="21b51-110">Tar bort säkerhets associationer för Managed Storage mysasdef associerat med kontot ' mystorageaccount ' i valv för valvet.</span><span class="sxs-lookup"><span data-stu-id="21b51-110">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="21b51-111">Exempel 2: ta bort en Key valv Managed definition av Azure-lagring utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="21b51-111">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -Force -Confirm:$False
```

<span data-ttu-id="21b51-112">Tar bort säkerhets associationer för Managed Storage mysasdef associerat med kontot ' mystorageaccount ' i valv för valvet.</span><span class="sxs-lookup"><span data-stu-id="21b51-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="21b51-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="21b51-113">PARAMETERS</span></span>

### <span data-ttu-id="21b51-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="21b51-114">-AccountName</span></span>
<span data-ttu-id="21b51-115">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="21b51-115">Storage account name.</span></span>
<span data-ttu-id="21b51-116">Cmdlet konstruerar FQDN för ett hanterat lagrings konto namn från ett valv namn, valt miljö-och lagrings konto namn.</span><span class="sxs-lookup"><span data-stu-id="21b51-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

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

### <span data-ttu-id="21b51-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21b51-117">-DefaultProfile</span></span>
<span data-ttu-id="21b51-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="21b51-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21b51-119">-Force</span><span class="sxs-lookup"><span data-stu-id="21b51-119">-Force</span></span>
<span data-ttu-id="21b51-120">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="21b51-120">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21b51-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="21b51-121">-Name</span></span>
<span data-ttu-id="21b51-122">Namn på lagrings-sa.</span><span class="sxs-lookup"><span data-stu-id="21b51-122">Storage sas definition name.</span></span>
<span data-ttu-id="21b51-123">Cmdlet konstruerar FQDN-namnet på en lagrings-säkerhets Association från ett valv namn, för närvarande valda miljö-, lagrings konto namn och SAS-namn.</span><span class="sxs-lookup"><span data-stu-id="21b51-123">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21b51-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21b51-124">-PassThru</span></span>
<span data-ttu-id="21b51-125">Cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="21b51-125">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="21b51-126">Om denna växel anges returnerar cmdlet det hanterade lagrings konto som har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="21b51-126">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21b51-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="21b51-127">-VaultName</span></span>
<span data-ttu-id="21b51-128">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="21b51-128">Vault name.</span></span>
<span data-ttu-id="21b51-129">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="21b51-129">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="21b51-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="21b51-130">-Confirm</span></span>
<span data-ttu-id="21b51-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="21b51-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21b51-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21b51-132">-WhatIf</span></span>
<span data-ttu-id="21b51-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="21b51-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21b51-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="21b51-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21b51-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21b51-135">CommonParameters</span></span>
<span data-ttu-id="21b51-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21b51-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21b51-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21b51-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21b51-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="21b51-138">INPUTS</span></span>

### <span data-ttu-id="21b51-139">System. String</span><span class="sxs-lookup"><span data-stu-id="21b51-139">System.String</span></span>

## <span data-ttu-id="21b51-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="21b51-140">OUTPUTS</span></span>

### <span data-ttu-id="21b51-141">Microsoft. Azure. commands. valv. Models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="21b51-141">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="21b51-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="21b51-142">NOTES</span></span>

## <span data-ttu-id="21b51-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="21b51-143">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

