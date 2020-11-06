---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurermkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
ms.openlocfilehash: af6ed0e4db688cdc9ad6da598c0bc240e9b3c958
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576952"
---
# <span data-ttu-id="751da-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="751da-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="751da-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="751da-102">SYNOPSIS</span></span>
<span data-ttu-id="751da-103">Återställer ett borttaget Key-valv till ett aktivt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="751da-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="751da-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="751da-104">SYNTAX</span></span>

### <span data-ttu-id="751da-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="751da-105">Default (Default)</span></span>
```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="751da-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="751da-106">InputObject</span></span>
```
Undo-AzureRmKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="751da-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="751da-107">DESCRIPTION</span></span>
<span data-ttu-id="751da-108">Med cmdleten **Undo-AzureRmKeyVaultRemoval** återställs ett tidigare borttaget valv.</span><span class="sxs-lookup"><span data-stu-id="751da-108">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="751da-109">Det återställda valvet kommer att vara aktivt efter återställning</span><span class="sxs-lookup"><span data-stu-id="751da-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="751da-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="751da-110">EXAMPLES</span></span>

### <span data-ttu-id="751da-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="751da-111">Example 1</span></span>
```powershell
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}

Vault Name                       : MyKeyVault
Resource Group Name              : MyResourceGroup
Location                         : eastus2
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers
                                   /Microsoft.KeyVault/vaults/mykeyvault
Vault URI                        : https://mykeyvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : True
Enabled For Disk Encryption?     : True
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update

Tags                             :
                                   Name  Value
                                   ====  =====
                                   x     y
```

<span data-ttu-id="751da-112">Det här kommandot återställer nyckelordet ' MyKeyVault ' som tidigare tagits bort från eastus2 region och resurs gruppen ' MyResourceGroup ' i ett aktivt och användbart tillstånd.</span><span class="sxs-lookup"><span data-stu-id="751da-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="751da-113">Den ersätter också taggarna med ny tagg.</span><span class="sxs-lookup"><span data-stu-id="751da-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="751da-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="751da-114">PARAMETERS</span></span>

### <span data-ttu-id="751da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="751da-115">-DefaultProfile</span></span>
<span data-ttu-id="751da-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="751da-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="751da-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="751da-117">-InputObject</span></span>
<span data-ttu-id="751da-118">Objekt som tagits bort</span><span class="sxs-lookup"><span data-stu-id="751da-118">Deleted vault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="751da-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="751da-119">-Location</span></span>
<span data-ttu-id="751da-120">Anger det ursprungliga Azure-området för det borttagna valvet.</span><span class="sxs-lookup"><span data-stu-id="751da-120">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="751da-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="751da-121">-ResourceGroupName</span></span>
<span data-ttu-id="751da-122">Anger namnet på en befintlig resurs grupp där nyckelords valvet ska skapas.</span><span class="sxs-lookup"><span data-stu-id="751da-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="751da-123">-Tagg</span><span class="sxs-lookup"><span data-stu-id="751da-123">-Tag</span></span>
<span data-ttu-id="751da-124">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="751da-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="751da-125">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="751da-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="751da-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="751da-126">-VaultName</span></span>
<span data-ttu-id="751da-127">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="751da-127">Vault name.</span></span>
<span data-ttu-id="751da-128">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="751da-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="751da-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="751da-129">-Confirm</span></span>
<span data-ttu-id="751da-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="751da-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="751da-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="751da-131">-WhatIf</span></span>
<span data-ttu-id="751da-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="751da-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="751da-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="751da-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="751da-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="751da-134">CommonParameters</span></span>
<span data-ttu-id="751da-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="751da-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="751da-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="751da-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="751da-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="751da-137">INPUTS</span></span>

### <span data-ttu-id="751da-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="751da-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>
<span data-ttu-id="751da-139">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="751da-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="751da-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="751da-140">OUTPUTS</span></span>

### <span data-ttu-id="751da-141">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="751da-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="751da-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="751da-142">NOTES</span></span>

## <span data-ttu-id="751da-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="751da-143">RELATED LINKS</span></span>

[<span data-ttu-id="751da-144">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="751da-144">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="751da-145">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="751da-145">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="751da-146">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="751da-146">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)
