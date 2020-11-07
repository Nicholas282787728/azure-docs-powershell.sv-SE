---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 392c8aa5259419851d3cb85967ddf85afa3c94de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926833"
---
# <span data-ttu-id="aaa61-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="aaa61-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="aaa61-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aaa61-102">SYNOPSIS</span></span>
<span data-ttu-id="aaa61-103">Tar bort en Key valv Managed-definitioner för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="aaa61-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="aaa61-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aaa61-104">SYNTAX</span></span>

### <span data-ttu-id="aaa61-105">ByDefinitionName (standard)</span><span class="sxs-lookup"><span data-stu-id="aaa61-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaa61-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="aaa61-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaa61-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aaa61-107">DESCRIPTION</span></span>
<span data-ttu-id="aaa61-108">Tar bort en Key valv Managed-definitioner för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="aaa61-108">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="aaa61-109">Detta tar också bort hemligheten som används för att hämta SAS-token per denna säkerhets Association.</span><span class="sxs-lookup"><span data-stu-id="aaa61-109">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="aaa61-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aaa61-110">EXAMPLES</span></span>

### <span data-ttu-id="aaa61-111">Exempel 1: ta bort en Key valv Managed definition för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="aaa61-111">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="aaa61-112">Tar bort säkerhets associationer för Managed Storage mysasdef associerat med kontot ' mystorageaccount ' i valv för valvet.</span><span class="sxs-lookup"><span data-stu-id="aaa61-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="aaa61-113">Exempel 2: ta bort en Key valv Managed definition av Azure-lagring utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="aaa61-113">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru -Force

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="aaa61-114">Tar bort säkerhets associationer för Managed Storage mysasdef associerat med kontot ' mystorageaccount ' i valv för valvet.</span><span class="sxs-lookup"><span data-stu-id="aaa61-114">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="aaa61-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aaa61-115">PARAMETERS</span></span>

### <span data-ttu-id="aaa61-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="aaa61-116">-AccountName</span></span>
<span data-ttu-id="aaa61-117">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="aaa61-117">Storage account name.</span></span>
<span data-ttu-id="aaa61-118">Cmdlet konstruerar FQDN för ett hanterat lagrings konto namn från ett valv namn, valt miljö-och lagrings konto namn.</span><span class="sxs-lookup"><span data-stu-id="aaa61-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa61-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaa61-119">-DefaultProfile</span></span>
<span data-ttu-id="aaa61-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="aaa61-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aaa61-121">-Force</span><span class="sxs-lookup"><span data-stu-id="aaa61-121">-Force</span></span>
<span data-ttu-id="aaa61-122">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="aaa61-122">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa61-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aaa61-123">-InputObject</span></span>
<span data-ttu-id="aaa61-124">ManagedStorageSasDefinition-objekt.</span><span class="sxs-lookup"><span data-stu-id="aaa61-124">ManagedStorageSasDefinition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aaa61-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="aaa61-125">-Name</span></span>
<span data-ttu-id="aaa61-126">Namn på lagrings-sa.</span><span class="sxs-lookup"><span data-stu-id="aaa61-126">Storage sas definition name.</span></span>
<span data-ttu-id="aaa61-127">Cmdlet konstruerar FQDN-namnet på en lagrings-säkerhets Association från ett valv namn, för närvarande valda miljö-, lagrings konto namn och SAS-namn.</span><span class="sxs-lookup"><span data-stu-id="aaa61-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa61-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aaa61-128">-PassThru</span></span>
<span data-ttu-id="aaa61-129">Cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="aaa61-129">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="aaa61-130">Om denna växel anges returnerar cmdlet det hanterade lagrings konto som har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="aaa61-130">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa61-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="aaa61-131">-VaultName</span></span>
<span data-ttu-id="aaa61-132">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="aaa61-132">Vault name.</span></span>
<span data-ttu-id="aaa61-133">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="aaa61-133">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa61-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="aaa61-134">-Confirm</span></span>
<span data-ttu-id="aaa61-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aaa61-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa61-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaa61-136">-WhatIf</span></span>
<span data-ttu-id="aaa61-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="aaa61-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaa61-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="aaa61-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa61-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaa61-139">CommonParameters</span></span>
<span data-ttu-id="aaa61-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaa61-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaa61-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aaa61-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaa61-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aaa61-142">INPUTS</span></span>

### <span data-ttu-id="aaa61-143">Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="aaa61-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="aaa61-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aaa61-144">OUTPUTS</span></span>

### <span data-ttu-id="aaa61-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="aaa61-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="aaa61-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aaa61-146">NOTES</span></span>

## <span data-ttu-id="aaa61-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aaa61-147">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

