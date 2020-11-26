---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
ms.openlocfilehash: 98a3a023564c2c61f1398856e8a089276aeae7bc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259598"
---
# <span data-ttu-id="41088-101">Undo-AzKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="41088-101">Undo-AzKeyVaultRemoval</span></span>

## <span data-ttu-id="41088-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="41088-102">SYNOPSIS</span></span>
<span data-ttu-id="41088-103">Återställer ett borttaget Key-valv till ett aktivt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="41088-103">Recovers a deleted key vault into an active state.</span></span>

## <span data-ttu-id="41088-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="41088-104">SYNTAX</span></span>

### <span data-ttu-id="41088-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="41088-105">Default (Default)</span></span>
```
Undo-AzKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41088-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="41088-106">InputObject</span></span>
```
Undo-AzKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41088-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="41088-107">DESCRIPTION</span></span>
<span data-ttu-id="41088-108">Med cmdleten **Undo-AzKeyVaultRemoval** återställs ett tidigare borttaget valv.</span><span class="sxs-lookup"><span data-stu-id="41088-108">The **Undo-AzKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="41088-109">Det återställda valvet kommer att vara aktivt efter återställning</span><span class="sxs-lookup"><span data-stu-id="41088-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="41088-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="41088-110">EXAMPLES</span></span>

### <span data-ttu-id="41088-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="41088-111">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}

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

<span data-ttu-id="41088-112">Det här kommandot återställer nyckelordet ' MyKeyVault ' som tidigare tagits bort från eastus2 region och resurs gruppen ' MyResourceGroup ' i ett aktivt och användbart tillstånd.</span><span class="sxs-lookup"><span data-stu-id="41088-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="41088-113">Den ersätter också taggarna med ny tagg.</span><span class="sxs-lookup"><span data-stu-id="41088-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="41088-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="41088-114">PARAMETERS</span></span>

### <span data-ttu-id="41088-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41088-115">-DefaultProfile</span></span>
<span data-ttu-id="41088-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="41088-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41088-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41088-117">-InputObject</span></span>
<span data-ttu-id="41088-118">Objekt som tagits bort</span><span class="sxs-lookup"><span data-stu-id="41088-118">Deleted vault object</span></span>

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

### <span data-ttu-id="41088-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="41088-119">-Location</span></span>
<span data-ttu-id="41088-120">Anger det ursprungliga Azure-området för det borttagna valvet.</span><span class="sxs-lookup"><span data-stu-id="41088-120">Specifies the deleted vault original Azure region.</span></span>

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

### <span data-ttu-id="41088-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41088-121">-ResourceGroupName</span></span>
<span data-ttu-id="41088-122">Anger namnet på en befintlig resurs grupp där nyckelords valvet ska skapas.</span><span class="sxs-lookup"><span data-stu-id="41088-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="41088-123">-Tagg</span><span class="sxs-lookup"><span data-stu-id="41088-123">-Tag</span></span>
<span data-ttu-id="41088-124">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="41088-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="41088-125">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="41088-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="41088-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="41088-126">-VaultName</span></span>
<span data-ttu-id="41088-127">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="41088-127">Vault name.</span></span>
<span data-ttu-id="41088-128">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="41088-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="41088-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="41088-129">-Confirm</span></span>
<span data-ttu-id="41088-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="41088-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41088-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41088-131">-WhatIf</span></span>
<span data-ttu-id="41088-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="41088-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41088-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="41088-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41088-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41088-134">CommonParameters</span></span>
<span data-ttu-id="41088-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41088-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41088-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41088-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41088-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="41088-137">INPUTS</span></span>

### <span data-ttu-id="41088-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="41088-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="41088-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="41088-139">OUTPUTS</span></span>

### <span data-ttu-id="41088-140">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="41088-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="41088-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="41088-141">NOTES</span></span>

## <span data-ttu-id="41088-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="41088-142">RELATED LINKS</span></span>

[<span data-ttu-id="41088-143">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="41088-143">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)

[<span data-ttu-id="41088-144">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="41088-144">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="41088-145">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="41088-145">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)