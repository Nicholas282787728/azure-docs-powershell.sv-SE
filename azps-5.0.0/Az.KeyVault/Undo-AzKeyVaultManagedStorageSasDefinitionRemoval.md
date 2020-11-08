---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstoragesasdefinitionremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
ms.openlocfilehash: bb44bc8f5e4537691d1e5d5493a29111ceaf42a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272272"
---
# <span data-ttu-id="16dfc-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span><span class="sxs-lookup"><span data-stu-id="16dfc-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span></span>

## <span data-ttu-id="16dfc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="16dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="16dfc-103">Återställer en tidigare borttagen valv-hanterad säkerhets Association för mellanlagring.</span><span class="sxs-lookup"><span data-stu-id="16dfc-103">Recovers a previously deleted KeyVault-managed storage SAS definition.</span></span>

## <span data-ttu-id="16dfc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="16dfc-104">SYNTAX</span></span>

### <span data-ttu-id="16dfc-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="16dfc-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-VaultName] <String> [-AccountName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16dfc-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="16dfc-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-AccountName] <String>
 [-InputObject] <PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16dfc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="16dfc-107">DESCRIPTION</span></span>
<span data-ttu-id="16dfc-108">Kommandot **Ångra-AzKeyVaultManagedStorageSasDefinitionRemoval** återställer en tidigare borttagen HANTERAD säkerhets Association för lagring, förutsatt att den mjuka borttagningen är aktive rad för det här valvet och att försöket att återställa sker under återställnings intervallet.</span><span class="sxs-lookup"><span data-stu-id="16dfc-108">The **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** command recovers a previously deleted managed storage SAS definition, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="16dfc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="16dfc-109">EXAMPLES</span></span>

### <span data-ttu-id="16dfc-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="16dfc-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName myVault -AccountName myAccount -Name mySasName -InRemovedState
PS C:\> Undo-AzKeyVaultManagedStorageSasDefinitionRemoval -VaultName myVault -AccountName myAccount -Name mySasName

Id          : https://myvault.vault.azure.net:443/storage/myaccount/sas/mysasname
Secret Id   : https://myvault.vault.azure.net/secrets/myaccount-mysasname
Vault Name  : myVault
AccountName : myAccount
Name        : mySasName
Parameter   :
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="16dfc-111">Denna kommandosekvens bestämmer om den angivna definitionen för lagrings-SAS finns i valvet i ett borttaget tillstånd; det efterföljande kommandot återställer den borttagna SAS-definitionen och återställer den till ett aktivt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="16dfc-111">This sequence of commands determines whether the specified storage SAS definition exists in the vault in a deleted state; the subsequent command recovers the deleted sas definition, bringing it back into an active state.</span></span>

## <span data-ttu-id="16dfc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="16dfc-112">PARAMETERS</span></span>

### <span data-ttu-id="16dfc-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="16dfc-113">-AccountName</span></span>
<span data-ttu-id="16dfc-114">Namn på hanterat lagrings konto för valv.</span><span class="sxs-lookup"><span data-stu-id="16dfc-114">KeyVault-managed storage account name.</span></span>
<span data-ttu-id="16dfc-115">Cmdlet konstruerar FQDN för en säkerhets Association för hanterade lagrings enheter från valv namn, för närvarande-vald miljö och hanterat lagrings konto namn.</span><span class="sxs-lookup"><span data-stu-id="16dfc-115">Cmdlet constructs the FQDN of a managed storage SAS definition from vault name, currently-selected environment and managed storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16dfc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16dfc-116">-DefaultProfile</span></span>
<span data-ttu-id="16dfc-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="16dfc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16dfc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16dfc-118">-InputObject</span></span>
<span data-ttu-id="16dfc-119">Definitions objekt för Managed Storage-SÄKERHETSASSOCIATIONER</span><span class="sxs-lookup"><span data-stu-id="16dfc-119">Deleted managed storage SAS definition object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16dfc-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="16dfc-120">-Name</span></span>
<span data-ttu-id="16dfc-121">Namn på den säkerhetsdefinierade säkerhets associationen för det hanterade lagrings utrymmet.</span><span class="sxs-lookup"><span data-stu-id="16dfc-121">Name of the KeyVault-managed storage SAS definition.</span></span>
<span data-ttu-id="16dfc-122">Cmdlet konstruerar FQDN för målet från valv namn, för närvarande-vald miljö, namnet på det hanterade lagrings kontot och namnet på SAS-definitionen.</span><span class="sxs-lookup"><span data-stu-id="16dfc-122">Cmdlet constructs the FQDN of the target from vault name, currently-selected environment, the name of the managed storage account and the name of the SAS definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16dfc-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="16dfc-123">-VaultName</span></span>
<span data-ttu-id="16dfc-124">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="16dfc-124">Vault name.</span></span>
<span data-ttu-id="16dfc-125">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="16dfc-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16dfc-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="16dfc-126">-Confirm</span></span>
<span data-ttu-id="16dfc-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="16dfc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16dfc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16dfc-128">-WhatIf</span></span>
<span data-ttu-id="16dfc-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="16dfc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16dfc-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="16dfc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16dfc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16dfc-131">CommonParameters</span></span>
<span data-ttu-id="16dfc-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16dfc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16dfc-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16dfc-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16dfc-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="16dfc-134">INPUTS</span></span>

### <span data-ttu-id="16dfc-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="16dfc-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="16dfc-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="16dfc-136">OUTPUTS</span></span>

### <span data-ttu-id="16dfc-137">Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="16dfc-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="16dfc-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="16dfc-138">NOTES</span></span>

## <span data-ttu-id="16dfc-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="16dfc-139">RELATED LINKS</span></span>
