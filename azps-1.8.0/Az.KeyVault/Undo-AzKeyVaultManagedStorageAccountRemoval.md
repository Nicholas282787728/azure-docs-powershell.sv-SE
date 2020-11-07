---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstorageaccountremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
ms.openlocfilehash: 642c5ff36fb0647907cf72218bd626bcdafe19ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916205"
---
# <span data-ttu-id="c04bd-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="c04bd-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span></span>

## <span data-ttu-id="c04bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c04bd-102">SYNOPSIS</span></span>
<span data-ttu-id="c04bd-103">Återställer ett tidigare borttaget valv-hanterat lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="c04bd-103">Recovers a previously deleted KeyVault-managed storage account.</span></span>

## <span data-ttu-id="c04bd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c04bd-104">SYNTAX</span></span>

### <span data-ttu-id="c04bd-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="c04bd-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c04bd-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c04bd-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-InputObject] <PSDeletedKeyVaultManagedStorageAccountIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c04bd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c04bd-107">DESCRIPTION</span></span>
<span data-ttu-id="c04bd-108">Med kommandot **Ångra-AzKeyVaultManagedStorageAccountRemoval** återställer du ett tidigare borttaget hanterat lagrings konto, förutsatt att den mjuka borttagningen är aktive rad för detta valv och att försöket att återställa sker under återställnings intervallet.</span><span class="sxs-lookup"><span data-stu-id="c04bd-108">The **Undo-AzKeyVaultManagedStorageAccountRemoval** command recovers a previously deleted managed storage account, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="c04bd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c04bd-109">EXAMPLES</span></span>

### <span data-ttu-id="c04bd-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c04bd-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName myVault -Name myAccount -InRemovedState
PS C:\> Undo-AzKeyVaultManagedStorageAccountRemoval -VaultName myVault -Name myAccount

Id                  : https://myvault.vault.azure.net:443/storage/myaccount
Vault Name          : myVault
AccountName         : myAccount
Account Resource Id : /subscriptions/8bc48661-1801-4b7a-8ca1-6a3cadfb4870/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/myaccount
Active Key Name     : key2
Auto Regenerate Key : False
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="c04bd-111">Denna kommandosekvens bestämmer om det angivna lagrings kontot finns i valvet i ett borttaget läge. det efterföljande kommandot återställer det borttagna lagrings kontot och återställer det till ett aktivt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="c04bd-111">This sequence of commands determines whether the specified storage account exists in the vault in a deleted state; the subsequent command recovers the deleted storage account, bringing it back into an active state.</span></span>

## <span data-ttu-id="c04bd-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c04bd-112">PARAMETERS</span></span>

### <span data-ttu-id="c04bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c04bd-113">-DefaultProfile</span></span>
<span data-ttu-id="c04bd-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c04bd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c04bd-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c04bd-115">-InputObject</span></span>
<span data-ttu-id="c04bd-116">Borttaget hanterat lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="c04bd-116">Deleted Managed Storage Account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c04bd-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="c04bd-117">-Name</span></span>
<span data-ttu-id="c04bd-118">Namn på det hanterade lagrings kontot för valv.</span><span class="sxs-lookup"><span data-stu-id="c04bd-118">Name of the KeyVault managed storage account.</span></span>
<span data-ttu-id="c04bd-119">Cmdlet konstruerar FQDN för målet från valv namnet, den valda miljön och namnet på det hanterade lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="c04bd-119">Cmdlet constructs the FQDN of the target from vault name, currently selected environment and the name of the managed storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04bd-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c04bd-120">-VaultName</span></span>
<span data-ttu-id="c04bd-121">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="c04bd-121">Vault name.</span></span>
<span data-ttu-id="c04bd-122">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="c04bd-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="c04bd-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c04bd-123">-Confirm</span></span>
<span data-ttu-id="c04bd-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c04bd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c04bd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c04bd-125">-WhatIf</span></span>
<span data-ttu-id="c04bd-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c04bd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c04bd-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c04bd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c04bd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c04bd-128">CommonParameters</span></span>
<span data-ttu-id="c04bd-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c04bd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c04bd-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c04bd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c04bd-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c04bd-131">INPUTS</span></span>

### <span data-ttu-id="c04bd-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c04bd-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="c04bd-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c04bd-133">OUTPUTS</span></span>

### <span data-ttu-id="c04bd-134">Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c04bd-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="c04bd-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c04bd-135">NOTES</span></span>

## <span data-ttu-id="c04bd-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c04bd-136">RELATED LINKS</span></span>
