---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 0fe20196f805f292ecc6b351fbb9138c6617bb4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916261"
---
# <span data-ttu-id="f1451-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="f1451-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="f1451-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f1451-102">SYNOPSIS</span></span>
<span data-ttu-id="f1451-103">Tar bort en Key valv Managed-definitioner för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="f1451-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="f1451-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f1451-104">SYNTAX</span></span>

### <span data-ttu-id="f1451-105">ByDefinitionName (standard)</span><span class="sxs-lookup"><span data-stu-id="f1451-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1451-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f1451-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1451-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f1451-107">DESCRIPTION</span></span>
<span data-ttu-id="f1451-108">Tar bort en Key valv Managed-definitioner för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="f1451-108">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="f1451-109">Detta tar också bort hemligheten som används för att hämta SAS-token per denna säkerhets Association.</span><span class="sxs-lookup"><span data-stu-id="f1451-109">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="f1451-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f1451-110">EXAMPLES</span></span>

### <span data-ttu-id="f1451-111">Exempel 1: ta bort en Key valv Managed definition för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="f1451-111">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="f1451-112">Tar bort säkerhets associationer för Managed Storage mysasdef associerat med kontot ' mystorageaccount ' i valv för valvet.</span><span class="sxs-lookup"><span data-stu-id="f1451-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="f1451-113">Exempel 2: ta bort en Key valv Managed definition av Azure-lagring utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f1451-113">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru -Force

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="f1451-114">Tar bort säkerhets associationer för Managed Storage mysasdef associerat med kontot ' mystorageaccount ' i valv för valvet.</span><span class="sxs-lookup"><span data-stu-id="f1451-114">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="f1451-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f1451-115">PARAMETERS</span></span>

### <span data-ttu-id="f1451-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f1451-116">-AccountName</span></span>
<span data-ttu-id="f1451-117">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="f1451-117">Storage account name.</span></span>
<span data-ttu-id="f1451-118">Cmdlet konstruerar FQDN för ett hanterat lagrings konto namn från ett valv namn, valt miljö-och lagrings konto namn.</span><span class="sxs-lookup"><span data-stu-id="f1451-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

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

### <span data-ttu-id="f1451-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1451-119">-DefaultProfile</span></span>
<span data-ttu-id="f1451-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f1451-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1451-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f1451-121">-Force</span></span>
<span data-ttu-id="f1451-122">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f1451-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f1451-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1451-123">-InputObject</span></span>
<span data-ttu-id="f1451-124">ManagedStorageSasDefinition-objekt.</span><span class="sxs-lookup"><span data-stu-id="f1451-124">ManagedStorageSasDefinition object.</span></span>

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

### <span data-ttu-id="f1451-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="f1451-125">-Name</span></span>
<span data-ttu-id="f1451-126">Namn på lagrings-sa.</span><span class="sxs-lookup"><span data-stu-id="f1451-126">Storage sas definition name.</span></span>
<span data-ttu-id="f1451-127">Cmdlet konstruerar FQDN-namnet på en lagrings-säkerhets Association från ett valv namn, för närvarande valda miljö-, lagrings konto namn och SAS-namn.</span><span class="sxs-lookup"><span data-stu-id="f1451-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="f1451-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1451-128">-PassThru</span></span>
<span data-ttu-id="f1451-129">Cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="f1451-129">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f1451-130">Om denna växel anges returnerar cmdlet det hanterade lagrings konto som har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="f1451-130">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="f1451-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f1451-131">-VaultName</span></span>
<span data-ttu-id="f1451-132">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="f1451-132">Vault name.</span></span>
<span data-ttu-id="f1451-133">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="f1451-133">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f1451-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f1451-134">-Confirm</span></span>
<span data-ttu-id="f1451-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f1451-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1451-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1451-136">-WhatIf</span></span>
<span data-ttu-id="f1451-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f1451-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1451-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f1451-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1451-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1451-139">CommonParameters</span></span>
<span data-ttu-id="f1451-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1451-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1451-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1451-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1451-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f1451-142">INPUTS</span></span>

### <span data-ttu-id="f1451-143">Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f1451-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="f1451-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f1451-144">OUTPUTS</span></span>

### <span data-ttu-id="f1451-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="f1451-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="f1451-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f1451-146">NOTES</span></span>

## <span data-ttu-id="f1451-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f1451-147">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

